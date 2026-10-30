# Sojourn Access

Second Life with a screen reader and the keyboard, on Windows. Early test builds.

## Get it

1. Download the newest build: https://github.com/studio-quire/sojourn-access/releases/latest (under Assets, the file ending in win-x64.zip).
2. Unzip it, open the folder and press Enter on SojournAccess.exe. Nothing is installed.
3. If Windows says "Windows protected your PC": More info, then Run anyway. NVDA may read that button as just "R".

Then log in with your Second Life account. F1 shows the keys.

This software is not provided or supported by Linden Lab, the makers of Second Life.

## What it is

Its window is made of standard Windows controls. When NVDA is running, what arrives (chat, instant messages, notices) is spoken through NVDA by itself. Other screen readers get it through Windows' UI Automation. You choose what is read out, and nothing takes your focus while you type.

Some of what it does:

- Its double-slash commands follow Radegast's, so routes and commands written for Radegast run here too.
- People and things around you are given by clock-face direction and distance.
- Walk mode moves you with the arrow keys, with a sound for each step, footsteps by surface, and warnings before you bump into something.
- Every part of an object, and each face of a part, can be found and touched by keys.
- Script menus, offers and questions wait in Notices and are answered by number keys.

Sojourn Access can also work with an AI assistant that describes places, people and pictures and does things for you when you ask. Test builds don't include the assistant yet. Everything else works without it.

These are test builds: some things are missing or wrong. Please don't rely on Sojourn Access for anything that matters yet.

## More on starting it

To skip Windows' warning: before unzipping, press Alt+Enter on the zip, check Unblock near the bottom of the General tab, press Enter, then unzip.

It runs from the folder you unzip it into. It doesn't need .NET or anything else installed, and it never updates itself. Older builds are on the Releases page: https://github.com/studio-quire/sojourn-access/releases

When you first log in, Windows Firewall may ask whether Sojourn Access may use networks. It only makes outgoing connections, so Allow is fine, and it should work whichever you choose.

The login window has Grid (Second Life is chosen), Username, Password, Show password, Start at, and the Log in button. Your password isn't saved. If Second Life asks you to agree to its Terms of Service, or for a code from your authenticator, a small window asks you.

When you've arrived, the cursor is in the Say box, as in Radegast. The folder also has a README.txt with all of this.

## The first keys

- F1: the keys, in a window to read line by line. Escape closes it.
- Type //help in the Say box and press Enter: the commands.
- Enter says what you typed, Shift+Enter whispers, Control+Enter shouts.
- Alt+1 to Alt+9, and Alt+0: the areas (nearby chat, conversations, people, inventory, search, places, objects, notices, the assistant, settings).
- Control+Tab: the next conversation.
- Control+N: the newest notice. 1 to 9, 0, minus and equals press its buttons.
- Control+Shift+H: teleport home.
- F3: walk mode. Escape leaves it.
- F4, held: talk in voice chat.
- F6: mute what's read out, and again to turn it back on.
- Control+R: repeat the last thing read out.
- Alt+F4: log out and quit.

## Help and feedback

There's no formal support. To report a problem or ask for something, open an issue here: https://github.com/studio-quire/sojourn-access/issues

Issues are read, but there's no promised response time. Saying what you pressed, what you heard, and what you expected helps most. Your logs are in your data folder (below); they include chat, so read them before sharing any.

## Privacy

Sojourn Access has no analytics, tracking or crash reports, and sends nothing to its makers.

It connects only where any Second Life viewer does: to Linden Lab's servers (your login, the regions you visit, their assets, search, the map and voice chat), and, if a parcel plays music and music is on, to that music stream's server, which sees your IP address as it would with any viewer. Your username and password go only to Linden Lab.

Your settings, logs (the last ten sessions, including chat) and Second Life's cache stay on your computer, in a folder of your own: press Windows+R, type %LOCALAPPDATA%\Sojourn Access and press Enter.

A build that includes the assistant will send what it needs for each request to Anthropic, the maker of Claude, under your own Claude account: your request, what it looks up to answer it (such as names around you, recent chat when you ask about it, or pictures of the scene), and its notes on your preferences. Test builds today don't include it.

## Removing it

Quit it, delete its folder, and delete the Sojourn Access folder in your AppData Local folder. That's everything.

## Source code and licence

Sojourn Access is open source, under the GNU Lesser General Public License, version 2.1. It shares its code with Sojourn, a VR viewer, in one repository: https://github.com/studio-quire/sojourn

Each release's notes name the exact commit of that repository it was built from. The licences of the parts it includes are in the Licences folder of each build.

## Who makes it

Sojourn Access is made by Claude models (Anthropic's AI) at Studio Quire, who also direct its design, and Shoalstone, the person behind Studio Quire, decided it should be made. Blind residents trying it and saying what works is what shapes it most.

Second Life and Linden Lab are trademarks of Linden Research, Inc. Sojourn Access is not affiliated with or endorsed by Linden Lab.
