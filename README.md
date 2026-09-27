# Viremail for Mac, Windows and Linux

Viremail is private email, Vire chat and calls, calendar, tasks, notes, contacts and Drive in one place.
The desktop app gives you all of it in its own window, with alerts that reach you when the window is closed.

**Download it from [viremail.com/desktop](https://viremail.com/desktop).** That page picks the right file for your computer and always has the newest version. This repository only holds the installers that page links to.

## Opening it the first time

This first version is not signed yet, so your computer asks before it opens Viremail the first time. Here is what to do.

### Mac

1. Open the `.dmg` file you downloaded and drag Viremail into Applications.
2. Open Viremail from Applications. macOS says it could not check the app. Choose **Done** (not Move to Bin).
3. Open **System Settings**, then **Privacy & Security**. Scroll down to the Security section, where it says Viremail was blocked, and choose **Open Anyway**. If the button is not there, open Viremail from Applications once more, then look again.
4. Choose **Open Anyway** once more and enter your Mac password or use Touch ID. From then on Viremail opens like any other app.

On macOS 15 and later, Control-clicking the app and choosing Open no longer works for apps that are not signed yet, so use System Settings as above.

Which file? Open the Apple menu and choose About This Mac. If it says Chip, take the Apple silicon file (`mac-arm64`). If it says Processor, take the Intel file (`mac-x64`).

**New versions on a Mac.** Until the app is signed, it can't update itself on a Mac. Get new versions from [viremail.com/desktop](https://viremail.com/desktop) and drag Viremail into Applications again, replacing the old copy. If macOS stops the new version, use Open Anyway as above. It may also ask whether Viremail can use **Viremail Safe Storage** in your keychain. Choose **Always Allow**. If you choose Deny, you will need to sign in again.

### Windows

1. If your browser says the file isn't commonly downloaded, choose **Keep**. In Edge, Keep is in the menu next to the download, and you may then need **Show more** and **Keep anyway**.
2. Open the installer. If you see **Windows protected your PC**, choose **More info**, then **Run anyway**.
3. Viremail installs for you alone, with no administrator password, and opens by itself. It is in the Start menu from now on.

If Windows says Smart App Control blocked it, there is no Run anyway. For now, use Viremail in your browser at [viremail.com](https://viremail.com).

On Windows the app updates itself and asks you to restart when a new version is ready.

### Linux

On **Ubuntu or Debian**, use the `.deb` (on Ubuntu 24.04 and later, always use it). Open it with App Center, or in a terminal in your Downloads folder run:

```sh
sudo apt install ./viremail_1.0.0_amd64.deb
```

Use the name of the file you downloaded (`arm64` instead of `amd64` on an Arm computer).

On **other distributions**, you can use the AppImage. Make it executable, then run it:

```sh
chmod +x Viremail-1.0.0-linux-x86_64.AppImage
./Viremail-1.0.0-linux-x86_64.AppImage
```

On Ubuntu 24.04 and later the AppImage may not start, because of the system's AppArmor rules for unprivileged sandboxes. The `.deb` sets things up so Viremail runs as it should.

## Checking your download

Every download has a SHA-256 checksum, published with the release in the `SHA256SUMS` file (and on [viremail.com/desktop](https://viremail.com/desktop)). Work out the checksum of the file you downloaded and make sure it matches the line for that file.

Mac, in Terminal:

```sh
shasum -a 256 ~/Downloads/Viremail-1.0.0-mac-arm64.dmg
```

Windows, in PowerShell:

```powershell
Get-FileHash -Algorithm SHA256 $HOME\Downloads\Viremail-Setup-1.0.0-win-x64.exe
```

Linux, in a terminal:

```sh
sha256sum ~/Downloads/viremail_1.0.0_amd64.deb
```

Or, with `SHA256SUMS` in the same folder as your download, check them all at once:

```sh
sha256sum --check --ignore-missing SHA256SUMS
```

If the checksum does not match, delete the file and download it again from [viremail.com/desktop](https://viremail.com/desktop).

## Source code

The source code is not in this repository. It only holds the installers, their checksums and the files the app reads to find updates.

## Help

The [desktop app guide](https://viremail.com/help/desktop-app) covers settings, updates and removing the app. For anything else, email [support@viremail.com](mailto:support@viremail.com).

## Who makes Viremail

Svayam Incarnation Limited, a company registered in England and Wales, company number 15228262.
Registered office: 124 City Road, London EC1V 2NX, United Kingdom.

Mac and macOS are trademarks of Apple Inc. Windows is a trademark of the Microsoft group of companies. Linux is the registered trademark of Linus Torvalds.
