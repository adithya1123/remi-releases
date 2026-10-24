# remi

`remi` installs Remi, an assistant for a household with a long memory, on your own computer or server with Docker,
and looks after it: updates, backups and restores, and what to fix when something's wrong.

## What you need
- **A Mac** (Apple silicon or Intel) **or a Linux server** (amd64 or arm64), always on.
- **Docker**: Docker Desktop on a Mac; Docker Engine with Compose 2.24 or later on Linux, usable without `sudo`.
- **Room**: 4 GB of memory for Docker (8 GB on the machine), and 15 GB of disk free.
- **Access to Remi's images**, which are private: whoever gave you Remi gives you access, with a GitHub account or a
  token for this install.
- **Tailscale**, to reach Remi from phones and other computers. `remi setup` sets it up; without it, Remi is for the
  computer it runs on.

## Install
```bash
curl -fsSL https://github.com/adithya1123/remi-releases/releases/latest/download/install.sh | sh
remi setup
```
`remi setup` checks the machine, asks what it needs, shows everything before writing anything, and starts Remi.
After that, `remi status`, `remi update`, `remi backup` and `remi doctor` look after it.

## What's here
Releases only, no source. Each release has `remi` for macOS and Linux (amd64 and arm64) with their `SHA256SUMS`,
`install.sh`, the release's `compose.yaml`, and its manifest, `release.json`, signed (`release.json.minisig`):
`remi` takes an update only when it's signed with Remi's release key. A published release can't be changed.

## Licence
Remi isn't open source. Its licence (`LICENSE` in each archive; `remi licence` shows it) lets the people given access
to its images install and run Remi for themselves and their household, on computers they control. It doesn't let you
pass Remi or your access on, run it for anyone outside your household, change it, or take it apart. A copy of `remi`,
which anyone may download, gives no right to use Remi. What you put into Remi stays yours. The open source software
it includes keeps its own licences (`NOTICE` in each archive).
