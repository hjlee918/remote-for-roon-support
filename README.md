# Remote for Roon

Support page for **Remote for Roon**, a Stream Deck plugin for Roon, the music player from Roon Labs: playback keys for any zone that show the zone's state, and what's playing with its album art and progress. The plugin is in development and not on the Elgato Marketplace yet.

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
3. In the key's settings, choose the zone and what the key does. Add more keys; they all share the connection.

The plugin finds your Roon Core on its own. If it doesn't, type the Core's IP address in **Address** and click **Add**.

**More than one Roon Core?** Each key then has a **Core** menu; enable the extension on each Core you want to use.

## The actions

| Action | What it does |
|---|---|
| **Transport** | One key for play/pause, play, pause, stop, next, previous, shuffle, repeat (off, all, one) or Roon Radio. The key shows the zone's state, and dims when Roon says the control isn't available. What can't be paused, such as live radio, is stopped instead. |
| **Now Playing** | The album art of what the zone is playing, with a progress bar and a pause sign while paused. Press for play/pause or the next track. |

Each key is for one zone, or for **Whatever is playing**.

## Good to know

- **It uses Roon's official extension API** on your own network. There is no account sign-in and nothing goes through the cloud.
- **Grouping zones doesn't break keys:** a key remembers the audio device you chose and follows whichever zone that device is in.

## Troubleshooting

- **"Enable in Roon" on the keys:** in Roon, open Settings → Extensions and click Enable next to "Remote for Roon (Stream Deck)".
- **"No Core":** the plugin hasn't found a Roon Core. Check that Roon is running and on the same network, click **Search again** in a key's settings, or type the Core's IP address in **Address**.
- **"Core off":** the Roon Core stopped answering. Keys come back on their own when it does.
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
