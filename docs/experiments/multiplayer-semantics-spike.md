# Multiplayer semantics spike

**Owner:** PlayerLab
**Status:** proposed
**Destination on success:** a separately scoped multiplayer feature, never a hidden implementation detail of Player2.

## Question

Do players obtain a distinct value from a real second farmhand connection that a local companion body cannot provide?

## Minimum experiment

1. Use two supported game clients and a disposable test save.
2. Exercise join, leave, sleep/day transition, disconnect, reload, and host shutdown once each.
3. Send one mod message and one player-visible permission receipt; record host and client logs.
4. Compare the player explanation of the experience against the same scenario with the local Player2 companion.

## Success and teardown

**Pass:** the second connection creates a clearly articulated social or mechanical value, and all listed lifecycle transitions leave the save usable.
**Fail:** the value is indistinguishable from a local companion, or any transition creates a mismatch. Delete the spike and do not emulate a farmhand.

## Boundary

SMAPI's multiplayer API supports mod communication in real multiplayer sessions; it is not a license to manufacture a player identity. [SMAPI multiplayer API](https://wiki.stardewvalley.net/Modding%3AModder_Guide/APIs/Multiplayer)
