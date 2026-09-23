# Install Tikinson

[Русский](installation.ru.md)

Verified on Windows with Codex 26.915.4065.0 supporting custom v2 pets. The archive includes neither Codex nor executable installers.

1. Download `downloads/tikinson-v1.0.0.zip` from this repository and extract it.
2. If Tikinson is already installed, back up its folder.
3. Open `%USERPROFILE%\.codex\pets` in File Explorer. Create `pets` if missing. If you use a custom `CODEX_HOME`, use its `pets` subfolder.
4. Copy the archive's `tikinson` folder there. The resulting paths must be `.codex/pets/tikinson/pet.json` and `.codex/pets/tikinson/spritesheet.webp`, without an extra nested folder.
5. Restart Codex and select Tikinson in the pet menu. Retain the license and attribution.

To uninstall, select another pet and remove only the `tikinson` folder. To update, back up and replace its contents.

Other operating systems have not been tested. Codex triggers greetings and other emotions; a greeting is not guaranteed every time the pet appears. If the character is missing, check v2 support, paths and file integrity. The archive includes the atlas checksum; the external `SHA256SUMS` also covers the ZIP. In PowerShell: `Get-FileHash -Algorithm SHA256 <file-path>`.
