# Exported Blueprints & Data

Summary of the 116 JSON-exported assets under `ShipGraveyard3/Content/Blueprints/`.

## Contracts & Ships

- **Resource assets**: `AD_Fletcher.json`, `AD_GrafSpee.json`, `AD_JarleBerg.json`, `AD_Liberty_Ship.json`, `AD_Project1124.json`, `AD_Soya.json`, `AD_Soya_Artic.json`, `AD_Tutorial_Ship.json`, `AD_Uboat.json`  
  Type: `DA_ShipResources_C` — prop counts per ship (see `SHIPS.md`).

- **Contract data tables**: `DT_Fletcher.json`, `DT_GrafSpee.json`, `DT_JarleBerg.json`, `DT_Liberty_Ship.json`, `DT_Project1124.json`, `DT_Soya.json`, `DT_Tutorial_Ship.json`, `DT_Uboat.json`, `DT_Contracts.json`, `DT_TestingContracts.json`  
  Rows use `ContractBaseData` with tags such as `ShipContract.Fletcher.1`, customer text, portraits, etc.

- **Contract Data Assets**: `DA_Contract_Fletcher.json`, `DA_Contract_P1124.json`, `DA_Contract_Soya.json`, `DA_Contract_Tutorial.json`

- Shared: `DA_ShipResources.json`, `DT_ContractsTag.json`

## Core Systems

- `BP_ResourceManager.json`
- `BP_InitializationManager.json` (+ departure map variant for Soya)
- `BP_LevelManager.json`
- `BP_PreloadManager.json`
- `BP_CoopManager.json`
- `BP_Computer.json`, `BP_WarehouseComputer.json`
- `BP_RampVehicle.json`

## Data Tables & Structs

- `DT_Levels.json`, `DT_Liftables.json`, `DT_MapMarkers.json`, `DT_SubContract.json`
- `S_LevelData.json`, `S_MapMarkers.json`, `S_DecalData.json`
- Market: `DA_ResourceMarketConfig.json`

## NPCs

- Base: `BP_Npc_Base.json`, `BP_NPC_CommonNPC.json`, `BP_NPC_CommonNPC_NotMovable.json`, `BP_Npc_Buyer.json`
- Actions: `BPNA_BackToWork.json`, `BPNA_ChangeNpcVisibility.json`, `BPNA_StopWork.json`
- Station-specific under `NPC/ShowaStation/`

## Tools

- Blueprints under `Tool/` (e.g. Torch, TemporaryTool)
- Data under `ToolsData/` organized by tool type: Gloves, Hammer, Rope, Saw, ToolBox, Torch

## Warehouse

- Under `WareHouse/` and `WareHouse/Upgrades/`

## Notes

These JSON files are the FModel export format for UObjects / Blueprints / DataAssets / DataTables. They contain the full reflected property dumps and are the primary source for the summaries in this repository.

For modding, the most actionable files are the contract data tables, ship resource assets, and core managers.