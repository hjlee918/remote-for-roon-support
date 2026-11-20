# Remote for Roon

Support page for **Remote for Roon**, a Stream Deck plugin for Roon, the music player from Roon Labs: an active zone your keys follow, moving music between rooms, grouping, switching your amplifier on, playback and volume keys that show what's happening, and what's playing with its album art and progress. The plugin is in development and not on the Elgato Marketplace yet.

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
3. In the key's settings, choose what the key does. Keys follow the **active zone** unless you choose a room. Add a **Zone** key to switch the active zone. Add more keys; they all share the connection.

The plugin finds your Roon Core on its own. If it doesn't, type the Core's IP address in **Address** and click **Add**.

**More than one Roon Core?** Each key then has a **Core** menu; enable the extension on each Core you want to use.

## The actions

| Action | What it does |
|---|---|
| **Transport** | One key for play/pause, play, pause, stop, next, previous, shuffle, repeat (off, all, one) or Roon Radio. The key shows the zone's state, and dims when Roon says the control isn't available. What can't be paused, such as live radio, is stopped instead. |
| **Now Playing** | The album art (or the title and artist) of what the zone is playing, with a progress bar and a pause sign while paused, and optionally the time played, the time left or the track's length. Press for play/pause or the next track. |
| **Volume** | Volume up, down, a set level, or mute, with the level on the key (in dB or 0–100, as Roon shows it). For a group, every speaker moves together by its own step, or choose one room only. Hold up or down to keep going. Set a **Limit** so the key never goes above a level. Devices with fixed volume show **Fixed**; amplifiers with only + and − get + and −. |
| **Zone** | **Switch the active zone** (press for the next one; its settings list every zone on your Roon Core, and you can tick the ones to switch between), or **make a room active** (one key per room: the active one has a ring). |
| **Output** | Choose the **device the music plays on**. **Play on this device**: press to move what's playing there (one key per device: the one playing has a ring). **Move to the next device**: press to step the music through your devices. **Group this device** with the active zone, so they play together (press again to take it out). |
| **Roon Dial** (Stream Deck +) | **Volume** (turn; press to mute; touch for play/pause), **move through the track** (turn; Roon jumps there when you stop), **previous / next track**, **pick the active zone**, or **choose the output device** (turn to a device, press to play there, touch to group it). The touch strip shows the album art, the title and a bar. |
| **Power** | Switch the zone's amplifier or DAC **on** (and to the right input) or into **standby**, for devices Roon can control. Or **pause every zone**, or **mute every zone** (press again to unmute). |

Each key is for the **Active zone** (the default: the zone a Zone key picked, or whatever is playing until you pick one), **Whatever is playing**, or one room.

## Good to know

- **It uses Roon's official extension API** on your own network. There is no account sign-in and nothing goes through the cloud.
- **Hold Next or Previous** to move through the track instead of skipping.
- **Power needs a device Roon can control:** in Roon, Settings → Audio → the device's settings (Device Setup) → "Standby" and "Convenience switch". Otherwise the key says **No control**.
- **Grouping zones doesn't break keys:** a key remembers the audio device you chose and follows whichever zone that device is in.

## Troubleshooting

- **"Enable in Roon" on the keys:** in Roon, open Settings → Extensions and click Enable next to "Remote for Roon (Stream Deck)".
- **"No Core":** the plugin hasn't found a Roon Core. Check that Roon is running and on the same network, click **Search again** in a key's settings, or type the Core's IP address in **Address**.
- **"Core off":** the Roon Core stopped answering. Keys come back on their own when it does.
- **"Pick a room" / "Pick a device":** a Zone key set to make a room active, or an Output key set to play on a device or group it, needs one: choose it in the key's settings.
- **"Limit" on a volume key:** the key's limit is reached. Change it in the key's settings.
- **"Zone off":** the key's audio device isn't available in Roon right now (switched off, or disabled in Roon's audio settings).
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
