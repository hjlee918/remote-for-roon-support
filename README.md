# Remote for Roon

Support page for **Remote for Roon**, a Stream Deck plugin for Roon, the music player from Roon Labs: scenes that set up your whole system with one press, your library on keys and on the Stream Deck + dial, Album Roulette, an active zone your keys follow, transferring music between zones, grouping zones, switching your amplifier on, playback and volume keys that show what's happening, and what's playing with its album art and progress. The plugin is in development and not on the Elgato Marketplace yet.

## Get help

- **Found a bug?** [Open a bug report](../../issues/new?template=bug_report.yml).
- **Have an idea?** [Suggest a feature](../../issues/new?template=feature_request.yml).

Please search [existing issues](../../issues) first. Issues are public.

## Requirements

- Windows 10 or later, or macOS 12 or later.
- Stream Deck 7.1 or later.
- Roon, with its Roon Core (Roon Server) on the same network as the computer.

## Setup

1. Drag any **Remote for Roon** action onto a key, for example **Transport**. The key says **Enable in Roon**.
2. In Roon, open **Settings → Extensions** and click **Enable** next to "Remote for Roon (Stream Deck)". You only do this once.
3. In the key's settings, choose what the key does. Keys follow the **active zone** unless you choose a zone. Add a **Zone** key to switch the active zone. Add more keys; they all share the connection.

The plugin finds your Roon Core on its own. If it doesn't, type the Core's IP address in **Address** and click **Add**.

**More than one Roon Core?** Each key then has a **Core** menu; enable the extension on each Core you want to use.

## The actions

| Action | What it does |
|---|---|
| **Scene** | One press for a whole set-up. Each step is optional, and they run in this order: **switch on** the zone's audio devices, **group** zones with it, set the **volume**, **shuffle** on or off, **play** something from your library, **fade out** (over 10 seconds to 15 minutes, then pause; the volume goes back afterwards), **pause** this zone or every zone, **standby**, and make it the **active zone**. Press again while it runs to stop it. |
| **Play** | A playlist, album, artist, genre, composer or internet radio station from your Roon library, with its cover on the key. In the key's settings, choose the kind of music and type part of its name to find it. Press to **Play Now**, **Shuffle**, **Add Next**, **Queue** or **Start Radio**, as you choose. A ring shows while it's playing (albums, artists and stations). |
| **Album Roulette** | A random album from your library, with its cover. Press to play it; press and hold for another one. |
| **Up Next** | The next track in the zone's queue (or the one after, up to +5), with its cover. Press to play from that track on. Put a few side by side to see what's coming. |
| **Sleep Timer** | Press to start: at the **end of this track**, then press again for **15, 30, 60 or 90 minutes** (you can set your own times), then off. Press and hold to stop it. The key counts down. When it's time, the music fades out and the zone pauses (or every zone pauses, or the audio devices go into standby), and the volume goes back for next time. It keeps running while you use other pages, but not if Stream Deck or the computer restarts. |
| **Transport** | One key for play/pause, play, pause, stop, next, previous, shuffle, repeat (off, all, one) or Roon Radio. The key shows the zone's state, and dims when Roon says the control isn't available. What can't be paused, such as live radio, is stopped instead. |
| **Now Playing** | The album art (or the title and artist) of what the zone is playing, with a progress bar and a pause sign while paused, and optionally the time played, the time left or the track's length. Press for play/pause or the next track. Or **one big cover** over a block of keys (up to 5 × 3): put a Now Playing key on each, choose the same size, and give each key its number. |
| **Volume** | Volume up, down, a set level, or mute, with the level on the key (in dB or 0–100, as Roon shows it). For a grouped zone, every zone in it moves together by its own step, or choose one zone only. Hold up or down to keep going. Set a **Limit** so the key never goes above a level. Audio devices with fixed volume show **Fixed**; amplifiers with only + and − get + and −. |
| **Zone** | **Switch the active zone** (press for the next one; its settings list every zone on your Roon Core, and you can tick the ones to switch between), or **make a zone active** (one key per zone: the active one has a ring). |
| **Transfer** | Roon's **Transfer Zone**. **Transfer to this zone**: press to move what's playing (track, queue and radio) there; it becomes the active zone and has a ring. **Transfer to the next zone**: press to step the music through your zones. |
| **Group** | Roon's **Group**: press to group this zone with the active zone, so they play together; press again to **ungroup** it. Dimmed when Roon can't group the two (only zones of the same kind can, e.g. AirPlay with AirPlay). |
| **Roon Dial** (Stream Deck +) | **Up next** (turn through the tracks coming up, press to play from one, touch for the next track), **browse the library** (turn through playlists, albums, artists, genres, composers or radio stations with their covers, faster when you turn fast; press to play, touch to add next, touch and hold for the next list; albums sorted by album title, artist or random), **volume** (turn; press to mute; touch for play/pause), **move through the track** (turn; Roon jumps there when you stop), **previous / next track**, **pick the active zone**, or **transfer** (turn to a zone, press to transfer the music there, touch to group or ungroup it). The touch strip shows the album art, the title and a bar. |
| **Power** | Switch the zone's amplifier or DAC **on** (and to the right input) or into **standby**, for audio devices Roon can control. Or **pause every zone**, or **mute every zone** (press again to unmute). |

Each key is for the **Active zone** (the default: the zone a Zone key picked, or whatever is playing until you pick one), **Whatever is playing**, or one zone.

## Good to know

- **It uses Roon's official extension API** on your own network. There is no account sign-in and nothing goes through the cloud.
- **Hold Next or Previous** to move through the track instead of skipping.
- **Power needs an audio device Roon can control:** in Roon, Settings → Audio → the device's settings (Device Setup) → "Standby" and "Convenience switch". Otherwise the key says **No control**.
- **Grouping zones doesn't break keys:** a key set to a zone still finds it once it's in a grouped zone, and then shows the grouped zone.

## Troubleshooting

- **"Enable in Roon" on the keys:** in Roon, open Settings → Extensions and click Enable next to "Remote for Roon (Stream Deck)".
- **"No Core":** the plugin hasn't found a Roon Core. Check that Roon is running and on the same network, click **Search again** in a key's settings, or type the Core's IP address in **Address**.
- **"Core off":** the Roon Core stopped answering. Keys come back on their own when it does.
- **"Pick a zone":** a Zone key set to make a zone active, a Transfer key set to transfer to this zone, or a Group key needs a zone: choose it in the key's settings.
- **"Limit" on a volume key:** the key's limit is reached. Change it in the key's settings.
- **"Zone off":** the key's zone isn't available in Roon right now (its audio device is switched off, or disabled in Roon's audio settings).
- **Your computer asks whether to allow network access:** choose **Allow** so the plugin can find your Roon Core on your local network.

When reporting a bug, attach the latest log from:

- **macOS:** `~/Library/Application Support/com.elgato.StreamDeck/Plugins/com.johnlee.roonremote.sdPlugin/logs/`
- **Windows:** `%APPDATA%\Elgato\StreamDeck\Plugins\com.johnlee.roonremote.sdPlugin\logs\`

The log doesn't include Roon's token.

## Privacy

The plugin collects no personal data. It connects only to the Roon Core on your own network. See the [Privacy Policy](PRIVACY.md).

## Trademarks

Roon is a trademark of Roon Labs LLC. This plugin is not affiliated with, sponsored by, or endorsed by Roon Labs LLC. Other names are trademarks of their respective owners.

## Open-source software

The plugin uses the Roon API libraries by Roon Labs LLC (Apache License 2.0) and other open-source software; see `THIRD_PARTY_NOTICES.txt` inside the plugin.
