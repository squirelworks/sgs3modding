# Ship Resource Inventories

Extracted from `DA_ShipResources` data assets (`AD_*.json`) under `/Game/Blueprints/Contracts/Data/`.

Each ship defines a list of `PropType` counts that appear as salvageable / interactable items on the vessel.

## Summary

| Ship              | Total Items | Unique Prop Types | Notes |
|-------------------|-------------|-------------------|-------|
| Fletcher          | 773         | 63                | Destroyer; high ammo, lamps, electrical |
| GrafSpee          | 2039        | 119               | Heavy cruiser; large military loadout |
| JarleBerg         | 1647        | 90                | Research / fishing focus (lots of fish) |
| Liberty_Ship      | 4457        | 89                | Largest civilian cargo vessel |
| Project1124       | 332         | 49                | Smaller military / patrol vessel |
| Soya              | 1874        | 100               | Research ship; high cabinets / electrical |
| Soya_Artic        | 1014        | 86                | Arctic variant of Soya |
| Tutorial_Ship     | 547         | 51                | Intro vessel |
| Uboat             | 813         | 64                | Submarine; high battery / valve count |

## Most Common Prop Types (across all ships)

| Prop Type       | Total Count |
|-----------------|-------------|
| Lamp            | 659         |
| Bottle          | 619         |
| Chest           | 608         |
| ElectricalBox   | 598         |
| Tools           | 585         |
| Barrel          | 567         |
| Ammunition      | 518         |
| Trash           | 516         |
| CardboardBox    | 499         |
| Clothes         | 382         |
| Cable           | 356         |
| Newspaper       | 337         |
| MilitaryChest   | 306         |
| Cabinet         | 286         |

## Per-Ship Top Items

### Fletcher
Ammunition (84), Lamp (40), ElectricalBox (40), CardboardBox (40), Cable (37), MilitaryChest (33), Tools (33), Hull (33)

### GrafSpee
Chest (109), Ammunition (107), Tools (104), ElectricalBox (97), Trash (96), CardboardBox (95), AmmoStand (83), Barrel (69)

### JarleBerg
Fish (134), CardboardBox (87), Cable (71), Lamp (66), Trash (60), Newspaper (58), Bottle (57), Speaker (51)

### Liberty_Ship
Bottle (384), Lamp (334), Barrel (264), Chest (252), Tools (246), Trash (230), Ammunition (199), Clothes (169)

### Project1124
Ammunition (48), MilitaryChest (23), Clothes (23), Lamp (22), Trash (21), Gun (18), Chest (13), AirVent (12)

### Soya
ElectricalBox (159), Cabinet (103), Chest (87), Shelf (84), Plate (80), Barrel (72), CardboardBox (70), Lamp (57)

### Soya_Artic
Cabinet (66), Lamp (59), ElectricalBox (58), CardboardBox (56), Barrel (55), Chest (53), Shelf (50), Ammunition (40)

### Tutorial_Ship
Tools (65), CardboardBox (45), Barrel (42), Chest (39), Cable (37), Bottle (28), Newspaper (26), Plank (24)

### Uboat
Battery (193), Valve (92), ElectricalBox (46), Desk (38), Cable (37), Plank (34), Lamp (34), SearchLight (30)

## Notes

- Prop types come from the game’s `PropType` enum (see headers).
- Counts represent placed instances available for salvage / interaction on that contract map.
- Related data tables (`DT_*.json`) define contract rows using `ContractBaseData` / gameplay tags such as `ShipContract.Fletcher.1`.
- Contract data assets live under `ContractDataAssets/`.

These inventories are useful for balancing mods, understanding ship difficulty, or scripting resource drops.