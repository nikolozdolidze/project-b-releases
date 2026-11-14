# Mosaic Browser

A browser for Windows, built on Firefox for heavy multitasking and for security. It was called Project B until 0.4.5.

This repository holds Mosaic Browser's releases: the installer, its checksums and the release notes. **[Download the latest release](https://github.com/nikolozdolidze/mosaic-browser-releases/releases/latest).**

- [What it does](#what-it-does)
  - [Many pages at once](#many-pages-at-once)
  - [Privacy and security](#privacy-and-security)
  - [Passwords, addresses and cards](#passwords-addresses-and-cards)
  - [Everyday browsing](#everyday-browsing)
  - [Settings](#settings)
- [Keyboard shortcuts](#keyboard-shortcuts)
- [Installing](#installing)
- [Uninstalling](#uninstalling)
- [Checking the download](#checking-the-download)
- [Updates](#updates)
- [Known limits](#known-limits)
- [Licenses](#licenses)

## What it does

### Many pages at once

- **Splits.** Any tab can become a split: panes beside and above one another, as many as you like, each with its own tabs. Split the pane you're in to the right or downwards, drag a tab onto a page to split it (a preview shows the half it will take: left, right, top or bottom, whichever edge you let go nearest), or let **snap layouts** lay a split out in one go and fill its spaces from your other tabs. Drag the borders to resize panes, or make them all equal. New panes slide in from the side they're split off to. Panes keep at least 280×200 px where there's room: a split that would make one smaller says so instead.
- **Each pane has its own bar**: its tabs and its own address bar. The bar slides in when you point at the pane's top edge, or stays put once pinned. It also shows itself for a couple of seconds when a link opens in a new tab in the pane, so you see the tab arrive. The pane under the pointer takes the focus, and you can move between panes with Ctrl+Alt and the arrows. In a pane with many tabs, they can scroll instead of shrinking. In a narrow pane, the address bar keeps its room and the other buttons move into the pane's menu, where they work as they did.
- **The tab strip** holds single tabs and splits side by side. Point at a tab for a picture of its page and how much memory it's using; its page is drawn ahead meanwhile, so going to it shows it at once. Drag tabs to reorder them, into a split, into another window, or out into a new window. Pin a tab to keep it at the start. Ctrl+1 to Ctrl+8 go to the strip's first eight, Ctrl+9 to its last. With more tabs than fit, the strip scrolls sideways (turn the mouse wheel over it), fading out at an end with more tabs beyond.
- **Tab groups.** Right-click a tab and choose **Add to new group** to keep tabs together under a label in the strip: one of nine colours, with a name or just the colour, its tabs tinted with it. Click the label to fold the group's tabs away behind it (it then shows how many) and again to bring them back. Add tabs from their menu, or drag them in among the group's tabs; drag them out to take them out, or drag the label to move the whole group. A link opened from a grouped tab joins its group. The label's menu renames and recolours it, opens a new tab in it, folds it, ungroups it or closes it. Groups come back when the browser restarts, and with saved sessions.
- **Workspaces.** Named sets of tabs in one window, the strip showing one set at a time: a "Work" and a "Home", say. Switch between them from the pill at the start of the strip, move a tab to another from its right-click menu, and rename or delete one. They come back as they were when the browser restarts.
- **Profiles.** A round button beside the window's buttons shows your profile's avatar (its name's first letter on a colour, or a picture) and opens its menu: your other profiles, **Add profile**, your passwords and a private window. Each profile is a browser of its own, in windows of its own, with its own tabs, sign-ins and cookies, passwords, history, bookmarks, extensions and settings: one Google account in "Personal", another in "Work". Rename one, change its colour or picture, or delete it from **Edit profile**. With two or more, every profile but your first has a taskbar button of its own, its windows on it and its avatar on the icon, and a Start menu shortcut ("Mosaic Browser (Work)", say) that opens it; pin a profile's button and it always opens that profile. The usual Mosaic Browser button (and its Start menu entry) opens the profile you used last, and its jump list's tasks (a new tab or window, a private tab or window, a private tab or window with Tor) open your first profile. A link clicked in another app asks which of the open profiles should open it.
- **Recently closed and saved sessions.** Ctrl+Shift+T reopens the last closed tab, or a whole closed window with its splits. The History page lists what you closed lately, and saves a window's tabs and splits as a session to open again later, in a new window or the one you're in (only the tabs in front load until you go to the others).
- **Saved splits.** Save a split to the new tab page and open it again later in one go. It remembers which of its tabs were sandboxed or private, and opens those in fresh sandboxes, signed out.
- **Resting tabs.** Tabs you haven't looked at for a while hibernate (frozen, their memory handed back to Windows; they wake instantly, exactly as they were), and later sleep (unloaded, their history kept). You choose the timings, or rest a tab yourself from its menu, the one you're on too: it stays asleep, blurred, with a **Wake up** button, until you wake it. Turn on **Keep resting tabs asleep when you go to them** (Settings > Tabs and panes) and any resting tab you go to stays that way too. Pinned tabs, tabs playing sound, tabs in a call or sharing your screen, camera or microphone, picture-in-picture and pages with unsaved work never rest.
- **Every tab has its own volume.** A tab playing sound shows a speaker: click it to mute, turn the mouse wheel over it to raise or lower the volume, or right-click the tab for a volume slider. A video can play quietly while a call stays loud.
- **Picture-in-picture.** Right-click a video and choose **Picture-in-picture** to watch it in a small window of its own, on top of everything else. A tab with a video (long enough, with sound) offers it in its right-click menu too, so you can pop the video out without going to the tab: it picks the video that's playing, or else the longest. While it's out, the same items say **Exit picture-in-picture**. Ctrl+Shift+] pops out the video of the tab in front. Its window can be made any size and shape (the video stays whole and centred, never stretched or cut), and its controls are in Mosaic's look, its corners rounded a little (on Windows 11). Once it's bigger than about 475 by 325, it has a speed button too (0.25x to 2x).
- **Video sandboxing.** A video going full screen fills only its tab's pane, not the whole screen, so the rest of a split stays in view. Turn it on for a tab from its right-click menu (in a split, from its pane's bar), or for every tab in a split in Settings > Tabs and panes. Esc or the player's own button leaves full screen as usual.
- **The command palette** (Ctrl+K) has every command the browser has, and your history: type what you're after. It also opens from the menu button, as a regular browser menu with search at the top.
- **The sidebar** (Ctrl+B), on the left or right of the window, with panels for bookmarks, history, downloads, your tabs and notes. Pin it open beside the page, or let it slide away when the pointer leaves.
  - **Sites pinned to the sidebar** live apart from your tabs: a chat or music site always at hand. Each can have sign-ins of its own, ask for the phone layout, and sleep when unused. Pin one from a page's or a link's right-click menu, or move a tab there.
  - **Notes**: a general note, and a note for each site, shown beside its page.
  - **Custom panels**: your own pages in the sidebar, written in HTML, CSS and JavaScript in Settings > Custom panels (start from a blank page or a scratchpad). Each runs like a tab, starting when you open it and sleeping when unused, or keeps running while the browser is open, so its timers and reminders go on while it's closed. What a panel saves is its own: no site, file or other panel can read it, and it stays through restarts and clearing browsing data until you delete the panel. A number in brackets at the start of its title shows on its icon, and it can show notifications. Its code is written in a code editor (highlighting, line numbers, find and replace), and a panel can be exported to a `.mosaicpanel` file and imported. A panel can open tabs, and one you let read the page you're on sees its address, title, text and selection; none sees private or Tor tabs. One that keeps running is one page for all your windows.
- **Right-click almost anything.** A tab: pin it, put it in a tab group (or take it out), rest it, its volume, pop its video out into picture-in-picture, video sandboxing, sandbox it or make it private, open a sandboxed or private copy beside it, move it to another workspace, save its split, close it or the tabs around it. A tab group's label: rename and recolour it, a new tab in it, fold it, ungroup it or close it. Anything on a page: block it (Block element…). The + button: a private tab, one with Tor, or a sandbox. The strip: new tabs and windows. A link, a picture or a video: open it in a new tab, a new sandbox, a private tab or one with Tor, or in a split on the side you choose (right, left, top or bottom); a link also in a new window, or pinned to the sidebar. A bookmark opens the same ways, and a site in the sidebar in a split. A video: play, mute, loop, its controls, picture-in-picture. The address bar: paste and go in one. The taskbar button: a new tab or window, a private tab or window, or a private tab or window with Tor.

### Privacy and security

- **Sandboxes.** A sandboxed tab has sign-ins of its own, so you can use two accounts on one site side by side. Everything it opens stays in its sandbox, and each sandbox has a number and a colour on its tabs, its pane's outline and the address bar. While it lasts, a sandbox is as private as a private window: its pages aren't kept in history, what you type into its forms isn't remembered, its downloads aren't added to your download history, it isn't written into the saved session, and nothing it loads is cached on disk. What its sites keep themselves (cookies and site data; a private tab's cookies stay in memory) is on disk while it's open. When its last tab closes, everything it kept (cookies, storage, permissions) is wiped, and after a crash that happens before any page loads.
- **Private tabs** are sandboxes that start on a new tab page, so a private tab can sit right beside a normal one. A private tab (and one with Tor) fills nothing in and offers to save nothing: no saved sign-ins, addresses or cards, and nothing typed there kept. Its downloads are its own, as a private window's are: only its tabs' downloads button, list and downloads page show them, and your other tabs' never do. They're never kept to start again later: one still coming when the browser quits is stopped, its partial file deleted.
- **Private tabs with Tor.** Every request from such a tab goes through Tor, DNS included, with nothing ever falling back to a direct connection. WebRTC and speech recognition are removed from its pages, onion sites work, and typing an onion address in a normal tab opens it in a new Tor tab. You can ask for a new Tor circuit for a tab. Tor ships with the browser and starts when you first need it, locked down: it can't read your files or reach the browser's memory, and writes only its own folder.
- **Private, Tor and sandbox windows**: every new tab in a private window shares one private sandbox, in a private window with Tor one that goes through Tor, and every new tab in a sandbox window gets its own. Unlike Firefox's private windows, tabs can move in and out of them.
- **Shields** block ads and trackers on every site, using filter lists you choose from a catalogue (see below) and uBlock Origin's own lists, their procedural filters (hiding an element by its text, its styles or what it's inside) and pop-up filters included. They also hide ad leftovers on pages, hide "we use cookies" notices (or turn them down where that's what makes them go), strip tracking parameters from addresses, skip redirect trackers, and stop pages a list says not to open at all (badware), with a warning you can go past. Turn them off for a single site from the site menu.
  - **Filter lists, all in one place** (Settings > Ad blocking): 65 lists in eight groups (Ad blocking, Privacy, Social widgets, Annoyances, Security, Other, Language-specific, and your own), from AdGuard, EasyList, Fanboy, Dandelion Sprout, uBlock Origin and others. Each group can be switched as a whole and shows how many of its lists are on; each list shows what it does, its version, when it was updated, its homepage and tags, with its own switch. Search finds any list by name. AdGuard's lists come as AdGuard's own builds for uBlock-style blockers, so their page-fixing scripts work.
  - **Your security level** (top of Settings > Ad blocking): Maximum, Balanced, Minimum or None, each with its own set of lists and tracking-protection options (it asks first, and says what it changes). uBlock Origin's own lists (filters, privacy, unbreak, quick fixes) stay on at every level.
  - **Make them your own**: add any number of filter lists by their https:// address (Custom), and write your own filters, which win over the lists, including exceptions. The lists update on their own as often as you choose, from every 5 minutes to every 30 days (a day to begin with), or only when you press **Update now**; a list is downloaded again only if it changed.
  - **Block an element**: right-click anything on a page and choose **Block element…** (or use the site menu). The picker outlines what's under the pointer; click to choose, make it broader or narrower, and press Enter to hide it on that site from then on. The page doesn't see your clicks while you pick. What you've blocked is in your own filters, to undo; in a private or Tor tab, it's that tab's alone, forgotten when it closes.
  - **Trackers under a site's own name**: a tracker can be given a name on the site you're visiting (`metrics.example.com`), so no list naming the tracker sees it. A request the lists let through is looked at again by the name its host really has, and blocked if that's a tracker's (as uBlock Origin and Brave do). Not in Tor tabs or through a proxy, where the name isn't looked up on your computer.
- **Phishing and malware sites** are stopped before they load, with a warning page. You can still go on if you know better.
- **Google Safe Browsing** (on unless you turn it off): sites on Google's lists of phishing, malware and unwanted software are stopped too. The lists are kept on your computer and updated through Mosaic Browser's proxy server (hosted by Cloudflare), so Google sees the proxy, not you. An address is checked against them on your computer; only when it matches the start of a listed one is that start sent to make sure.
- **Fingerprinting protection.** Firefox's protection is on in every window. On top of it, what sites can measure of your computer (canvas, WebGL, audio) varies from site to site and session to session, so it can't be used to follow you, and the number of processor cores is given only as 4 or 8. A Strict setting goes further.
- **HTTPS only.** An http site opens only after a warning, and you can go on over http for that site if you choose.
- **Secure DNS** with Quad9 (which also blocks domains known to be malicious), Cloudflare or Google, over HTTPS. Your computer's own DNS is asked too when the provider can't be reached or says a name doesn't exist (so Quad9's blocking is complete only in strict mode), or never, if you turn on strict mode.
- **Revoked certificates** are checked against lists downloaded in full, so no one is asked about the sites you visit.
- **Third-party cookies** are kept apart per site, and sites are told not to sell or share your data (Global Privacy Control) and not to track you (Do Not Track).
- **Tracking protection** (Settings > Ad blocking): block trackers, remove tracking parameters from addresses, hide your searches from the sites you go to from a search engine, delete third-party cookies after a while or block them, delete first-party cookies after a while (not recommended), stop WebRTC from showing your IP address, and hide where you came from from third parties. Sites you keep, and sites pinned to the sidebar, keep their cookies; private and Tor tabs are left alone.
- **Each site's cookies and data**: the site menu says how many cookies a site keeps, and Settings lists them, to delete one or all. Block a site's cookies, keep them only until the browser closes, clear everything it keeps, have it **forgotten when its tabs close**, or have it **always open in a sandbox** (or a private tab).
- **Downloads held back**: files that can run code, a web page or picture a site downloaded by itself, and anything that came over plain http wait for you to keep or discard them. One never kept is deleted when the browser closes. What you save yourself with **Save link as…** is kept as you saved it. Nothing about a download is sent to Google to check it, as Firefox does for programs it doesn't know.
- **More guards.** A frame or picture from another site can't ask for a username and password. Files on other computers (`\\server\share`) are never opened. Links are never handed to Windows handlers that have been used to run code. WebRTC uses only your default network connection.
- **Nothing about you is sent to Mozilla**: no telemetry, studies or crash reports, no ping from the installer or uninstaller, and no Firefox account, sync or email masks. There are no sponsored tiles, suggestions, AI chat or promotions either.

### Passwords, addresses and cards

**Your passwords, addresses and cards never leave your computer through the browser.** There's no sync, no account and no cloud: they're kept in an encrypted vault on this computer, and only go out when you fill one into a site, or export or back them up to a file yourself. (A backup is encrypted; an exported CSV file isn't. Either goes wherever you save it, so a folder that OneDrive syncs, for instance, uploads it.)

- **Kept in a vault of their own**, not Firefox's store: every bit of them encrypted (sites and usernames too) with a key only your primary password opens (Argon2id, then AES-256-GCM). They're decrypted only in the browser's memory, and even then a password stays encrypted until it's used.
- **The primary password must be strong**: a meter shows how strong as you type.
- **It locks itself** when you step away from the computer or leave the browser unused for a few minutes (you choose how long), when Windows locks or sleeps, and when the browser closes. Or set it to **always ask**: unlocked for one use (picking a sign-in from the menu under a field, say), then locked again at once.
- **Windows Hello and a recovery key**, if you want them, as other ways to unlock.
- **Filling in**: sign-ins aren't filled in on their own. Click a sign-in field and the site's saved sign-ins are listed under it; the one you pick is filled in (turn filling in as pages load back on in the Passwords page's settings). While your passwords are locked, the menu under the field offers **Show sign-ins**, which unlocks them right there (your primary password, or Windows Hello) and lists the site's, and **Manage passwords**; nothing asks to unlock as a page loads or as you type. Addresses and cards are offered as you click their fields. The browser asks whether to save new and changed passwords, addresses and cards; while your passwords are locked, a sign-in you already saved for a site isn't offered for saving again. Nothing is filled in or offered for saving in private or Tor tabs. A card number stays sealed, even from the page's own process, until you give your primary password again to fill it (that holds for a few minutes).
- **Two-factor codes.** Add a site's setup key (or its `otpauth://` link) to its saved sign-in, and the vault makes its six-digit codes, as an authenticator app does. They're offered under the site's code field, and in its right-click menu; the Passwords page shows the current one and how long it's good for, never the key. The key is sealed in the vault with the rest.
- **The Passwords page**: see, copy, change, generate, add and delete passwords. Copied passwords and usernames are kept out of Windows' clipboard history and cloud clipboard, and a copied password is cleared after a minute. Addresses and cards work the same, and a card's full number shows only after your primary password. There's also a checkup of weak and reused passwords, the vault's settings, encrypted backups and restoring them, importing a CSV file from Chrome, Edge and others, exporting to CSV (asks for your primary password every time), and clearing it all (asks for your primary password, then for you to type CLEAR).

### Everyday browsing

- **The address bar** shows the site with its host standing out. As you type, it completes what you’re typing with the site you visit most that starts so (`you` becomes `youtube.com/`, the rest selected: Enter goes there, Backspace takes it away), from your history and bookmarks on this computer alone, and it suggests searches from your search engine (Google, Bing, DuckDuckGo or Brave Search), your bookmarks and your history. Suggestions from the search engine aren't asked for in private or Tor tabs. A star bookmarks the page (Ctrl+D).
- **The site menu**, in the address bar: the connection's security; what the site may do (camera, microphone, location, notifications, MIDI devices, virtual reality, autoplay, storage, and whether it may ask to handle links like mailto:); pop-ups and redirects; whether it may ask before you leave; its shields and how many they blocked; blocking an element on the page; its cookies and data; and its zoom. Blocked pop-ups are offered from the address bar.
- **Sites' questions** (a site asking for your location, camera and so on) and pages' alerts and sign-ins appear in the browser's own prompt. Alt+Shift+A answers the waiting one. A camera, microphone or speakers come with the choice of which, the default already chosen. Closing a question just turns the site down this once.
- **Pop-ups are Mosaic Browser windows too.** A site's pop-up (a "Sign in with Google" window, say) has the browser's own title bar and a slim toolbar: its address (not for typing over), back, forward, reload and the site menu, at the size the site asked for. New tabs and links from it open in your main window.
- **Google's sign-in prompt** on a dark site (X, for one) sits on the page as it does in Chrome, not in a white box.
- **The new tab page**: your shortcuts (drag them into order; undo a removal), your saved splits, and a background picture of your own (from a file or a link), with blur and frosted panels. Each shortcut shows its site's own large icon where the site offers one, fetched from the site itself without your cookies; in Customize, line your shortcuts up to the left, in the middle or to the right, choose the most in a row, and turn off the animation it opens with if you'd rather have it there at once. Typing there goes straight into the address bar.
- **Sharing your screen**: windows and screens are shown as pictures, each on its own tab, and the one you choose plays live before you share it, with a warning for a whole screen or a Mosaic Browser window. While you share, a small bar stays on top of everything: what's shared and with which site (click to go back to that tab), Stop sharing, and Hide.
- **History** (Ctrl+H): the pages you visited, by day, searchable, each removable, with what you closed lately and your saved sessions at the top. Clear browsing data: history and the downloads list from the last hour, day, week, four weeks or all time (downloaded files stay), and all cookies and site data and the whole cache, whatever the time range.
- **Tools**: screenshots (Ctrl+Shift+S: an area you drag out, the visible part, or the whole page, copied or saved), reader view (F9, its button in the address bar for a page that can be read so), page translation (on your computer, its button in the address bar for a page in another language), the page's source (Ctrl+U), and a task manager (memory and processor use of each tab).
- **26 languages** (Settings > Languages > Display language): English, Arabic, Bengali, Chinese (simplified and traditional), Czech, Dutch, French, Georgian, German, Hebrew, Hindi, Indonesian, Italian, Japanese, Korean, Persian, Polish, Portuguese (Brazil), Russian, Spanish, Thai, Turkish, Ukrainian, Urdu and Vietnamese, Firefox's own parts included after a restart. Arabic, Persian, Hebrew and Urdu lay the whole window out right to left. Our text was translated by AI, using Firefox's own words in each language.
- **Spell check** as you type, in the languages you choose (Settings > Languages), with Mozilla's dictionaries to add. Right-click a text box for suggestions, to turn it off there, or to choose a site's languages. Checking happens on your computer.
- **Downloads** (Ctrl+J): the downloads button shows progress, and its list and the downloads page let you open, show in folder, copy the address, retry, keep or discard a held-back file, and delete. Quitting while anything's still downloading asks first.
- **Torrents**, among the same downloads: click a magnet link or download a `.torrent` file. A torrent with several files asks which ones you want first, with their sizes and where they go. Its row has its speeds, time left and peers, with pause, resume and Stop seeding; on the downloads page its details show the rest (what you've shared, availability, pieces, its trackers) and each file's progress, which you can still tick or untick. Every torrent asks before it starts. Torrents are downloaded by Transmission, which ships with the browser, locked down: it reaches the folders it downloads into and its own, not your profile, your other files or the browser's memory. Never from private or Tor tabs: everyone sharing a torrent can see your IP address, even through Tor.
- **Bookmarks** in the sidebar, in folders (Ctrl+Shift+O), and on the **bookmarks bar** under the address bar: what's in your Bookmarks bar folder, with folders as menus, a menu for those that don't fit, and your main Bookmarks folder at its end. Drag them along it or onto it from the sidebar; right-click it to add the page you're on or to hide it (it's put away in a split). Export them to an HTML file any browser can open, and import one (adding to yours, not replacing them).
- **Extensions** from addons.mozilla.org, with a button of their own beside the address bar. Pin any to the toolbar or into the address bar, with its icon, badge and popup. For each one, choose whether it may run in private tabs, Tor tabs and sandboxes; by default it's kept out of private and Tor tabs. The extensions page (Ctrl+Shift+A) turns them on and off, sets their permissions, options, updates and keyboard shortcuts, and installs from a file.
- **Zoom per site**, from 25% to 500%. Also find in page (with **Highlight all**, every match marked and the current one in another colour), print and developer tools.
- **Clear error pages**: why a page couldn't load, a warning before an http site, a dangerous one or one your filter lists say not to open, and a page for a tab whose page crashed. Reload tries again.
- **How protected to be**, on first start: Maximum (every protection, at its strictest: what's chosen to begin with, and what Skip keeps), Balanced (all but what can break sites), Minimum (the essentials) or None. Each turns Settings' own switches on or off, so any can be changed later.
- **The welcome tour** on first start: what the browser does, a step at a time, with importing bookmarks, history, passwords and cards from Chrome, Edge, Brave, Opera, Vivaldi and others on the same computer. It's in the command palette ("Welcome") to see again.

### Settings

- **Appearance**: light, dark or follow Windows, and an accent colour (ours, Windows' own, or any you pick).
- **On startup**: continue where you left off (tabs load when you go to them) or start with a new tab page. Make it your default browser.
- **Address bar and search**: the search engine, search suggestions, and completing addresses as you type.
- **Toolbar**: always show the downloads button, show the bookmarks bar, and drag the toolbar's buttons into the order you like.
- **Tabs and panes**: where a tab opened from another goes (after it in the order opened, right after it, or at the end of the strip), sleeping tabs and when they hibernate and sleep, whether resting tabs stay asleep when you go to them, how far the mouse wheel turns a tab's volume, scrollable tabs in split panes (and the key to hold for a tab's volume there), and video sandboxing by default in split tabs.
- **Sidebar**: its side, pinning, hiding, showing at the window's edge, its button in a split's corner, and which panels it has.
- **Custom panels**: your own sidebar panels, each with its name, icon, how it runs, whether it may read the page you're on, and its HTML, CSS and JavaScript to edit; export and import.
- **Keyboard shortcuts**: every command and its keys, each to change (click it and press new keys), add to, take away or put back.
- **Privacy and security**: clearing browsing data, shields, always using secure connections, fingerprinting protection (Off, Standard or Strict), secure DNS, Google Safe Browsing, and playing protected content (DRM).
- **Ad blocking**: your security level, shields on or off, the filter list catalogue and how often it updates, lists you've added, your own filters, and tracking protection.
- **Site settings**: each site you've changed something for, with its cookies to see and delete.
- **Languages**: the display language, and spell check and its languages.
- **Downloads**: where they go, or ask each time; and for torrents, how long to keep sharing once one's downloaded (until as much is shared as downloaded, not at all, or until you stop it), and download and upload speed limits.
- **New tab page**: the background picture, its blur, frosted panels, and whether it's animated as it opens.
- **About**: the version, checking for updates (and, unless you turn it off, a check each time the browser starts, with a small popup when a newer version is out), and what's new in each version: every version's notes, looked up from these releases on GitHub as you scroll to them or check for updates, yours marked.

## Keyboard shortcuts

These are the defaults: change any of them in Settings > Keyboard shortcuts. Click a shortcut and press the new keys (Ctrl or Alt with a key, or an F key); Backspace takes it away. Keys another command already has are asked about first, keys that would break typing (Ctrl+C, Ctrl+V and the like) are refused, and your keys win over Firefox's own. Every command, with or without keys, is also in the command palette (Ctrl+K).

A web page gets most keys first, as in any browser, so a site's own Ctrl+B, Ctrl+K or Ctrl+F works in it, and the browser's does its thing wherever the page doesn't take it. These are always the browser's: new tab, new window and new private window, close tab, reopen closed tab, next and previous tab, exit, answering a site's question, the keys for panes (split, close pane, keep its bar visible, focus a pane), Ctrl+Shift+P for the command palette, and F6.

| Keys | Command |
|---|---|
| Ctrl+T | New tab |
| Ctrl+N | New window |
| Ctrl+Shift+N | New private window |
| Ctrl+W, Ctrl+F4 | Close tab |
| Ctrl+Shift+T | Reopen closed tab (or window) |
| Ctrl+1 to Ctrl+8, Ctrl+9 | Go to tab 1 to 8, the last tab |
| Ctrl+Tab, Ctrl+PageDown | Next tab |
| Ctrl+Shift+Tab, Ctrl+PageUp | Previous tab |
| Ctrl+L, Alt+D, F6 | Address bar |
| Ctrl+K, Ctrl+Shift+P | Command palette |
| Alt+Left, Alt+Right | Back, forward |
| F5, Ctrl+R | Reload |
| Ctrl+F5, Ctrl+Shift+R, Shift+F5 | Reload, skipping the cache |
| Ctrl+F | Find in page |
| F3, Ctrl+G / Shift+F3, Ctrl+Shift+G | Find next / previous |
| Ctrl+=, Ctrl+-, Ctrl+0 | Zoom in, out, back to 100% |
| Ctrl+\ | Split pane right |
| Ctrl+Shift+\ | Split pane down |
| Ctrl+Alt+Arrows | Move to the pane left, right, above, below |
| Ctrl+Shift+W | Close pane and its tabs |
| Ctrl+Shift+B | Keep pane bar visible |
| Ctrl+B | Sidebar |
| Ctrl+D | Bookmark this page |
| Ctrl+Shift+O | Bookmarks |
| Ctrl+H | History |
| Ctrl+J | Downloads |
| Ctrl+Shift+A | Extensions |
| Ctrl+, | Settings |
| Ctrl+Shift+Delete | Clear browsing data |
| Alt+Shift+A | Answer a site's question |
| Ctrl+Shift+S | Screenshot |
| F9 | Reader view |
| Ctrl+U | View page source |
| Ctrl+P | Print |
| F12, Ctrl+Shift+I | Developer tools |
| Ctrl+Shift+Q | Exit |

## Installing

Download `mosaic-browser-<firefox version>.en-US.win64.installer.exe` from the latest release and run it. The installer isn't code-signed yet, so Windows SmartScreen says it "protected your PC": choose **More info**, then **Run anyway**. It loads Windows' own system files only from Windows' folder, so a file a site left in your Downloads folder can't slip in when you run it from there.

Then **Install**. It installs as **Mosaic Browser** in `C:\Program Files\Mosaic Browser`, with a Start menu entry, a desktop shortcut and an uninstaller; **Options** lets you choose another folder, and leave out the shortcut. To pin it to the taskbar, right-click its button there while it's open and choose **Pin to taskbar** (Windows doesn't let an installer pin it). Installing in Program Files needs an administrator's permission, which Windows asks for. When it's done, **Open Mosaic Browser**.

Run over a copy that's installed already, it offers **Update** instead, and keeps your profile: tabs, passwords and settings. A copy installed as Project B is updated where it is, and its shortcuts take the new name.

## Uninstalling

Uninstall from Windows' Installed apps. Mosaic Browser's own uninstaller removes the program and its shortcuts. Turn on **Also delete my data** to delete everything Mosaic Browser keeps for your Windows account as well, in every profile: history, saved passwords and cards, bookmarks, cookies, sandboxes, Tor's data, your torrents' list and progress, settings, the profiles' pictures and their Windows Hello keys. Profiles' Start menu shortcuts go with the program. Your downloaded files stay, and so does what other Windows accounts on this computer keep, and another Firefox on the same computer is never touched. If Windows runs the uninstaller as another account (a standard account, an administrator's password given), your data can't be reached from there, and is kept. Left off, your data is kept for when you install again.

## Checking the download

Each release has a `SHA256SUMS` file. In a terminal, in the folder you downloaded to:

```
certutil -hashfile mosaic-browser-160.0.en-US.win64.installer.exe SHA256
```

The result should match the installer's line in `SHA256SUMS`. From 0.5.1 on, `SHA256SUMS.sig` is its signature, made with the project's own key; the browser checks it itself before it updates.

To check that signature yourself, so you know `SHA256SUMS` is the project's and not just whatever this release holds, you need OpenSSL 3 (Git for Windows' Git Bash has it). Save the project's two public keys (the one releases are signed with, and its spare) as `mosaic.pem` and `mosaic-spare.pem`:

```
-----BEGIN PUBLIC KEY-----
MCowBQYDK2VwAyEAMtyQylRs5aEejAIF+1/GtGhwhqswcc7CJNzAIIE2DK8=
-----END PUBLIC KEY-----
```

```
-----BEGIN PUBLIC KEY-----
MCowBQYDK2VwAyEADBqbdZF/2ROMIrqjKWexieYhYbO6vUWjmodUcfZxCeo=
-----END PUBLIC KEY-----
```

Then, in the folder with `SHA256SUMS` and `SHA256SUMS.sig`:

```
openssl base64 -d -A -in SHA256SUMS.sig -out SHA256SUMS.sig.bin
openssl pkeyutl -verify -pubin -inkey mosaic.pem -rawin -in SHA256SUMS -sigfile SHA256SUMS.sig.bin
```

It should say `Signature Verified Successfully` (or with `mosaic-spare.pem` in place of `mosaic.pem`: the spare signs if the first key is ever lost). The first line of `SHA256SUMS` is the version it's for, which should be the release's. These are the same keys the browser has built in; someone who got into this GitHub account could change this page too, so keep a copy of them, and compare.

## Updates

Mosaic Browser looks for a newer release here each time it starts (and tells you in a small popup if there is one), or once a day with that turned off (Settings > About; Check for updates there looks now). From 0.5.1 on, it takes a release only if its `SHA256SUMS` is signed with the project's key, for that very version, so no one else can put out an update even if they got into this GitHub account. Choose **Download** in Settings > About and it downloads the new installer and checks it against that release's `SHA256SUMS`. When you choose **Install and restart** (with your other profiles closed), it closes, the installer puts the new version in place with its progress showing, and Mosaic Browser starts again.

## Known limits

- 0.7 to 0.7.26 are experimental releases: what was there in 0.6.2 works as it did (0.7.2 and 0.7.3 fix everything an independent review of the whole browser found), but their new features (profiles, their taskbar buttons, which profile opens a link, tab groups, what's new in About) need extensive testing. Features new in 0.6.2 (the menu under a sign-in field while your passwords are locked), 0.6.1 (the security level on first start), 0.6 (the languages, Google Safe Browsing, custom panels' editor and API, procedural and pop-up filters) and 0.5.1 (custom panels, workspaces, video sandboxing, your own filter lists and filters, blocking an element, two-factor codes, saved sessions and the rest in its notes) aren't fully tested yet.
- The translations haven't been read through by native speakers yet: if something reads wrong, [open an issue](https://github.com/nikolozdolidze/mosaic-browser-releases/issues).
- Windows only, 64-bit.
- Not code-signed yet (see Installing).
- At Maximum, the level a new profile starts on, a few sites may not work properly, and public Wi-Fi sign-in pages won't open (secure DNS never falls back to your computer's). Balanced, or turning strict mode off in Settings > Privacy and security, puts that right.
- Netflix, Disney+, Spotify and other protected streaming don't play until you allow it: the site asks, or turn on **Play protected content (DRM)** in Settings > Privacy and security. Nothing is downloaded from Google (Widevine) or Cisco (OpenH264) before that.
- A site's notifications come only while it's open in a tab.
- Tor tabs don't work on a network that blocks Tor: bridges aren't included.
- The installer unpacks into your own temporary folder before Windows asks for an administrator's permission, as Firefox's installer does. A program already running on your Windows account could change what's unpacked there, and so what gets installed; nothing from outside your account can.
- A tab group moves as a whole only within its own window; its tabs can still be dragged to another window one at a time.
- Tor tabs send everything through Tor, but to a site they look like Firefox on Windows, not like Tor Browser.
- The camera question doesn't show a live preview of the camera yet.

## Licenses

Mosaic Browser's own code is under the Mozilla Public License 2.0. It's built on [Firefox](https://www.firefox.com/) (Mozilla Public License 2.0), whose source is at [github.com/mozilla-firefox/firefox](https://github.com/mozilla-firefox/firefox). It includes the Tor Project's `tor.exe`, unchanged (GNU GPL 3.0; its source is at [dist.torproject.org](https://dist.torproject.org/)). It also includes Transmission's `transmission-daemon.exe`, unchanged (GNU GPL; its source is at [github.com/transmission/transmission](https://github.com/transmission/transmission)), with the libraries it needs: curl (curl license), OpenSSL (Apache License 2.0) and zlib (zlib license). In the folder it's installed in, `tor\docs` and `transmission\docs` hold their licenses and where their source is. It also includes Ghostery's ad-blocking engine (Mozilla Public License 2.0), and tldts, hash-wasm's Argon2, zxcvbn-ts and CodeMirror (all MIT).
