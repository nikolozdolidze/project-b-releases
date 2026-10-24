# Project B

A tiling, keyboard-first browser for Windows, built on Firefox.

This repository holds Project B's releases: the installer, its checksums and the release notes. **[Download the latest release](https://github.com/nikolozdolidze/project-b-releases/releases/latest).**

## Installing

Download `projectb-<firefox version>.en-US.win64.installer.exe` from the latest release and run it. It installs as **Project B** in `C:\Program Files\Project B`, with a Start menu entry, a desktop shortcut and an uninstaller.

The installer isn't code-signed yet, so Windows SmartScreen says it "protected your PC". Choose **More info**, then **Run anyway**.

## Checking the download

Each release has a `SHA256SUMS` file. In a terminal, in the folder you downloaded to:

```
certutil -hashfile projectb-158.0.1.en-US.win64.installer.exe SHA256
```

The result should match the installer's line in `SHA256SUMS`.

## Updates

Project B looks for a newer release here once a day (Settings > About > Check for updates, to look now). It downloads the new installer, checks it against that release's `SHA256SUMS`, and installs it when you choose **Install and restart**.

## Licenses

Project B's own code is under the Mozilla Public License 2.0. It's built on [Firefox](https://www.firefox.com/) (Mozilla Public License 2.0), whose source is at [github.com/mozilla-firefox/firefox](https://github.com/mozilla-firefox/firefox). It includes the Tor Project's `tor.exe`, unchanged (GNU GPL 3.0; its source is at [dist.torproject.org](https://dist.torproject.org/)). The installer's `tor\docs` folder holds Tor's licenses and where its source is.
