# Local Actions

This directory contains local copies of GitHub Actions for testing purposes only.

## agp-action/

**Purpose:** Local copy of `sonatype/agp-action@v1` for testing.

**Why local?**
- The official action repository is private (sonatype/agp-action)
- External repos cannot access private actions from other organizations
- This local copy allows testing with self-hosted runner

**Official Action:**
- Repository: https://github.com/sonatype/agp-action (private)
- Latest Release: v1.0.0
- Published: 2026-02-09

**Usage:**
```yaml
# Local copy (this repo)
uses: ./.github/actions/agp-action

# Official (only works in Sonatype org repos)
uses: sonatype/agp-action@v1
```

**Keeping in sync:**
This copy should be manually updated when the official action is updated.

```bash
# Update from official repo
cd /path/to/nextjs-app
git show origin/main:.github/actions/agp-action/action.yml > .github/actions/agp-action/action.yml
```
