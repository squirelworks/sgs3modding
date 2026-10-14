# Asset & Content Structure

Overview of the extracted content hierarchy from the ShipGraveyard3 FModel / pak-JSON dump (UE 5.7.4).

## Local Extracted Paths (this dump)

```
ShipGraveyard3/
└── Content/
    └── Blueprints/
        ├── Contracts/
        │   └── Data/                  # Ship resource assets (AD_*), contract data tables (DT_*), DA_Contract_*
        │       └── ContractDataAssets/
        ├── Core/                      # Managers: Resource, Initialization, Level, Coop, Warehouse, Computer, RampVehicle, Preload
        ├── Data/                      # Shared data tables: Levels, Liftables, MapMarkers, SubContract, Market, structs (S_*)
        │   └── Market/
        ├── NPC/
        │   ├── Actions/               # NPC behavior actions (BackToWork, ChangeVisibility, StopWork, etc.)
        │   └── ShowaStation/
        ├── Tool/                      # Tool blueprints (Torch, TemporaryTool, etc.)
        ├── ToolsData/                 # Tool data by type
        │   ├── Gloves/
        │   ├── Hammer/
        │   ├── Rope/
        │   ├── Saw/
        │   ├── ToolBox/
        │   └── Torch/
        └── WareHouse/
            └── Upgrades/
```

## Original Pak Tree (excerpt)

The full Windows `tree` listing of the pak-JSON extraction showed standard UE structure under `pak-JSON/`:

- Engine/ (Config, Content/Localization, Plugins: AI, Animation, Audio, etc.)
- Game content under the main package (Blueprints, Assets, Maps, etc.)

Key game modules visible in headers and paths:
- ShipGraveyard3 (main game module)
- Standard UE5 plugins (ControlRig, Niagara, PCG, IKRig, GeometryCollection, etc.)

## Maps

- `Content/Maps/Tutorial_Ship.umap` was present in the original dump (large binary) but removed for size.
- Other ship maps are referenced via contract / level data tables (`DT_Levels`, `S_LevelData`, etc.).

## Data Tables of Interest

- `DT_Contracts` — Gameplay tags for contracts / quests
- `DT_Fletcher`, `DT_GrafSpee`, `DT_JarleBerg`, `DT_Liberty_Ship`, `DT_Project1124`, `DT_Soya`, `DT_Tutorial_Ship`, `DT_Uboat` — Per-ship contract rows (`ContractBaseData`)
- `DT_Levels`, `DT_Liftables`, `DT_MapMarkers`, `DT_SubContract`
- Market: `DA_ResourceMarketConfig`

## Managers & Core Systems

Exported blueprints indicate systems for:
- Resource management (`BP_ResourceManager`)
- Initialization / level loading (`BP_InitializationManager`, `BP_LevelManager`, `BP_PreloadManager`)
- Coop (`BP_CoopManager`)
- Warehouse / computer interfaces
- Ramp vehicles

This structure is typical of a UE5 game using Data Assets + Data Tables for content-driven contracts and a Blueprint-heavy gameplay layer on top of C++ game module classes.