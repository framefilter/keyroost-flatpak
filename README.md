# keyroost-flatpak

Self-hosted **Flatpak OSTree repo** for
[keyroost](https://github.com/framefilter/keyroost) — the independent,
vendor-neutral hardware-security-key manager.

Hosts the Flatpak auto-update remote on its own GitHub Pages. Its contents — the
OSTree tree plus `keyroost.flatpakrepo` and `keyroost-icon.svg` — are published
by the `linux-bundles.yml` workflow in the main repo on each release tag.

```bash
flatpak remote-add --if-not-exists keyroost \
    https://framefilter.github.io/keyroost-flatpak/keyroost.flatpakrepo
flatpak install keyroost io.github.framefilter.keyroost
```
