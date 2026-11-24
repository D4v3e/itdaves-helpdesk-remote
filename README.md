# IT Dave's Helpdesk Remote Support

This is a modified Windows client of [RustDesk](https://github.com/rustdesk/rustdesk) **1.5.3** (commit `95cca3f661f635b3cc85c04935fe8d96d8f432ef`), branded for IT Dave's Helpdesk and hard-wired to the self-hosted server `remote.itdaveshelpdesk.co.uk`.

It is **not** affiliated with, sponsored by, or endorsed by the RustDesk project or Purslane Tech Pte. Ltd. The name and logo of RustDesk are used only to identify the upstream software.

## Licence

RustDesk is licensed under the [GNU Affero General Public License v3.0](LICENCE). This modified version is released under the same licence. The original copyright of Purslane Tech Pte. Ltd. is retained. Modifications are Copyright © 2026 IT Dave's Helpdesk.

The corresponding source for this modified client is this repository. See [NOTICE](NOTICE).

## What was changed

- Product name **IT Dave's Helpdesk**, window title **IT Dave's Helpdesk Remote Support**.
- IT Dave's Helpdesk icons and colours in place of the RustDesk mark in the Windows UI.
- The ID/rendezvous server and public key are compiled in, so the executable connects to `remote.itdaveshelpdesk.co.uk` regardless of its filename.
- Official RustDesk auto-update and “powered by” UI are disabled (`is_custom_client()` is true because the app name is no longer `RustDesk`).
- The Windows executable is `ITDavesHelpdesk.exe`.

No RustDesk Server Pro code is included. The server this client talks to is the official open-source `hbbs`/`hbbr` 1.1.16.

## Build (Windows x86_64)

The GitHub Actions workflow `.github/workflows/windows-x64-client.yml` builds the unsigned Windows EXE (portable self-extractor) and MSI on a free `windows-2022` runner. Trigger it with `workflow_dispatch` or by pushing a tag such as `itdaves-1.5.3`.

Do not enable the upstream nightly, full Flutter CI, or multi-platform tag workflows in this repository; they would build every platform and the Windows ARM job needs `windows-11-arm`.

## Trademark

Do not use the RustDesk name or logo as the name of this product. Attribution of the upstream project, required by AGPL, belongs in the About box, NOTICE, and this README.
