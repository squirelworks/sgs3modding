# C++ Header Dump Notes

The dump includes a large CXX header export (UE4SS-style) for Unreal Engine 5.7.4 + the ShipGraveyard3 game module.

## Location

`CXXHeaderDump/` contains ~1,175 `.hpp` files covering:
- Engine modules (Engine, CoreUObject, AIModule, AnimGraphRuntime, ControlRig, Niagara, PCG, UMG, etc.)
- Game module: `ShipGraveyard3.hpp` + `ShipGraveyard3_enums.hpp`
- Animation blueprints (ABP_*), AI controllers (AIC_*), etc.

`Engine.hpp` was the largest and was removed for size; the game-specific and remaining engine headers are retained in the original dump.

## Key Game Structs (from ShipGraveyard3.hpp)

Examples of important reflected types:

- `FAIWorker` — Worker name, icon, cost, `EWorkerType`
- `FAIWorkerTask` — Task validity, point of interest, actor target, worker type
- `FActiveResourceMarketEvent` — Market events affecting resource types
- `FActorSaveData` — Actor class, transform, custom data, unique ID, color
- `FCharacterPlayerData` — Character selection / preset
- Contract-related types referenced by data tables (`ContractBaseData`, gameplay tags like `ShipContract.*`)
- Resource / prop systems (`PropType` enum, resource market config)

Other notable files:
- `ShipGraveyard3.hpp` — Main game structs and UCLASS/USTRUCT definitions
- Animation BPs: `ABP_ShipThirdPerson.hpp`, `ABP_ArmsShipAnimBP.hpp`
- AI: `AIC_Npc.hpp`, `AIC_Worker_Base.hpp`

## Usage for Modding

- Use the headers to understand reflected properties, enum values, and class hierarchies when writing Blueprint mods, UE4SS scripts, or custom C++ plugins.
- Data table row structs (e.g. `ContractBaseData`) are defined here and populated in the JSON `DT_*.json` exports.
- Enums such as `EWorkerType`, `PropType`, resource types drive the salvage and contract systems.

## Engine Version

Unreal Engine 5.7.4 (Release-5.7). Mapping files (`.usmap` / `.jmap`) were generated from the Shipping executable and used for the dump but have been removed from the lightweight workspace.

For full header browsing, refer to the original FModel / UE4SS CXXHeaderDump output.