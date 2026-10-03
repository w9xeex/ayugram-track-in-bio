# Track in Bio

A plugin for AyuGram / exteraGram that shows the track you are listening to in your Telegram bio, and restores your original bio when the music stops.

Example bio while playing:

> 🎵 Artist - Track name

## How it works
Music player → scrobbler app → Last.fm → this plugin → Telegram bio

Every 30 seconds the plugin asks Last.fm what you are listening to right now. If the track changed, it updates your bio. When nothing is playing, it puts your old bio back.

## Requirements

- AyuGram (or exteraGram) with plugin support
- A [Last.fm](https://www.last.fm) account and a free API key
- Any app that scrobbles your player to Last.fm (for example, [Pano Scrobbler](https://github.com/kawaiiDango/pScrobbler) on Android)

## Installation

1. Download `lastfm_bio.plugin` from this repository.
2. Send it to your Saved Messages and tap it to install.
3. Open Settings → Plugins → Track in Bio.
4. Enter your Last.fm API key and username.
5. Tap "Check Last.fm now" while a track is playing to make sure it works.
6. Turn on "Show track in bio".

Get an API key here: https://www.last.fm/api/account/create

## Notes

- Your original bio is saved before the first change and restored when the music stops or the plugin is turned off. Make sure your bio contains your normal text before enabling the plugin.
- The bio is limited to 70 characters, long names are shortened.
- The plugin only works while the app is running. Allow AyuGram and your scrobbler to run in the background (battery setting: unrestricted).
- Your API key is stored in the plugin settings on your phone, not in this repository.
- Last.fm may show "now playing" with a delay of a minute or two.

## Status

Tested on AyuGram. This is an unofficial hobby project.
