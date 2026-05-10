# fork-sync

Management repository that automatically syncs [@modalware](https://github.com/modalware) DICOM-related fork repositories with their upstreams daily.

## Synced Repositories (12)

| Fork | Schedule |
|------|----------|
| dicom-validator-ts | Daily |
| cornerstone3D | Daily |
| dicom3tools | Daily |
| dcmjs | Daily |
| dwv | Daily |
| dcmtk | Daily |
| dicomweb-client | Daily |
| dicom-validator | Daily |
| pydicom | Daily |
| pynetdicom | Daily |
| dicomParser | Daily |
| DVTk | Daily |

## Schedule

Runs automatically every day at UTC 2:00 (JST 11:00). Manual runs are also available via Actions tab → "Sync Upstream Forks" → "Run workflow".

## Setup

Register a Fine-grained Personal Access Token as a repository secret named `SYNC_TOKEN`.

**Token settings:**
- Resource owner: `modalware`
- Repository access: Select the 12 repositories above
- Permissions: `Contents: Write`
