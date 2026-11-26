# Lab architecture

```mermaid
flowchart TD
  K[Kali test host] --> F[OPNsense firewall]
  F --> W[Windows endpoint]
  F --> U[Ubuntu]
  F --> D[AD DS lab server]
  W --> X[Defender XDR]
  U --> S[Microsoft Sentinel]
  W --> S
  D --> X
  X -. Incident monitoring .-> C[Cloudflare Worker]
  S -. Incident monitoring .-> C
  C --> E[CYBER OS ESP32 and iPhone dashboard]
```
Logical architecture, not a verified physical wiring diagram. Individual integrations were exercised at different stages; simultaneous end-to-end operation is not asserted.

- Windows security events and Linux syslog collected through Azure Monitor Agent and data collection rules.
- Ubuntu onboarded to Azure Arc and Defender for Endpoint.
- Windows endpoint onboarded to Defender for Endpoint; ARM Sysmon driver limitation encountered.
- AD DS and DNS configured in a separate lab; Defender for Identity sensor reported healthy, with auditing advisories.
- CYBER OS project reported Sentinel/XDR monitoring through a Cloudflare Worker and iPhone interface.
