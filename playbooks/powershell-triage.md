# Playbook — Suspicious PowerShell (T1059.001)

**Goal:** Triage and scope suspicious PowerShell execution with obfuscation or stealth flags.

---

## Where to Look
- **Wazuh Dashboard** → Security Events → Windows → Process Create
- **Windows Event Logs** (via Wazuh):
  - Sysmon **Event ID 1** (Process Create)
  - Security **4688** (Process Creation) if enabled
- **Command line** field (Image, ParentImage, CommandLine)

---

## Red Flags (Examples)
- `powershell.exe -nop -w hidden -enc ...`
- `-NoProfile`, `-ExecutionPolicy Bypass`, `-EncodedCommand`
- PowerShell spawned from Office, browser, or `wscript.exe`

---

## Triage Steps
1. **Confirm alert details**: user, host, timestamp, parent process.
2. **Decode** if `-enc` is present (base64). On mac/Linux:
   ```bash
   echo "BASE64_STRING" | base64 -d
