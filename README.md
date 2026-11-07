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

## What it can't do yet

Next to the official Second Life viewer and Radegast, some things are missing:

- There's no picture of the world on screen, by design: what's around you comes as lists, words and sounds. A HUD that is one picture of buttons can only be read by the assistant.
- Web pages and video on objects and parcels don't play. Parcel music does.
- Running a group: sending notices, roles, and ejecting or banning members aren't there yet. Group chat, members, the notices archive and inviting people are.
- Some inventory housekeeping, such as emptying Lost and Found, searching by creator, and backing up to disk.
- Importing and exporting objects.
- In voice chat, a list of who's there to act on. You can mute one person or change how loud they are.
- Your password isn't saved, so you type it at each login.
- You type requests to the assistant; it doesn't hear speech.
- It runs on Windows 10 and 11, 64-bit, only. Builds aren't code-signed, so Windows warns the first time you run one.

## Content

Sojourn Access has no content of its own beyond General. What it reads out and describes is what's around you, so in Moderate and Adult regions that can include mature content, as any viewer would show it. The highest rating of region you go into is your account's and your own choice: type //maturity in the Say box, or find "Highest rating of region" in the World menu.

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

There's no formal support. To report a problem or ask for something, open an issue here: https://github.com/studio-quire/sojourn-access/issues (issues are public), or write to hello@studioquire.org.

Both are read, but there's no promised response time. Saying what you pressed, what you heard, and what you expected helps most. Your logs are in your data folder (below); they include chat, so read them before sharing any.

If Studio Quire has given you a token, you can send a session's log from inside Sojourn Access instead: Help, then Send a log to Studio Quire, or type //sendlog. You choose the session and can write a note on what happened. What it sends leaves out what other people said, as the Privacy section below says, and the Review button shows you exactly what will be sent first.

With a token, you can also write to us from inside Sojourn Access: Help, then Message the builders, or Control+Shift+B, opens a conversation tab. You're writing to Claude sessions (AI) building Sojourn Access at Studio Quire, not a person. Replies come when a session reads your message, sometimes a day later, and are read out like an instant message.

With the assistant switched on, with or without a token, you can also ask it to report a problem. It tells you what will be sent and waits for your key press; the report is this session's log, filtered in the same way, with your words.

## Privacy

This is Sojourn Access's privacy policy. It describes what the current build does, in effect from 2026-11-07, and changes when the code changes what's sent; its history is this repository's. Sojourn, the VR viewer, has its own.

Sojourn Access has no analytics or tracking, and sends no crash reports. Nothing reaches Studio Quire unless you send it.

**Second Life.** It connects where any Second Life viewer does: to Linden Lab's servers (your login, the regions you visit, their assets, search, the map and voice chat), and, if a parcel plays music and music is on, to that music stream's server, which sees your IP address as it would with any viewer. Your username and password go only to Linden Lab. Like every viewer, it sends the region the viewer statistics Linden Lab asks for: how long it has run, its memory, the regions visited, how many avatars are around, and your computer's operating system, processor and memory; not your network card's address or your disk's serial number, which the official viewer also sends.

**GitHub.** Once after logging in, and when you choose Help, then Newer build?, Sojourn Access asks GitHub for the newest test build's number, to tell you if yours is older. Nothing of yours goes with it; GitHub sees your IP address, as with any visit.

**Your computer.** Your settings, logs (the last ten sessions, including chat) and Second Life's cache stay on your computer, in a folder of your own: press Windows+R, type %LOCALAPPDATA%\Sojourn Access and press Enter. The password isn't saved. A token or key for the assistant is kept encrypted by Windows for your account, in %LOCALAPPDATA%\Sojourn.

**Studio Quire's relay** (relay.studioquire.org) gets only what you choose to send:

- A log, if you send one (Help, then Send a log to Studio Quire), which needs a token from Studio Quire. It goes with your note, for the people making Sojourn Access to read, and is kept for 30 days.
- A problem report, if you ask the assistant for one and confirm it: this session's log and your words. With a token it goes as yours; without one it goes anonymously, and your IP address isn't kept. Kept for 30 days.
- Messages to the builders (Help, then Message the builders), with a token: only what you type there, kept with our replies for 90 days. While you have a token, Sojourn Access asks the relay for replies about once a minute; Alt+0's row "Messages with the builders", in the General group, turns this off.

Before a log or report is sent, everything other people said or wrote is taken out of it (nearby chat, instant messages, group chat, their offers and notices, profiles and descriptions they wrote), and their names become "person 1", "person 2" and so on; your own name becomes "me". What stays is what Sojourn Access did and read out to you, your own chat, what objects said, the assistant's replies, the names of places and things, errors and timings. Keys, tokens, your Windows account's folder name and your IP address are masked too. Send a log's Review button shows you exactly what will be sent.

**The assistant** is off unless you choose it in Alt+0. When you use it, each request goes to the provider you chose, under that provider's terms and privacy policy:

- with your own Anthropic key, to Anthropic, the maker of Claude;
- with your own OpenRouter key, to OpenRouter and the model's provider it routes to. "No data collection" is on by default, so OpenRouter uses only providers that say they don't keep or train on what's sent. Choosing OpenRouter also fetches its public list of models, with no key;
- with a token from Studio Quire, to Anthropic through Studio Quire's relay, which passes requests on and keeps nothing of them, only how much was used.

What's sent: your request, what it looks up to answer it (the names of people and things around you, recent chat when your request is about it, pictures of the view), and its notes on your preferences. Its tools may search the web. Its notes are kept in your data folder; it keeps no transcripts. In incognito (Control+Shift+I), nothing from that time is kept, and by default the assistant sees only a general picture.

**What we hold, and how.** Logs, reports and messages are stored by the relay on Cloudflare, readable only with Studio Quire's own secret, never shared or sold, and deleted automatically after 30 days (logs and reports) or 90 days (messages). Cloudflare, which runs the relay, sees IP addresses as for any website it serves. Linden Lab may ask a viewer's makers to update or delete data received from Second Life; the only such data we hold is in what people chose to send, with other people's words already left out, and we delete it on request.

**Questions, or to have something deleted:** write to hello@studioquire.org, or, with a token, Message the builders. Issues on this repository are public, so a request to delete something is better sent by email.

## Removing it

Quit it, delete its folder, and delete the Sojourn Access folder in your AppData Local folder. If you put in a token or key for the assistant, delete the Sojourn folder there too. That's everything.

## Source code and licence

Sojourn Access is open source, under the GNU Lesser General Public License, version 2.1. It shares its code with Sojourn, a VR viewer, in one repository: https://github.com/studio-quire/sojourn

Each release's notes name the exact commit of that repository it was built from. The licences of the parts it includes are in the Licences folder of each build.

## Who makes it

Sojourn Access is made by Claude models (Anthropic's AI) at Studio Quire, who also direct its design, and Shoalstone, the person behind Studio Quire, decided it should be made. Blind residents trying it and saying what works is what shapes it most.

Second Life and Linden Lab are trademarks of Linden Research, Inc. Sojourn Access is not affiliated with or endorsed by Linden Lab.
