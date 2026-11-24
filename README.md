# CyberGrindPlaylistBuilderOS 2.0

Build your ULTRAKILL Cyber Grind playlist in the browser instead of the in-game terminal.

**Use it here: [cybergrindplaylist.online](https://cybergrindplaylist.online/)**

![CyberGrindPlaylistBuilderOS 2.0](preview.png)

## What it does

Picking songs in the Cyber Grind's playlist menu works, but it's slow. This site lets you pick from all 82 built-in songs, put them in the order you want, and download a ready-made `slot1.json` that the game loads.

- Click or drag songs from the library into your playlist
- Drag songs to reorder them, on PC or phone (press and hold on mobile)
- Shuffle and repeat, just like in the game
- Import your current `slot1.json` to edit it, custom songs included
- Your playlist is saved in your browser, so a refresh doesn't lose it
- Undo for Clear, Add all and Import

## How to use it

1. Open [cybergrindplaylist.online](https://cybergrindplaylist.online/) and build your playlist.
2. Click **Download slot1.json**.
3. Keep a copy of your old `slot1.json`, just in case.
4. Put the new file in your Playlists folder, replacing the old one. On a standard Steam install it's here:
   ```
   C:\Program Files (x86)\Steam\steamapps\common\ULTRAKILL\Preferences\Playlists
   ```
   Installed somewhere else? In Steam, right-click ULTRAKILL, choose **Manage**, then **Browse local files**, and open `Preferences\Playlists`.
5. Open the Cyber Grind. You don't need to close the game first, it works even while you're in the Cyber Grind lobby.

## Good to know

- **Locked songs work.** Songs play in your playlist even if you haven't unlocked them in the Cyber Grind yet. The library includes music from later levels, so the song names can spoil a little.
- **Repeat** loops the song you highlight. With shuffle on as well, the game picks one random song and loops it.
- **Custom music** is kept when you import your `slot1.json`. To add new files of your own, use the in-game playlist menu.

## How it works

The game stores your playlist in `slot1.json`. Each built-in song is saved as a 32-character ID, and custom songs as a file path:

```json
{
  "_ids": [
    { "path": "c90a6ca8dddd623478c6e608f94b5166", "type": 0 },
    { "path": "C:\\Music\\my-song.mp3", "type": 1 }
  ],
  "_loopMode": 0,
  "_selected": 0,
  "_shuffled": true
}
```

The IDs aren't listed anywhere official, so all 82 were matched to their song names by hand. They're the same for every player.

The whole site is one HTML file with no build step and no backend, hosted on GitHub Pages.

## Privacy

The site uses [GoatCounter](https://www.goatcounter.com/) to count visits and how many playlists get downloaded. It doesn't use cookies or collect personal data. Your playlist itself never leaves your browser.

## Feedback

Found a bug or have an idea? [Open an issue](https://github.com/adr1an-dev/cg-playlist-builder/issues).

---

Made by [Adrian](https://github.com/adr1an-dev) for the ULTRAKILL community. Fan-made, not affiliated with New Blood Interactive. ULTRAKILL and its music belong to their owners.
