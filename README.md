# ShipGraveyard3 Modding Documentation

Documentation and reverse-engineered data for **ShipGraveyard3** (SGS3), an Unreal Engine 5.7.4 IoStore game focused on shipbreaking / scrapyard contracts.

This repository collects findings from FModel dumps of the Shipping build (UE 5.7.4, build ~51494982).

## Game Overview

Players take contracts to dismantle ships (military, cargo, research, etc.), recover resources, manage NPCs/workers, use tools, and sell materials. Ships include historical / fictional vessels:

- Fletcher (USS Fletcher-style destroyer)
- GrafSpee (Admiral Graf Spee)
- Jarle Berg
- Liberty Ship
- Project 1124 (P1124)
- Soya / Soya Arctic
- Tutorial Ship
- U-boat

## Dump Sources

- CXX header dump (UE4SS / FModel style) — classes, structs, enums for the game module and engine.
- Exported JSON blueprints and data assets from `/Game/Blueprints/...`
- Directory tree of the pak-JSON extraction.

Large binary dumps (`.jmap`, `.usmap`, `.umap`) were removed to keep the workspace light; structured data remains.

## Repository Structure

- `docs/SHIPS.md` — Per-ship resource / prop inventories extracted from `AD_*.json` data assets.
- `docs/ASSET_STRUCTURE.md` — Overview of the Blueprint / Content hierarchy.
- `docs/HEADERS.md` — Notes on the C++ header dump and key game structs.
- `docs/BLUEPRINTS.md` — Categories of exported blueprints and data tables.

## Contributing / Further Research

- Full JSON exports and headers are available from the original dump process.
- Useful for modding: resource types, contract tags, NPC actions, tool data, market configs.
- Engine version: Unreal Engine 5.7.4.

See the `docs/` folder for detailed findings.