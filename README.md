# vRP Drug Selling Script (Dansk)

Dette er et simpelt FiveM-script rettet mod vRP-rammen, der bruger `ox_target` til interaktioner, `ox_lib`/`lib` til UI og logger salg til en SQL-tabel. Det sender også en discord webhook ved hvert salg.

## Installation
1. Placer mappen i din serverresources (f.eks. `resources/[local]/sell_drugs_vrp`).
2. Importer `sql/sql.sql` i din database (f.eks. via phpMyAdmin eller MySQL client).
3. Indsæt din Discord webhook i `config.lua`.
4. Start ressourcen i din `server.cfg`:
```
ensure sell_drugs_vrp
```

## Krav
- vRP (tilpasset til din version — funktioner som `vRP.getInventory`, `vRP.tryGetInventoryItem` og `vRP.giveMoney` kan variere)
- ox_target
- ox_lib / lib
- MySQL-async eller tilsvarende SQL-driver (tilpas server.lua hvis du bruger en anden)

## Sikkerhed & tilpasning
- Dette er et udgangspunkt. Tilpas inventory-funktioner til din version af vRP.
- Tjek ox_target API i din version — nogle versioner bruger `addBox`, andre `addSphere` eller `addTarget`.
- Forbedr validering på serveren for at forhindre exploit (double-spend, syncing issues etc.)

## Licens
Fri til personlig/privat serverbrug. Ændr efter behov.
