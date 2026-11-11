# Keep it Split releases

Signed and notarized builds of [Keep it Split](https://kis.appsurd.lol) — a split view for the Mac
where each window keeps the room it needs.

This repository holds release files only: the disk images, their SHA-256 checksums and the
release notes. The source code is not public. The website is <https://kis.appsurd.lol>.

- **Download:** <https://kis.appsurd.lol/download> always points to the newest release.
- **Requirements:** macOS 26 or later, Apple Silicon or Intel.
- **Updates:** Keep it Split checks <https://kis.appsurd.lol/updates/appcast.xml> and asks before
  installing anything.

Releases are immutable: a fixed build gets a new build number rather than replacing files.
Every file is signed with Developer ID (team `5QVM5Y9RYP`) and notarized by Apple. To check a
download:

```bash
shasum -a 256 Keep-it-Split-*.dmg   # compare with SHA256SUMS.txt in the same release
spctl -a -vv -t open --context context:primary-signature Keep-it-Split-*.dmg
```
