# How releases work

This repository holds no code. Sojourn Access's source is in https://github.com/studio-quire/sojourn, which it shares with Sojourn.

Each release here is one test build:

1. The source is published to studio-quire/sojourn first, as a commit there.
2. The build is made from that same source by `python tools/access.py package`, which makes a self-contained Windows zip (no .NET needed), versioned 0.1.0.N, with a README.txt for screen-reader users and a Licences folder holding the notices of everything it includes.
3. The release here is tagged with that version, carries the zip as its asset, and its notes name the exact studio-quire/sojourn commit it was built from, so the source of every build is available under the GNU LGPL 2.1.

Release notes are short: the download first (the zip under Assets, unzip, run SojournAccess.exe), then in a few plain words what changed, then the source commit and the disclaimer: this software is not provided or supported by Linden Lab, the makers of Second Life.
