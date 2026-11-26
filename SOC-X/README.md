# SOC-X | Security Operations & Incident Response Lab

A hands-on Microsoft security operations portfolio by Farhan Fathah — [Professional portfolio](https://farhanfathah.com).

## Overview
SOC-X documents security monitoring, detection engineering, alert triage and response exercises in an authorized home lab. It builds on an IT operations and NOC background and practical Microsoft security training. Microsoft SC-300 completed; SC-200 preparation ongoing.

## Case studies
| Case | Exercise | Recorded outcome |
|---|---|---|
| [01](investigations/01-rdp.md) | RDP investigation | RemoteInteractive login and subsequent shell activity observed |
| [02](investigations/02-asr.md) | Attack surface reduction | Audit event 1122 and block event 1121 observed |
| [03](investigations/03-dlp.md) | Endpoint DLP | TXT upload blocked; DOCX upload audited |
| [04](investigations/04-oauth.md) | OAuth investigation | Mailbox access reviewed; permissions revoked in exercise |
| [05](investigations/05-phishing.md) | Safe Links investigation | ClickAllowed observed; investigation completed with no threats found |
| [06](investigations/06-authentication.md) | Authentication monitoring | Windows and Linux telemetry queried |
| [07](investigations/07-app-control.md) | Application control | Code Integrity audit observed |
| [08](investigations/08-account-creation.md) | Account creation analytics | Low severity alert created and resolved |

## Architecture
See [architecture](architecture/overview.md). The environment includes Windows, Active Directory, Ubuntu, Kali, OPNsense, Sentinel, Defender XDR and a separate CYBER OS ESP32 monitoring project.

## Detection engineering
The [detections](detections/) directory contains reconstructed KQL examples for the exercises. These are candidate queries, not exported production rules. See [validation](tests/validation.md) before deployment.

## Evidence and limitations
Outcomes are reconstructed from previously reported lab observations, not independently verified from raw exports. Screenshots, incident IDs, exact timestamps and original rule exports are intentionally omitted until sanitized originals are available. No employer or customer data is included. Exercises are not claims of production incident handling. MITRE mappings identify relevant behavior, not proof of malicious intent.

## Security
Use only authorized systems. Do not commit access tokens, tenant IDs, personal identifiers, real incident data or private keys. CYBER OS integration is described separately; firmware and API credentials are not included.
