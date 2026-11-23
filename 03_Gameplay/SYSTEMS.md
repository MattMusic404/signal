# Gameplay systems — proposed interfaces

- Third-person movement, sprint, crouch, vault, traversal; camera blends into/from Sequencer.
- Stealth: enemy vision cones, light exposure, search patterns, alerts, reinforcement triggers.
- Shooter: aim, recoil, reload, cover, dodge, health/recovery, enemy armor/weak points.
- Signal casting: Signal Scan (reveal routes/interactions), Pulse Shock (temporary electronics disruption), later unlockable decoding, hiding, combat and network powers.
- Hacking: graph routing puzzle, interference, hostile nodes, optional bypass paths.
- Network: relay/tower control, coverage, power, bandwidth, civilian connectivity, security; regional state affects traversal and NPCs.
- Republic building: predefined construction pads at first; workshop, power, research, defense; later hybrid customization.
- Dialogue: authored protagonist with pragmatic/compassionate/defiant responses; choices write persistent flags; no obligatory romance.
- Intel: unique IDs, locations, transcripts, archive types, optional bonuses; missing lore never blocks main story.
- Quest system: prerequisites, objective states, side-quest persistence, replay-safe cinematic flags.

## Suggested save keys (proposal, not implemented)
`INTEL_001_FOUND`, `MAIN_004_CHOICE`, `NODE_ZERO_RESTORED`, `TOWER_01_REPUBLIC_CONTROL`, `REPUBLIC_BROADCAST_SENT`, `ELIAS_TRUST`, `AURELIA_TRUST`, `AURELIA_CLOSENESS`, `AURELIA_ROMANCE_INTEREST`.

## Suggested UE5 structure (proposal)
Primary Data Assets: `DA_Quest`, `DA_Character`, `DA_Location`, `DA_Intel`, `DA_Cinematic`. GameInstance subsystem or equivalent for persistent story state; save-game serialization; event-driven objectives; Sequencer bindings; behavior trees/state trees for enemies. Codex must inspect the real project before selecting classes/plugins.
