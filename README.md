# Cloudflare-Software-Repo
Cloudflare D2 storage-based enterprise software distribution

## Work in progress...

### Background and Purpose
- Many device management platforms lack an integrated private software repository to distribute licensed applications and binary updates to client machines.
- Cloudflare D2 storage is inexpensive and even free for enterprises needing a limited amount of storage space (< 10GB).  See [https://developers.cloudflare.com/r2/pricing](https://developers.cloudflare.com/r2/pricing)

### High-level functionality
- Easily upload and manage software assets in D2 storage via Cloudflare Worker
- Authenticate clients and release binaries to authorized clients via Cloudflare Worker
- Sample PowerShell scripts to retrieve binaries and perform software installation
