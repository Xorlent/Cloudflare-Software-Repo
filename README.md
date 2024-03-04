# Cloudflare-Software-Repo
Cloudflare D2 storage-based enterprise software distribution

## Work in progress...

### Background and Purpose
- Many device management platforms lack an integrated private software repository to distribute licensed applications and binary updates to client machines.
- Cloudflare D2 storage is inexpensive and even free for enterprises needing a limited amount of storage space (< 10GB).  See [https://developers.cloudflare.com/r2/pricing](https://developers.cloudflare.com/r2/pricing)

### High-level functionality
- Easily upload and manage software assets in D2 storage via Cloudflare Worker
  - Secure access via ............
  - Prompt to delete expired D2 assets
  - Upload asset: Friendly name, ID (auto-gen), expiration (default 1yr), tags/groups
  - Search and select assets: view logs, edit, expire (delete)
    - AssetKV: ID, FriendlyName (expiration)
  - Search and select tags/groups: edit name, edit enforced security, view linked assets
    - TagsKV: Name, security
    - AssetTagKV: Name, {AssetIDs}
- Authenticate and release binaries to authorized clients via Cloudflare Worker
  - TLS 1.2 connection security
  - Secure access via IP allowlisting, shared secret, hostname validation, or any combination of these three
  - Access logging and rate limiting functionality
- Sample PowerShell scripts to retrieve binary and perform software installation

