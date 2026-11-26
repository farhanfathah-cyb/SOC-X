# Windows and Linux authentication

## Recorded observation
A Windows query returned 213 successful and 2 failed logon events; Linux authpriv info query returned 695 records in a reported exercise.

## Investigation approach
Check time range, account, source and host; distinguish failures from successful authentication.

## Disposition and response
Telemetry validation only; no brute-force incident proven.

## ATT&CK context
T1110 (candidate detection)

## Evidence status
Reconstructed from prior lab notes. Original event exports, screenshots and exact timestamps not included. Investigation approach is a recommended workflow, not a claim that every step was performed.

## Candidate query
[View KQL](../detections/failed-logons.kql)
