# fork-sync

Management repository that automatically syncs [@modalware](https://github.com/modalware) DICOM-related repositories with their upstreams.

## Workflows

### Sync Upstream Forks

Syncs 11 forked repositories with their GitHub upstreams daily.

| Fork | Schedule |
|------|----------|
| dicom-validator-ts | Daily (JST 11:00) |
| cornerstone3D | Daily (JST 11:00) |
| dcmjs | Daily (JST 11:00) |
| dwv | Daily (JST 11:00) |
| dcmtk | Daily (JST 11:00) |
| dicomweb-client | Daily (JST 11:00) |
| dicom-validator | Daily (JST 11:00) |
| pydicom | Daily (JST 11:00) |
| pynetdicom | Daily (JST 11:00) |
| dicomParser | Daily (JST 11:00) |
| DVTk | Daily (JST 11:00) |

Manual run: Actions tab → "Sync Upstream Forks" → "Run workflow"

### Sync dicom3tools Snapshots

Checks [dclunie.com](https://dclunie.com/dicom3tools/workinprogress/index.html) for new snapshots monthly and applies them in chronological order to [modalware/dicom3tools](https://github.com/modalware/dicom3tools).

| Repository | Source | Schedule |
|------------|--------|----------|
| dicom3tools | dclunie.com (tarball snapshots) | Monthly 1st (JST 12:00) |

Each new snapshot is committed and tagged as `1.00.snapshot.YYYYMMDDHHMMSS`.

Manual run: Actions tab → "Sync dicom3tools Snapshots" → "Run workflow"

## Setup

Register a Fine-grained Personal Access Token as a repository secret named `SYNC_TOKEN`.

**Token settings:**
- Resource owner: `modalware`
- Repository access: All 12 repositories listed above (including `dicom3tools`)
- Permissions:
  - `Contents: Read and write`
  - `Workflows: Read and write`
