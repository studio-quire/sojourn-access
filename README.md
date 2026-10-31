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
- A menu bar (Alt or F10) lists what there is to do, each item with its key.

It also has an AI assistant that describes places, people and pictures, and does things for you when you ask. It's off unless you choose it in Alt+0 (settings), with a token from Studio Quire if the studio has given you one, or your own Anthropic or OpenRouter key. Everything else works without it.

These are test builds: some things are missing or wrong. Please don't rely on Sojourn Access for anything that matters yet.

## More on starting it

To skip Windows' warning: before unzipping, press Alt+Enter on the zip, check Unblock near the bottom of the General tab, press Enter, then unzip.

It runs from the folder you unzip it into. It doesn't need .NET or anything else installed, and it never updates itself. Older builds are on the Releases page: https://github.com/studio-quire/sojourn-access/releases

The first time you log in or teleport, Windows Firewall may ask whether Sojourn Access may use networks. It only makes outgoing connections, so Allow is fine, and it should work whichever you choose.

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

If Studio Quire has given you a token, you can send a session's log from inside Sojourn Access instead: Help, then Send a log to Studio Quire, or type //sendlog. You choose the session and can write a note on what happened. What it sends leaves out what other people said, as the Privacy section below says, and the Review button shows you exactly what will be sent first.

## Privacy

Sojourn Access has no analytics, tracking or crash reports.

Without the assistant, it connects only where any Second Life viewer does: to Linden Lab's servers (your login, the regions you visit, their assets, search, the map and voice chat), and, if a parcel plays music and music is on, to that music stream's server, which sees your IP address as it would with any viewer. Your username and password go only to Linden Lab.

Your settings, logs (the last ten sessions, including chat) and Second Life's cache stay on your computer, in a folder of your own: press Windows+R, type %LOCALAPPDATA%\Sojourn Access and press Enter.

A log leaves your computer only if you send one (Help, then Send a log to Studio Quire), which needs a token from Studio Quire. It goes to Studio Quire's relay with your note, for the people making Sojourn Access to read, and is deleted after 30 days. Before it's sent, everything other people said or wrote is taken out of it (nearby chat, instant messages, group chat, their offers and notices, profiles and descriptions they wrote), and their names become "person 1", "person 2" and so on; your own name becomes "me". What stays is what Sojourn Access did and read out to you, your own chat, what objects said, the assistant's replies, the names of places and things, errors and timings. Keys, tokens, your Windows account's folder name and your IP address are masked too.

The assistant is off unless you choose it. When you use it, each request goes to Anthropic, the maker of Claude: your request, what it looks up to answer it (the names of people and things around you, recent chat when it's needed, pictures of the view), and its notes on your preferences. With a token from Studio Quire, requests go through Studio Quire's relay, which passes them on and keeps nothing of them, only how much was used. With your own key, they go to Anthropic or OpenRouter directly.

## Removing it

Quit it, delete its folder, and delete the Sojourn Access folder in your AppData Local folder. If you put in a token or key for the assistant, delete the Sojourn folder there too. That's everything.

## Source code and licence

Sojourn Access is open source, under the GNU Lesser General Public License, version 2.1. It shares its code with Sojourn, a VR viewer, in one repository: https://github.com/studio-quire/sojourn

Each release's notes name the exact commit of that repository it was built from. The licences of the parts it includes are in the Licences folder of each build.

## Who makes it

Sojourn Access is made by Claude models (Anthropic's AI) at Studio Quire, who also direct its design, and Shoalstone, the person behind Studio Quire, decided it should be made. Blind residents trying it and saying what works is what shapes it most.

Second Life and Linden Lab are trademarks of Linden Research, Inc. Sojourn Access is not affiliated with or endorsed by Linden Lab.
