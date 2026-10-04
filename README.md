# Track in Bio

A plugin for AyuGram / exteraGram that shows the track you are listening to in your Telegram bio (or business location) and restores your original text when the music stops. It also adds a `.np` command that sends a card with the current track to any chat.

Example bio while playing:

> 🎵 Artist - Track name

## Features

- **Bio or business location.** Show the track in your bio, or in your business location (Telegram Premium only). Your previous text or address is saved and put back when the music stops.
- **Custom format.** Use `{artist}` and `{title}`, for example `🎵 {artist} - {title}`.
- **Limits handled for you.** 70 characters in the bio (140 with Premium), 96 in the location.
- **`.np` command.** Type `.np` in any chat to send a card with the cover, title and artist. Four styles: dark, light, square and minimal. Optional link in the caption (Last.fm or Yandex Music search).
- **Hide tracks.** A list of artists or words that should never appear, and quiet hours (for example `23:00-07:00`).
- **Pause switch.** Stops changing your profile and restores the original text.
- **Stale status protection.** If a "now playing" status lasts longer than the track itself, the plugin treats it as stale and restores your text.
- **Adjustable check interval** from 5 to 120 seconds (10 by default).

## How it works

```
Music player → scrobbler app → Last.fm → this plugin → Telegram
```

The plugin asks Last.fm what you are listening to right now. When the track changes, it updates your profile. When nothing is playing, it puts your old text back.

## Requirements

- AyuGram (or exteraGram) with plugin support
- A [Last.fm](https://www.last.fm) account and a free API key
- Any app that scrobbles your player to Last.fm (for example, [Pano Scrobbler](https://github.com/kawaiiDango/pScrobbler) on Android)

## Installation

1. Download `lastfm_bio.plugin` from the [latest release](../../releases/latest).
2. Send it to your Saved Messages and tap it to install.
3. Open Settings → Plugins → Track in Bio.
4. Enter your Last.fm API key and username.
5. Tap "Check Last.fm now" while a track is playing to make sure it works.
6. Turn on "Show track in profile".

Get an API key here: https://www.last.fm/api/account/create

## Notes

- Your original bio (or location) is saved before the first change. Make sure it contains your normal text before enabling the plugin.
- If your location has a map point set, the plugin will not overwrite it and the location mode will not start.
- The plugin only works while the app is running. Allow AyuGram and your scrobbler to work in the background (battery setting: unrestricted, autostart enabled).
- Your API key is stored in the plugin settings on your phone, not in this repository.
- Last.fm may show "now playing" with a delay of a minute or two, and it does not know when you pause the music. The status clears itself at about the end of the track.
- The `.np` command works regardless of the hide list and quiet hours.
- Do not run it together with other plugins that change your bio.
- Tested with [Lane](https://sklane.com/ru) as the music player.

## Status

Tested on AyuGram (bio mode and the `.np` command). Business location mode is experimental. This is an unofficial hobby project.

## License

MIT
