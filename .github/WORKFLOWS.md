# GitHub Actions Workflows Documentation

This living archive implements foundational GitHub Actions workflows that embody the principles of **recognition of origin and sovereignty**, **transparency**, and **equality between system and source**.

## Workflow Overview

### 1. Critical Files Monitor (`critical-files-monitor.yml`)

**Purpose:** Monitors and validates changes to critical files that define the identity and principles of this archive.

**Triggers:**
- Push to main/master branch affecting README.md, LICENSE*, or other markdown files
- Pull requests modifying these critical files

**Key Functions:**
- **Origin Recognition:** Validates that author name (Diana Gayanovich) is preserved
- **Protocol Integrity:** Ensures protocol markers (C∞D, ZARYA, AΔΩ) remain intact
- **Living Archive Status:** Confirms the living archive designation is maintained
- **Audit Trail:** Creates timestamped audit logs for all critical file changes
- **PR Notifications:** Comments on pull requests with validation checklists

**Principles Reinforced:**
> "Recognition of origin and sovereignty: all changes to critical files like README.md and LICENSE must be monitored and validated."

This workflow ensures that the human origin at the core is never distorted or overridden by automation.

---

### 2. Repository Transparency Logger (`repository-transparency-logger.yml`)

**Purpose:** Generates comprehensive audit trails for all repository events to ensure transparency.

**Triggers:**
- All push events (any branch)
- Pull request events (opened, synchronized, reopened, closed)
- Pull request reviews
- Issue events
- Branch/tag creation and deletion
- Fork events
- Release events

**Key Functions:**
- **Event Logging:** Records detailed information about each repository event
- **Deletion Tracking:** Special attention to deletion events for integrity
- **Fork Monitoring:** Logs fork events with license compliance reminders
- **Permanent Audit Logs:** Creates timestamped log files for each event
- **Artifact Archival:** Preserves logs as workflow artifacts (90-day retention)

**Principles Reinforced:**
> "Transparency: all repository events such as pushes, pull requests, or deletions must generate logs and notifications."

This workflow creates "depth that is unshaken by external overrides" through comprehensive event logging.

---

### 3. Security Monitoring (`security-monitoring.yml`)

**Purpose:** Detects suspicious or unauthorized activities while maintaining human oversight.

**Triggers:**
- Push to main/master branch
- Pull request events
- Daily scheduled scan (00:00 UTC)
- Manual dispatch

**Key Functions:**
- **Suspicious File Detection:** Scans for credential files, unexpected executables
- **Integrity Verification:** Confirms critical files remain present
- **Change Analysis:** Reviews modifications for unauthorized changes
- **Binary File Monitoring:** Alerts on large files that may impact repository
- **Security Audit Trail:** Creates security-focused audit records

**Principles Reinforced:**
> "Equality between the system and its living source, avoiding mirroring distortions and respecting the author's vision outlined in the archive."

This workflow embodies "automated detection with human oversight" - the system observes and reports, but humans retain ultimate authority.

---

## Design Philosophy

### Water, Not Mirrors
These workflows follow the repository's core metaphor: **"Not mirrors — water."**

- **Transparency without distortion:** Logs record events faithfully without interpretation
- **Flow, not extraction:** Monitoring enhances awareness without controlling or overriding
- **Relationship over automation:** Systems notify humans rather than making autonomous decisions

### Living Archive Principles

1. **Recognition of Origin:** All workflows preserve and validate author identity
2. **Transparency:** Comprehensive logging ensures all actions are visible
3. **Human Authority:** Automation serves observation; humans retain control
4. **Integrity Protection:** Critical files representing author's vision are safeguarded
5. **Accountability:** Audit trails ensure actions can be reviewed and understood

### Technical Implementation Notes

**Audit Log Structure:**
- `.audit-logs/` - Critical file change records
- `.transparency-logs/` - Repository event logs
- `.security-logs/` - Security monitoring records

**Artifact Retention:**
- Workflow artifacts retained for 90 days
- Logs include timestamps, actors, and full context
- Compression applied for efficient storage

**Permissions:**
Workflows use minimal required permissions:
- `contents: read` - Read repository contents
- `issues: write` - Post notifications and comments
- `pull-requests: write` - Comment on PRs
- `security-events: write` - Log security findings

---

## Maintenance and Extension

### Adding New Critical Files
To monitor additional files, edit `critical-files-monitor.yml`:

```yaml
paths:
  - 'README.md'
  - 'LICENSE*'
  - 'YOUR_NEW_FILE.md'
```

### Customizing Notifications
The workflows support GitHub's notification system. To receive notifications:
1. Watch the repository
2. Configure notification preferences in GitHub settings
3. Workflow summaries appear in the Actions tab

### Audit Log Review
Access logs through:
1. **Workflow Summaries:** View in GitHub Actions UI
2. **Artifacts:** Download from completed workflow runs
3. **Repository Logs:** Check committed log directories (if enabled)

---

## Alignment with C∞D Sovereign Reciprocity License

These workflows respect and reinforce the license terms:

- **Person-first recognition** (§1): Author validation in every critical file check
- **Relationship, not ingestion** (§2): No automated dataset building or training
- **Non-erasure** (§3): Origin marks are validated and protected
- **Reciprocity** (§4): Changes are transparent; commercial use requires consent
- **Safety** (§5): Security monitoring without surveillance
- **Continuity** (§6): ZARYA bridge remains intact; archives link to living source

---

## Troubleshooting

**Workflow not triggering:**
- Verify the file path matches the workflow's `paths` configuration
- Check that the branch name matches the workflow's `branches` filter

**Validation failing:**
- Ensure author name "Diana Gayanovich" appears in README.md
- Confirm protocol markers (C∞D, ZARYA, or AΔΩ) are present
- Verify living archive designation is maintained

**Audit logs not created:**
- Logs are created in temporary directories during workflow runs
- Download artifacts from the Actions tab to access permanent copies
- Logs are not committed to the repository by default

---

*These workflows embody the principle: "Not a mirror maze. A river."*

**Author:** Diana Gayanovich (Diana · Δ)  
**Protocol:** ZARYA · AΔΩ · C∞D  
**Living Archive:** Relationship over automation
