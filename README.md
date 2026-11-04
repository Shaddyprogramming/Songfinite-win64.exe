# Songfinite

A pixel-pink desktop music player for your own files and YouTube links,
with synced karaoke lyrics, offline copies and an endless YouTube radio made
from your taste.

Your songs, videos and links live in one library. Nothing is uploaded and
nothing leaves your computer except the requests needed to play, look up and
download what you ask for.

## Download

[link](https://github.com/Shaddyprogramming/Songfinite-win64.exe/releases/download/v1/SongfiniteSetup-1.22.exe)

---

## What it does

| Part | What it holds | Highlights |
| --- | --- | --- |
| `LIBRARY` | Files, folders, YouTube and Spotify links | Playlists with their own covers, favourites, ratings, tags, smart views |
| `PLAYER` | The song playing, its video and the queue | Gapless, crossfade, 10-band EQ, speed, A-B loop, sleep timer |
| `LYRICS` | Synced and plain lyrics | Smart download, Lyrics Studio, karaoke in full screen |
| `SONGS WINDOW` | Every song as a grid or a list | Filters that combine: playlists, "in no playlist", tags, stars |
| `YOUTUBE RADIO` | Endless mixes from your taste | Stations per sound, rerolls, ADD and DOWNLOAD on every song |
| `MINI PLAYER` | A small window that stays on top | Eight looks, from a pill to a visualizer or lyrics |

**One library for everything.** Local files (MP3, M4A, AAC, WAV, FLAC, OGG,
OPUS, WMA, AIFF, ALAC, APE, MKA and video files) sit next to YouTube links.
Spotify links keep Spotify's title, artist, length and cover and play the
closest YouTube upload, checked against the song's length so live versions
and hour-long loops are passed over.

**Lyrics that keep time.** Lyrics are found automatically or pasted in, then
synced line by line in the Lyrics Studio. The studio can also search Google,
Genius or Musixmatch; whatever you copy there comes back to the editor.

**A radio that never runs out.** Sign in with Google and the radio reads your
likes, playlists and subscriptions, read only. It sorts them into sounds
(nightcore, rock versions, phonk, lo-fi, the artists you love) and turns each
into a station. When a mix nears its end, the mix of the song playing joins it.

**Offline when you want.** Any link can be kept as a video or an MP3, with its
title, artist and cover written into the file.

---

## Using it

1. **Add songs.** Drag files, folders or links onto the window, or press `ADD`
   (`Ctrl` + `N`). Pasting a link anywhere (`Ctrl` + `V`) adds it too. Watched
   folders pick up new files by themselves.
2. **Make playlists.** `+` beside `PLAYLISTS` in the left panel. Drag songs onto
   a playlist to add them. Each playlist gets a cover: an icon, letters, a
   drawing, a picture or a mosaic of its songs.
3. **Play.** Double click a song. The header of a playlist folds away as you
   scroll; the shuffle button fills pink when shuffle is on.
4. **Sing along.** Open `LYRICS` in the right panel. Right click a song for
   `Smart download lyrics` or `Lyrics studio…` to sync it yourself. `F` goes
   full screen with the lyrics floating over the video.
5. **Tune in.** Press `RADIO` at the top of the left panel. Pick a mix, a sound
   or a playlist; every song in a mix has `ADD` (keep the link) and `DOWNLOAD`
   (keep it offline). `REROLL` starts the station again from other songs.
   Right click any song for `Start a mix from this song`.

---

## Interface

- **Title bar.** Drag to move, double click to maximise. On the right: your
  Google account, settings, day and night, the mini player and the window
  buttons. The status line reports what just happened.
- **Left panel.** `ADD` and `RADIO`, the songs window, listening stats, the
  lyrics library, the library views, smart views and your playlists.
- **Centre.** The video or the spinning record above the song list. Either
  can be folded away.
- **Right panel.** `UP NEXT` and `LYRICS`. The arrow at its edge folds it to
  a thin strip at any time.
- **Deck.** Play controls, the seek bar, volume, and the buttons for video,
  A-B loop, speed, EQ, sleep and saving offline.
- **Account page.** Your Google profile, the YouTube sign-in used for
  downloads, and the radio's settings.

### Shortcuts

| Keys | Action |
| --- | --- |
| `Space` | Play or pause |
| `Ctrl` + `→` / `Ctrl` + `←` | Next / previous song |
| `→` / `←` | Seek forward / back |
| `Shift` + `→` / `Shift` + `←` | Seek further |
| `Ctrl` + `↑` / `Ctrl` + `↓` | Volume up / down |
| `M` | Mute |
| `S` / `R` | Shuffle / repeat |
| `V` | Show or hide the video |
| `L` | Love the song |
| `B` | A-B loop |
| `E` | Equaliser |
| `T` | Sleep timer |
| `[` / `]` | Slower / faster |
| `D` | Save the song offline |
| `F` | Full screen |
| `Ctrl` + `N` | Add songs |
| `Ctrl` + `Shift` + `N` | New playlist |
| `Ctrl` + `F` | Search |
| `Ctrl` + `L` | Lyrics library |
| `Ctrl` + `I` | Listening stats |
| `Ctrl` + `M` | Mini player |
| `Ctrl` + `T` | Day and night |
| `Ctrl` + `,` | Settings |
| `Esc` | Leave full screen |

---

## Good to know

- **Helpers.** YouTube playback needs `deno`, and MP3 saving needs `ffmpeg`.
  When either is missing, a gift appears in the title bar: the helpers card
  downloads and installs them for you.
- **Google sign-in is optional.** It is read only: Songfinite can see your
  likes, playlists and subscriptions, and cannot change anything. YouTube does
  not give apps your watch history; import `watch-history.json` from Google
  Takeout on the account page to teach the radio more.
- **Downloads go as you.** YouTube asks guests to prove they are not bots.
  Songfinite finds the browser where you are signed in to YouTube and borrows
  only its YouTube and Google cookies. Firefox works best; newer Chrome and
  Edge lock their sign-in away, so for them export a `cookies.txt` and use
  `IMPORT` on the account page.
- **Radio songs** are only borrowed until you `ADD`, `DOWNLOAD`, love them or
  put them in a playlist. Until then they do not show in your library.
- **Your data** lives in `Documents/ShaddyGames/Songfinite`: `library.json`,
  `settings.json`, and the `media`, `lyrics` and `covers` folders. The
  media and covers folders can be moved in settings.
- **Building from source:** `python install.py` installs the packages and
  libmpv, `python main.py` runs it, `python build.py` makes the executable and
  `python setup.py` the installer. To use Google sign-in in your own build,
  fill `GOOGLE_CLIENT_ID` and `GOOGLE_CLIENT_SECRET` in `constants.py` with a
  Desktop app OAuth client that has the YouTube Data API v3 turned on.
- Only download what you have the right to keep.
- The window will not go below 1060 × 680.

## If something goes wrong

| Symptom | Cause |
| --- | --- |
| `Sign in to confirm you're not a bot` | YouTube wants a signed-in person. Sign in to youtube.com in Firefox, or import a `cookies.txt` on the account page. |
| It still asks while `· YT` shows by your name | YouTube changed its checks. Update the YouTube helper from the helpers card, or try again later. |
| `MP3 NEEDS FFMPEG` | Install the HD saver from the helpers card. |
| `Error 403: access_denied` on Google's page | Your account is not a test user of the Google project. Add it under Audience, or publish the app. |
| Sign in with Google is greyed out | `GOOGLE_CLIENT_ID` and `GOOGLE_CLIENT_SECRET` are empty in `constants.py`. |
| `COULD NOT OPEN` on a link | The video is private, removed or blocked in your country. |
| A local song will not play | The file was moved or deleted. Add it again from its new place. |
| Windows says it protected your PC | The installer is not code-signed. Press `More info`, then `Run anyway`. |
