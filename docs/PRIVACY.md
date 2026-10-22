# Peak and your privacy

Peak runs on your Mac and keeps what it knows there. It has no accounts, no analytics, no tracking, no crash
reporting service and no ads. This page says exactly what it reads, keeps and sends.

## What Peak sends over the internet

One thing: **Spotify's album art** for the song playing in Spotify. Peak asks Spotify's own public service
(`open.spotify.com`) for the cover of that song, by the track ID Spotify itself announces, then downloads the picture
from Spotify's image servers. Once per song, over HTTPS, with no cookies and nothing cached on disk. Nothing else ever
leaves your Mac: not your files, your calendar, what you play, or how you use Peak.

Opening a link from Settings › About (updates, reporting a problem) opens it in your browser, only when you click
it.

## What Peak reads, on your Mac

| What | Why | How |
|---|---|---|
| What's playing | The song on Home and beside the notch | Music's and Spotify's own announcements; for other apps (browsers, podcasts), macOS's Now Playing, a video's thumbnail included (from macOS, never downloaded) |
| Your calendar | Today on Home, and a meeting about to start | Only after you allow it (macOS asks the first time Peak opens); events are shown, never changed |
| Downloads in progress | Their progress, and the file once it's done | The progress browsers publish; Peak never lists your Downloads folder |
| New screenshots | Showing each one for a moment, and among Recent | Spotlight says when one's added; Peak reads a screenshot's picture only to show it |
| The sound devices and their volume | The volume, and the Sound panel | macOS's audio system |
| Which apps use the microphone | Knowing a call is under way | The names of the apps only: Peak never hears anything |
| Headphones' batteries | The Sound panel's device list | macOS's Bluetooth information, while the panel is open |
| Windows' positions, sizes and titles | Window snapping and Snap Assist | Positions from macOS; with Accessibility (which you allow), titles and moving windows; never what's in them |

## What Peak keeps

- **Your settings**, the players Peak has controlled, and which apps window snapping placed together, in
  `~/Library/Preferences/com.wetzeldevelopments.Peak.plist`.
- **What you hold in Files**: bookmarks to the original files (so Peak can find them if they move), and links and text
  you dropped, in `~/Library/Application Support/Peak/Shelf/shelf.json`.
- Everything else, such as album art, recent files and timers, is kept in memory and gone when Peak quits.

Peak never moves, changes or deletes your files. Dragging something out of Peak always makes a copy, and removing it
from Peak only lets go of Peak's bookmark.

## What Peak logs

Peak writes diagnostic messages to macOS's own log, on your Mac. File names, songs, device and app names are marked
private there (macOS hides them in logs unless you're debugging), and what's in your calendar is never logged.

## Permissions

Peak asks for a permission only when a feature first needs it, and works without it:

- **Calendar**, as Peak first opens, for Today.
- **Automation** for Music and Spotify, the first time you use their controls.
- **Accessibility**, the first time you snap a window.
- macOS may ask about your **Desktop** folder (a screenshot saved there) or **Downloads** folder (sharing a finished
  download).

Peak never asks for Screen Recording, the microphone, the camera, location, contacts, or Input Monitoring. Its
keyboard shortcuts are system hot keys, which see no other keystroke.

## Removing what Peak kept

Delete `~/Library/Application Support/Peak`, and run `defaults delete com.wetzeldevelopments.Peak` in Terminal. The
permissions you gave it are in System Settings › Privacy & Security.
