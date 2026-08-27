# Shadow Farmer spike

**Owner:** PlayerLab
**Status:** proposed
**Destination on success:** none by default; it needs a separate product decision before any promotion.

## Question

Can an off-screen helper entity perform one real, bounded tool action in a single-player save without pretending to be a network farmhand or corrupting game lifecycle state?

## Evidence behind the caution

The related StardewValley-MCP prototype uses a visible NPC plus a shadow Farmer for tool and inventory capabilities, while documenting that the fake Farmer is not entered into the normal multiplayer table because sync assumptions break. This makes it useful risk evidence, not a Player2 dependency or blueprint.[StardewValley-MCP](https://github.com/amarisaster/StardewValley-MCP)

## Minimum experiment

1. Start from an isolated save copy outside the repository.
2. Allow one predeclared tool action on one target only; deny all arbitrary item, combat, money, and world edits.
3. Execute once, reload, advance a day, and inspect the save and SMAPI log for duplicate effects or errors.
4. Repeat with a second real player only to observe failures; do not claim multiplayer support.

## Success and teardown

**Pass:** one action is idempotent across restart, has a visible receipt, and does not add a false player identity to multiplayer synchronization.
**Fail:** any duplicate execution, save anomaly, network-table dependency, or need for a general autonomous loop. Delete it; Player2 remains on marker/body validation.

## Explicit non-goals

- No unattended farming, combat bot, inventory planner, or real-player impersonation.
- No promotion simply because it can water a crop; mechanic power is not relationship evidence.
