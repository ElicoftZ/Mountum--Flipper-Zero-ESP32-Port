# Credits and Attribution

This firmware is a **fork of a fork**. The overwhelming majority of it was written by
other people, and this document exists to say exactly who wrote what.

Provenance below was established mechanically, not by guesswork: every entry was checked
for presence in [Sor3nt's ESP32 port](https://github.com/Sor3nt/Flipper-Zero-ESP32-Port)
and in [Momentum Firmware](https://github.com/Next-Flip/Momentum-Firmware). Anything
present in either tree is **not** original to this fork and is listed in Part 1.

---

# Part 1 — Not written by this fork

## 1.1 Foundation layers

| Project | Author | Role here | License |
|---|---|---|---|
| [Flipper Zero firmware](https://github.com/flipperdevices/flipperzero-firmware) | Flipper Devices Inc. | Furi OS, GUI, services, app framework — everything derives from this | GPLv3 |
| [Momentum Firmware](https://github.com/Next-Flip/Momentum-Firmware) | The Momentum team | Custom-firmware feature set: dolphin, passport, settings, menu styles, asset packs | GPLv3 |
| [Flipper-Zero-ESP32-Port](https://github.com/Sor3nt/Flipper-Zero-ESP32-Port) | **Sor3nt** | The ESP32 / ESP-IDF port this repository is forked from — HAL, board bring-up, web flasher, wireless tooling, OTA and SD update | — |
| [ESP-IDF](https://github.com/espressif/esp-idf) | Espressif Systems | SDK and toolchain | Apache-2.0 |

> Everything in sections 1.2–1.4 reached this repository **through Sor3nt's port**. Where an
> app had an earlier original author, both are named.

## 1.2 Applications inherited via the Sor3nt port

Present in Sor3nt's tree — **not** written here.

| App | Original author / project | License |
|---|---|---|
| archive, bad_usb, clock_app, gpio, ibutton, infrared, lfrfid, nfc, onewire, subghz | Flipper Devices (OFW) | GPLv3 |
| u2f | Flipper Devices / Momentum (CTAP2 additions) | GPLv3 |
| wlan_app, esp_now, nrf24 | **Sor3nt** — ESP32 wireless tooling | — |
| ble_spam | includes **WhisperPair** by [zalexdev](https://github.com/zalexdev/wpair-app) | Apache-2.0 (WhisperPair) |
| doom | **doomgeneric** by [ozkl](https://github.com/ozkl/doomgeneric); id Software | GPLv2 |
| wolf3d | **Wolf4SDL** by Moritz Kroll; id Software | GPL |
| streaming | **Helix** decoder by RealNetworks | RPSL / RCSL |
| subghz_remote | **DarkFlippers** — [@gid9798](https://github.com/gid9798), [@xMasterX](https://github.com/xMasterX) | MIT |

## 1.3 Community apps inherited via the Sor3nt port

All present in Sor3nt's tree. Authors as declared in each app's `application.fam`,
`LICENSE` or source headers.

| App | Author | Upstream | License |
|---|---|---|---|
| FindMyFlipper | [@MatthewKuKanich](https://github.com/MatthewKuKanich) | [FindMyFlipper](https://github.com/MatthewKuKanich/FindMyFlipper) | see upstream |
| TagTinker | i12bp8 | — | GPLv3 |
| flipper-zero_authenticator | Alexander Kopachov ([@akopachov](https://github.com/akopachov)) | [repo](https://github.com/akopachov/flipper-zero_authenticator) | GPLv3 |
| flipper_xremote | [@kala13x](https://github.com/kala13x) | [flipper-xremote](https://github.com/kala13x/flipper-xremote) | GPLv3 |
| protopirate | The Pirates' Plunder | [protopirate.net](https://protopirate.net/ProtoPirate) | GPLv3 |
| wmbuster | wm-buster / i12bp8 | [wmbuster](https://github.com/i12bp8/wmbuster) | GPLv3 |
| tamagotchi_p1 | cyanic (app); **tamalib** by Jean-Christophe Rona | [repo](https://github.com/GMMan/flipperzero-tamagotch-p1) | GPLv2 (tamalib) |
| blackjack, blackjack_split | Tibor Tálosi | — | MIT |
| asteroids | Salvatore Sanfilippo | — | see source header |
| pong | nmrr | [github.com/nmrr](https://github.com/nmrr) | CC0-1.0 |
| dice | [@Ka3u6y6a](https://github.com/Ka3u6y6a) | [flipper-zero-dice](https://github.com/Ka3u6y6a/flipper-zero-dice) | see upstream |
| snake20 | [@Willzvul](https://github.com/Willzvul) | [Snake_2.0](https://github.com/Willzvul/Snake_2.0) | see upstream |
| mifare_fuzzer | [@spheeere98](https://github.com/spheeere98), @Sil333033 | [mifare_fuzzer](https://github.com/spheeere98/mifare_fuzzer) | see upstream |
| nRF24_jammer | W0rthlessS0ul | [FZ_nRF24_jammer](https://github.com/W0rthlessS0ul/FZ_nRF24_jammer) | see upstream |
| nfc_rfid_detector | SkorP | — | see upstream |
| reverse_shell, rfid2_reader | cardputer | — | see upstream |
| roulette | Superagent | — | see upstream |
| game15, nfc_magic, t_embed_snake, tetris, texas_holdem, weather_station | **author not declared in-tree** | — | unknown |

## 1.4 Bundled libraries

| Library | Author | Used for | License |
|---|---|---|---|
| libsmb2 | [sahlberg](https://github.com/sahlberg/libsmb2) | SMB2/3 client | LGPL-2.1 |
| mJS | [Cesanta](https://github.com/cesanta/mjs) | JavaScript runner | Apache-2.0 |
| heatshrink | [Atomic Object](https://github.com/atomicobject/heatshrink) | compression | ISC |
| Helix | RealNetworks | MP3 decoding | RPSL / RCSL |
| doomgeneric | [ozkl](https://github.com/ozkl/doomgeneric) | Doom | GPLv2 |
| Wolf4SDL | Moritz Kroll / id Software | Wolfenstein 3D | GPL |
| tamalib | Jean-Christophe Rona | Tamagotchi emulation | GPLv2 |
| u8g2, nanopb, mlib | respective upstreams | display, protobuf, containers | see each |
| **Hotspot Arcade** | [tarikbc](https://github.com/tarikbc/hotspot-arcade) | arcade app | MIT |

> **Hotspot Arcade** was added in this fork, but the game itself is tarikbc's work.
> Only the ESP-IDF integration around it (`components/hotspot_arcade_*`) is original here.

## 1.5 Momentum components carried over

`momentum_app`, `lib/momentum`, `components/momentum` — present in Momentum Firmware.
The Momentum settings app, settings core, asset-pack loader and PNG icon decoder are
**Momentum's work**, adapted to ESP-IDF. See [NOTICE_MOMENTUM_PORT.md](NOTICE_MOMENTUM_PORT.md).

---

# Part 2 — Original to this fork

Absent from **both** Sor3nt's port and Momentum Firmware. Written for the
LilyGo T-Embed CC1101 by **[ElicoftZ](https://github.com/ElicoftZ)**.

## 2.1 Applications

| App | What it does |
|---|---|
| **Dual Boot** | Install and switch between multiple firmwares from a boot menu, with a side-button recovery escape hatch. Dynamic partition allocation with interrupted-update recovery. |
| **Power Profiler** | Live power-draw trace from the BQ27220 fuel gauge. |
| **Wardriving** | Passive WiFi + BLE + Sub-GHz logger to PSRAM. |
| **BLE Detector** | Rapid Bluetooth device scanning and profiling, with unbounded scan lists. |

## 2.2 System components

| Component | What it does |
|---|---|
| `components/multiboot` | Dynamic multi-boot partition layout, table staging and bootloader-side recovery of interrupted updates. |
| `components/nimble_glue` | NimBLE host integration for the port. |
| `applications/settings/backup_settings` | Settings backup / restore. |
| `components/hotspot_arcade_runtime`, `components/hotspot_arcade_service` | ESP-IDF integration for Hotspot Arcade (the game itself is tarikbc's — see 1.4). |
| `applications/main/mp3_player` | I2S playback glue (the Helix decoder is RealNetworks' — see 1.4). |

## 2.3 Microphone and audio tools

Added 2026-08-18. No upstream equivalent in either tree.

`mic_common`, `mic_level`, `mic_logger`, `mic_sonar`, `mic_waterfall`, `tone_gen`,
`ultrasonic`, `voice_notes`

---

## Unconfirmed

- **`macro_pad`** — present in neither Sor3nt's nor Momentum's tree, but carries no author
  header and nothing T-Embed-specific. Origin not established; **not claimed here** pending
  confirmation.
- Several inherited community apps (1.3) ship no `LICENSE` file. Their terms must be taken
  from their upstream repositories before redistribution.
- No Momentum asset-pack artwork is redistributed here. If you add asset packs, preserve
  each asset's own license and attribution.
