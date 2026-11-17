# Privacy Policy

**Remote for Roon** (Stream Deck plugin), published by Artifex.
Effective date: November 16, 2026.

## Summary

The plugin does not collect, sell, or share personal data. It sends nothing to us. It talks only to the Roon Core (Roon Server) on your own network.

## What the plugin stores, and where

The plugin saves the following in Stream Deck's settings on your computer:

- The **token** your Roon Core gives the plugin when you click Enable in Roon (Settings → Extensions). It lets the plugin connect again without asking. It is sent only to that Roon Core.
- Each Roon Core you enabled or added: its name, identifier, version and address on your network.
- What you chose for each key, for example which zone it controls.

The plugin never asks for, sees or stores your Roon account's email or password.

To delete them, uninstall the plugin. You can also remove the plugin's access in Roon: Settings → Extensions.

## Network use

- **Finding your Roon Core:** the plugin sends Roon's standard discovery message on your local network.
- **While the plugin runs,** it keeps a connection open to each Roon Core it found, to hear about your zones and what they play as it happens (titles, artists, positions, volume), and it downloads album art from the Core for the keys.
- **Pressing a key** sends that command (play, pause, next and so on) to your Roon Core.

The plugin contains no analytics, tracking, or advertising, and uses no server of ours. It does not connect to Roon Labs or to any streaming service.

## Logs

Stream Deck keeps a plugin log on your computer to help diagnose problems:

- macOS: `~/Library/Application Support/com.elgato.StreamDeck/Plugins/com.johnlee.roonremote.sdPlugin/logs/`
- Windows: `%APPDATA%\Elgato\StreamDeck\Plugins\com.johnlee.roonremote.sdPlugin\logs\`

The log can include your Roon Core's name and address, zone names, and messages about commands that failed. It never includes the token or what you listen to. The log stays on your computer unless you choose to share it.

## Support requests

If you open an issue in this repository, the issue and anything you attach to it (such as a log) are **public on GitHub** and subject to [GitHub's Privacy Statement](https://docs.github.com/site-policy/privacy-policies/github-general-privacy-statement). Remove anything you don't want to share before posting.

## Roon and purchases

Roon and your Roon account are provided by Roon Labs, under Roon's own terms and privacy policy. Purchases on the Elgato Marketplace are handled by Elgato (Corsair) and its payment processor, Stripe. We do not receive your payment details. Elgato's privacy policy and [Stripe's Privacy Policy](https://stripe.com/privacy) describe how they handle your data.

## Changes

If this policy changes, the updated version will be posted here with a new effective date.

## Contact

Questions about this policy: [open an issue](https://github.com/hjlee918/remote-for-roon-support/issues).
