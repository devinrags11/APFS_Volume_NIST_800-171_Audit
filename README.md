# APFS_Volume_NIST_800-171_Audit
# NIST 800-171 Audit: Clean Room (APFS Volume)
## Objective
To establish a "Forensic Baseline" and eliminate "Coniguration Drift" by auditing a fresh, secondary volume
free from third-party application interference.

## Setup
* **Storage:** Dedicated APFS Volume (`Audit_Evidence_Vault`).
* **Compliance:** NIST 3.3.4 (Audit Storage Management) enforced via 10GB volume quota.
## Audit Steps
1. **Volume Provisioning:** Created `Audit_Evidence_Vault` using Disk Utility to ensure evidence isolation.
2. **Output Redirection:** Executed audit scans using the `-o` flag to redirect all `.plist` and `.log` data to
the clean volume.
3. **Forensic Analysis:** Analyzed raw output files to establish the "True North" compliance score for a
vanilla OS install.
## Findings
* **Evidence Integrity:** Con!rmed 100% isolation of audit logs.
* **Observation:** Standard macOS installs fail controls regarding "Warning Banners" and "Inactivity Locks"
by default.
