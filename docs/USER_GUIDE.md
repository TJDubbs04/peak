# Using Peak

Peak turns your MacBook's notch into a small, live surface: what's playing, today's calendar, a call, downloads,
timers and files that just arrived, a place to hold files for a while, and window snapping. It stays out of the way
until you hover the notch. Peak is free.

## What you need

- **A Mac with a notch:** MacBook Pro 14-inch or 16-inch (2021 and later) or MacBook Air (M2, 2022, and later). Peak
  lives in the notch: on a display without one (or with the lid closed and only an external display in use), it waits
  in the menu bar, and its menu says why.
- **macOS 14 Sonoma or later.**

## Install

1. Download the disk image (`Peak-<version>.dmg`) from the
   [latest release](https://github.com/TJDubbs04/peak/releases/latest) and open it.
2. Drag **Peak** onto **Applications**.
3. Open Peak from your Applications folder.

Peak has no Dock icon. The first time it opens, the notch shows **Peak is ready** for a moment, with **Open at Login**
(so Peak starts with your Mac) and **Settings**. macOS also asks once whether Peak may see your calendar: that's for
Today on Home, and Peak works without it.

You'll find Peak afterwards in the menu bar (the mountain icon: Settings, Quit) and, of course, at the notch.

## Getting around

- **Hover the notch** to open Peak; move away and it tucks back in. **Click** it (or the pin on the left) to keep it open
  until you click somewhere else.
- **Home** and **Files** are the two tabs. A two-finger swipe sideways switches between them.
- **Right-click** Peak for Settings and Quit. Settings is also the gear beside the notch, and in the menu bar.

## What's on Home

- **The song playing**, from Music, Spotify, your browser or any app macOS shows as Now Playing: its cover or a video's
  thumbnail (or its app's icon), previous, play or pause, next, and a bar you can drag to move through it. With two
  things playing, the other is a line under the card: click it to show it there, or play and pause it from its button.
  A video's ads show as what they are to your browser, short videos of their own; they don't pop up at the notch.
- **Today**, from your calendar: what's on now or next (with **Join** for an online meeting), the next two, and a
  chevron for the whole day and the days either side.
- **A row for what's under way:** a call (its time, **Mute**, **Show**), downloads, timers (**Pause**, **+1 min**,
  **Cancel**), keeping the Mac awake (**End**), and a screenshot or download that just arrived (drag it straight into
  another app, or **Keep** it in Files).
- **Quick actions** at the bottom: **Timer**, **Keep Awake** (stops your Mac sleeping for a while) and **Audio** (the
  volume, the microphone, and the devices they use).

While Peak is tucked away, what's going on shows beside the notch: the song's cover and bars, a timer's time, a
download's progress, a call's time, or a meeting about to start. Brief moments come and go by themselves too: a song
changing, the volume, a charger, headphones, a download or timer finishing, a new screenshot.

## Files

Drag files, folders, links or text onto the notch to hold them. Drag them back out wherever you need them: a file is
always copied, and the original never moves. On Files, click items to choose several and drag them together, point at
one to pin or remove it, or right-click it for Open, Show in Finder, Share or Copy. **AirDrop** at the bottom sends what
you chose (or everything held), and dropping files on Peak's AirDrop square sends them straight away. **Clear** lets go
of everything that isn't pinned. Removing something from Peak never deletes the original.

New screenshots (taken as usual with ⇧⌘3, ⇧⌘4 or ⇧⌘5) and finished downloads show up under **Recent** for a while.

## Window snapping

Drag a window toward the notch and six layouts appear below it. Drop the window on the zone you want; then Peak offers
your other windows for the rest of the layout, one zone at a time (Escape, or a click elsewhere, leaves them).
From the keyboard, **⌃⌥** with an arrow snaps the window in front to a half of its screen, **U I J K** to a quarter,
**D F G** to a third, and **Return** fills the screen. Settings › Windows turns snapping or its shortcuts off.

## Permissions

Peak asks only when a feature first needs something, and keeps working when you say no.

| What | When macOS asks | What it's for | If you decline |
|---|---|---|---|
| Calendar | The first time Peak opens | Today on Home, and a meeting about to start beside the notch | Today shows a line with Open Settings; the rest of Peak works |
| Automation (Music, Spotify) | The first time you press play, pause, next or previous for them | Controlling Music and Spotify | Their song still shows; the card says where to allow control |
| Accessibility | The first time you snap a window | Moving and resizing windows, and reading their titles for Snap Assist | Snapping doesn't move windows; Peak says where to allow it |
| Desktop folder | Perhaps, the first time Peak shows a screenshot saved to your Desktop | Showing that screenshot's picture | The screenshot shows without its picture |
| Downloads folder | Perhaps, the first time you share or drag out a finished download | Handing the file to the app or Share menu | That download can't be shared from Peak |

Peak never asks to record your screen, use your microphone or camera, or monitor your keyboard. It sees which apps use
the microphone (to know a call is under way), never what it hears. What it reads and keeps is in
[Privacy](PRIVACY.md).

You can change any of these later in System Settings › Privacy & Security.

## Settings

Settings has: **Open at login**; what Peak shows (music, calendar, downloads, timers, Keep Awake, Mac changes, the volume,
calls); Files, AirDrop and recent screenshots; window snapping and its shortcuts; showing Peak beside the notch; what Peak
reads and asks for; and **About**, with Peak's version.

## Updating

Peak doesn't update itself yet. When a new version is out, download its disk image from
[Peak's releases page](https://github.com/TJDubbs04/peak/releases) (Settings › About › **Check for Updates…** opens it), quit Peak (menu bar › Quit Peak), and drag the new Peak onto
Applications, replacing the old one. Your settings and held files stay.

## Uninstalling

1. In Settings, turn off **Open at login** (or remove Peak in System Settings › General › Login Items).
2. Quit Peak (menu bar › Quit Peak) and drag it from Applications to the Trash.
3. To remove what it kept too: delete `~/Library/Application Support/Peak`, and run
   `defaults delete com.wetzeldevelopments.Peak` in Terminal for its settings.
4. Permissions you gave it are listed in System Settings › Privacy & Security, where you can remove them.

## Where Peak keeps things

| What | Where |
|---|---|
| Settings, the players Peak has controlled, the apps window snapping placed together | `~/Library/Preferences/com.wetzeldevelopments.Peak.plist` |
| What you hold in Files (as bookmarks to the originals, plus links and text) | `~/Library/Application Support/Peak/Shelf/shelf.json` |
| Everything else (album art, recent files, timers, the calendar's day) | Memory only, gone when Peak quits |

## Troubleshooting

- **Peak doesn't appear.** Peak needs a display with a notch: check the menu bar's mountain icon (its menu says if
  there's no notch display in use). If **Show Peak beside the notch** is off, Peak hides inside the notch until
  something happens: hover the notch.
- **Music or Spotify won't respond to Peak's buttons.** Allow Peak in System Settings › Privacy & Security ›
  Automation (Settings › Privacy has a button for it).
- **A song in the browser doesn't show.** Peak shows what macOS shows as Now Playing, one app at a time; check Control
  Center's Now Playing. Pressing play in the browser again usually brings it back.
- **Today is empty.** Allow Peak in System Settings › Privacy & Security › Calendars.
- **Windows don't snap.** Allow Peak in System Settings › Privacy & Security › Accessibility. If it's already allowed
  and snapping still doesn't work (after replacing Peak, say), turn it off and on again there.
- **Peak doesn't start with my Mac.** Turn on Settings › Open at login, and check System Settings › General › Login
  Items.
- **macOS says Peak can't be opened.** Download Peak only from its
  [releases page](https://github.com/TJDubbs04/peak/releases); those builds are signed and notarized by Apple.

## Reporting a problem

Settings › About › **Report a Problem…** opens [Peak's issues](https://github.com/TJDubbs04/peak/issues/new/choose).
Say what happened and how to make it happen, your Peak version (Settings › About), your macOS version, your Mac model,
and whether you use external displays.
