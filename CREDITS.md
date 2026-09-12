# Feature Origin — Merged vs Written Here

This document answers one question for every feature in this fork:
**did it come from the merge, or was it written here?**

Nothing below is a guess. Every directory was tested for presence in
[Sor3nt's ESP32 port](https://github.com/Sor3nt/Flipper-Zero-ESP32-Port) and in
[Momentum Firmware](https://github.com/Next-Flip/Momentum-Firmware). Presence in either
tree means it was **merged**, not written here.

| Bucket | Meaning |
|---|---|
| **Part 1 — Merged** | Came from Sor3nt's port (or from OFW/Momentum through it). Not my work. |
| **Part 2 — Brought over from Momentum** | Not from Sor3nt's port, but not mine either — Momentum's code, added here. |
| **Part 3 — Written here** | Exists in neither tree. Original to this fork. |

---

# Part 1 — Merged (not my work)

## 1.1 The foundation

| Project | Author | What it provides |
|---|---|---|
| [Flipper-Zero-ESP32-Port](https://github.com/Sor3nt/Flipper-Zero-ESP32-Port) | **Sor3nt** | The port this fork is built on — ESP32/ESP-IDF HAL, board bring-up, web flasher, wireless tooling, OTA and SD update |
| [Flipper Zero firmware](https://github.com/flipperdevices/flipperzero-firmware) | Flipper Devices Inc. | Furi OS, GUI, services, app framework (GPLv3) |
| [ESP-IDF](https://github.com/espressif/esp-idf) | Espressif Systems | SDK and toolchain (Apache-2.0) |

## 1.2 Applications that came with the port

Present in Sor3nt's tree — **merged, not written here**.

`archive` · `bad_usb` · `ble_spam` · `clock_app` · `doom` · `esp_now` · `gpio` ·
`ibutton` · `infrared` · `lfrfid` · `nfc` · `nrf24` · `onewire` · `streaming` ·
`subghz` · `subghz_remote` · `u2f` · `wlan_app` · `wolf3d`

Where those apps embed someone else's project:

| App | Embedded work | Author | License |
|---|---|---|---|
| `wlan_app`, `esp_now`, `nrf24` | ESP32 wireless tooling | **Sor3nt** | — |
| `ble_spam` | WhisperPair | [zalexdev](https://github.com/zalexdev/wpair-app) | Apache-2.0 |
| `doom` | doomgeneric | [ozkl](https://github.com/ozkl/doomgeneric) / id Software | GPLv2 |
| `wolf3d` | Wolf4SDL | Moritz Kroll / id Software | GPL |
| `streaming` | Helix decoder | RealNetworks | RPSL / RCSL |
| `subghz_remote` | SubGHz Remote | DarkFlippers — [@gid9798](https://github.com/gid9798), [@xMasterX](https://github.com/xMasterX) | MIT |

## 1.3 Community apps that came with the port

All present in Sor3nt's tree. Authors as declared in each app's own `application.fam`,
`LICENSE` or source header.

| App | Author | Upstream | License |
|---|---|---|---|
| FindMyFlipper | [@MatthewKuKanich](https://github.com/MatthewKuKanich) | [FindMyFlipper](https://github.com/MatthewKuKanich/FindMyFlipper) | see upstream |
| TagTinker | i12bp8 | — | GPLv3 |
| flipper-zero_authenticator | Alexander Kopachov ([@akopachov](https://github.com/akopachov)) | [repo](https://github.com/akopachov/flipper-zero_authenticator) | GPLv3 |
| flipper_xremote | [@kala13x](https://github.com/kala13x) | [flipper-xremote](https://github.com/kala13x/flipper-xremote) | GPLv3 |
| protopirate | The Pirates' Plunder | [protopirate.net](https://protopirate.net/ProtoPirate) | GPLv3 |
| wmbuster | wm-buster / i12bp8 | [wmbuster](https://github.com/i12bp8/wmbuster) | GPLv3 |
| tamagotchi_p1 | cyanic; tamalib by Jean-Christophe Rona | [repo](https://github.com/GMMan/flipperzero-tamagotch-p1) | GPLv2 |
| blackjack, blackjack_split | Tibor Tálosi | — | MIT |
| asteroids | Salvatore Sanfilippo | — | see source |
| pong | nmrr | [github.com/nmrr](https://github.com/nmrr) | CC0-1.0 |
| dice | [@Ka3u6y6a](https://github.com/Ka3u6y6a) | [flipper-zero-dice](https://github.com/Ka3u6y6a/flipper-zero-dice) | see upstream |
| snake20 | [@Willzvul](https://github.com/Willzvul) | [Snake_2.0](https://github.com/Willzvul/Snake_2.0) | see upstream |
| mifare_fuzzer | [@spheeere98](https://github.com/spheeere98), @Sil333033 | [mifare_fuzzer](https://github.com/spheeere98/mifare_fuzzer) | see upstream |
| nRF24_jammer | W0rthlessS0ul | [FZ_nRF24_jammer](https://github.com/W0rthlessS0ul/FZ_nRF24_jammer) | see upstream |
| nfc_rfid_detector | SkorP | — | see upstream |
| reverse_shell, rfid2_reader | cardputer | — | see upstream |
| roulette | Superagent | — | see upstream |
| game15, nfc_magic, t_embed_snake, tetris, texas_holdem, weather_station | not declared in-tree | — | unknown |

## 1.4 Libraries that came with the port

libsmb2 (LGPL-2.1, [sahlberg](https://github.com/sahlberg/libsmb2)) · mJS (Apache-2.0,
[Cesanta](https://github.com/cesanta/mjs)) · heatshrink (ISC,
[Atomic Object](https://github.com/atomicobject/heatshrink)) · u8g2 · nanopb · mlib

---

# Part 2 — Brought over from Momentum (not mine, not from the port)

Present in Momentum Firmware, absent from Sor3nt's port. **The Momentum team's work**,
adapted to ESP-IDF here.

| Item | What it is |
|---|---|
| `momentum_app` | The Momentum settings application |
| `lib/momentum`, `components/momentum` | Settings core, asset-pack loader, PNG icon decoder |

The wider Momentum feature set (dolphin levels, passport, menu styles, lockscreen)
also originates here. See [NOTICE_MOMENTUM_PORT.md](NOTICE_MOMENTUM_PORT.md). Licensed GPLv3.

---

# Part 3 — Written here

Absent from **both** Sor3nt's port and Momentum Firmware. Written for the
LilyGo T-Embed CC1101 by **[ElicoftZ](https://github.com/ElicoftZ)**.

## 3.1 Applications

| App | What it does |
|---|---|
| **Dual Boot** | Install and switch between multiple firmwares from a boot menu, with a side-button recovery escape hatch. Dynamic partition allocation, and recovery of an interrupted table update. |
| **Power Profiler** | Live power-draw trace from the BQ27220 fuel gauge. |
| **Wardriving** | Passive WiFi + BLE + Sub-GHz logger to PSRAM. |
| **BLE Detector** | Rapid Bluetooth scanning and profiling, with unbounded scan lists. |

## 3.2 System components

| Component | What it does |
|---|---|
| `components/multiboot` | Dynamic multi-boot partition layout, staged table writes, bootloader-side recovery of an interrupted update. |
| `components/nimble_glue` | NimBLE host integration. |
| `applications/settings/backup_settings` | Settings backup and restore. |

## 3.3 Microphone and audio tools

`mic_common` · `mic_level` · `mic_logger` · `mic_sonar` · `mic_waterfall` ·
`tone_gen` · `ultrasonic` · `voice_notes`

## 3.4 Integration only — the code inside is someone else's

Added here, but **not my code**. Only the ESP-IDF plumbing around it is.

| Item | Whose work it is | License |
|---|---|---|
| `hotspot_arcade` + `components/hotspot_arcade_runtime` / `_service` | [tarikbc](https://github.com/tarikbc/hotspot-arcade) | MIT |
| `applications/main/mp3_player` | Helix decoder — RealNetworks (only the I2S glue is mine) | RPSL / RCSL |

---

## Unconfirmed

- **`macro_pad`** — in neither tree, but carries no author header and nothing
  T-Embed-specific. Origin not established, so it is **not claimed here**.
- Several merged community apps (1.3) ship no `LICENSE` file; their terms must be taken
  from their upstream repositories.
- No Momentum asset-pack artwork is redistributed here.
