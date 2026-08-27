# Companion body spike

**Owner:** PlayerLab
**Status:** proposed
**Destination on success:** a deliberately small Player2 visual actor seam; otherwise delete.

## Question

After a Player2 permission turn, does seeing a game-world body travel toward the agreed target make players describe the companion as a partner rather than a HUD feature?

## Why this is isolated

A custom Stardew NPC is not a lightweight sprite toggle. It requires character data, dialogue, schedules, and art assets; missing data can fail to spawn the NPC without an obvious error. That is too much unrelated surface for Player2's first permission experiment. [NPC data](https://wiki.stardewvalley.net/Modding%3ANPC_data) | [common tasks](https://wiki.stardewvalley.net/Modding%3ACommon_tasks)

## Minimum experiment

1. Use one placeholder body, one fixed farm target, and one route after a pre-authorized choice.
2. Never alter crop state, inventory, money, friendship, or player position.
3. Reload the save and advance a day; confirm no duplicate body, stuck path, or persistent save mutation.
4. Record a short video and ask the same Player2 interview question: “它刚才像什么？”

## Success and teardown

**Pass:** most testers distinguish the body from a task marker and link its visible travel to the permission they gave; reload leaves no residue.
**Fail:** the body is merely decorative, requires persistent custom-NPC content, or damages lifecycle correctness. Delete the experiment and keep Player2's visible-result marker.

## Explicit non-goals

- No romance, friendship score, gifts, schedules, portraits, festivals, or generated art.
- No dependency from Player2 to this spike.
- Do not rely on Stardew Valley 1.6.16 ephemeral-character support while Player2's verified game version is earlier.
