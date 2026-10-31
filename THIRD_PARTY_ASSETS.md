# Third-party assets and dataset provenance inventory

**Priority: review raw EEG files for recording consent, de-identification and publication rights.** This is a rights/privacy check, not an assertion that the files contain personal information.

| Item | Path | Observation | Status / action |
|---|---|---|---|
| EEG recording CSVs | `thisone/*.md.csv` | Multiple large exported recordings are committed | **Consent, origin and redistribution rights unverified**. Determine source/participants, consent, de-identification and whether public release is permitted |
| Recording interval markers | `thisone/*intervalMarker.csv` | Timing annotations accompanying recordings | Review alongside recording consent and metadata sensitivity |
| Simulated EEG/EOG experiments | Code described in README | Local synthetic experiments described | Verify which plots/data are simulated versus measured |
| Reference article | DOI `10.1016/S0165-1684(96)00129-6` | Scholarly reference, not a software/data license | Cite source; do not assume redistribution rights for publisher content |
| Team contributions | README names four team members | Collaborative project | Confirm contributor rights for code and data before applying MIT broadly |

This file is an inventory, not authorization to publish physiological recordings. Review all existing copies and history if a recording is found to have been uploaded without permission.
