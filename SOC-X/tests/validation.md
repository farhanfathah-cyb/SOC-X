# Validation checklist

These queries have not been executed in this packaging session. Before marking validated:

- Confirm table availability, column names, connector and audit configuration.
- Generate benign authorized positive test activity and confirm matching rows.
- Run a negative control and record unexpected matches.
- Tune time windows and thresholds; failed logons and allowed URL clicks alone do not establish compromise.
- Record actual query output, timestamp, policy mode and sanitized evidence.
- For ASR, confirm whether WindowsEvent is populated; alternatively inspect Defender Operational logs locally.
- For RDP, correlate process activity separately using DeviceProcessEvents; the supplied query detects logons only.
- Publish only redacted exports; keep any unverified claims marked as such.
