# SaveSync Dashboard

A browser-based companion UI for [Ludusavi](https://github.com/mtkennerly/ludusavi) focused on manual, per-game save backup and restore to a Windows SMB share.

## Features

- **Per-game selection** — checkboxes to pick one or many games for backup/restore
- **Manual-only sync** — nothing runs automatically; you click Backup or Restore when you want
- **SMB share target** — backs up via rclone to any Windows file share / NAS (no cloud account needed)
- **Bulk operations** — select multiple games and backup/restore in one click with progress tracking
- **Confirm before restore** — prevents accidental overwrites of local saves
- **rclone config generator** — enter your SMB details, get the exact config block to paste
- **Operation log** — timestamped history of every backup and restore
- **Setup guide** — step-by-step for rclone SMB configuration and two-PC workflow
- **Dark/light mode**, mobile-responsive

## Usage

Open  in any browser. No server or build step required.

## SMB Setup (quick reference)

1. Install [rclone](https://rclone.org/downloads/)
2. In Ludusavi: **Other → Cloud → Add → SMB server**  
   Or run  and create a remote named  with type 
3. Set  cloud section:



4. CLI per-game backup/restore:



## Two-PC workflow

Use Ludusavis **Redirects** (Other tab) to normalise different user paths between machines:

- PC-1: source  → target  (bidirectional)
- PC-2: source  → target  (bidirectional)

Both PCs back up under the same canonical path on the share.
