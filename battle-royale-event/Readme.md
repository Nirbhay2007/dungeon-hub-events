Battle Royale Plugin – Final PRD with Class Paths

Overview

This plugin adds a Battle Royale event with RPG-style progression. Players can choose a Path by interacting with one of 5 Quest Masters. Each path offers unique quests, permanent upgrades, and abilities to make gameplay more engaging and strategic.

⸻

Core Concept
	•	5 Quest Masters, each representing a unique path (class):
	1.	Healer → Support role, health regeneration, potion-based gameplay.
	2.	Tank → High defense, resistance buffs.
	3.	Berserker → High melee damage, strength effects.
	4.	Archer → Ranged specialization, speed effects.
	5.	Mage → Magic-like effects (simulated with potion effects).

⸻

Quest System
	•	Each path has 6 quests total, increasing in difficulty:
	•	Quests 1–3: Easy to Medium difficulty.
	•	Quests 4–6: Hard difficulty.
	•	Reward progression:
	•	After completing first 3 quests: Player gains a passive effect (based on path).
	•	Healer → Regeneration I
	•	Tank → Resistance I
	•	Berserker → Strength I
	•	Archer → Speed I
	•	Mage → Haste I
	•	After completing all 6 quests: Player gains +1 permanent heart (configurable in config.yml).

⸻

Quest Examples
	•	Healer Path:
	•	Quest 1: Heal 50 HP of players.
	•	Quest 2: Brew 5 healing potions.
	•	Quest 3: Heal 3 players during PvP.
	•	Quest 4: Heal 10 players during combat.
	•	Quest 5: Brew 10 splash healing potions.
	•	Quest 6: Heal 500 HP total in the event.
	•	Tank Path:
	•	Quest 1: Block 500 damage using armor.
	•	Quest 2: Survive 5 minutes in a combat zone.
	•	Quest 3: Absorb 1000 damage without dying.
	•	Quest 4: Kill 5 players while under Resistance.
	•	Quest 5: Take 2000 damage total in event.
	•	Quest 6: Survive 15 minutes in shrinking zone.

(Similar unique structure for Berserker, Archer, Mage.)

⸻

GUI & Player Flow
	•	Step 1: Player right-clicks a Quest Master → Opens Path Selection GUI (with 5 options).
	•	Step 2: Choosing a path locks them into that path (can’t change).
	•	Step 3: Opens the Quest GUI for that path:
	•	Shows 6 slots, each representing a quest.
	•	Locked quests are greyed out until previous ones are completed.
	•	Hover shows:
	•	Quest name
	•	Requirements
	•	Rewards
	•	Step 4: Player completes quests → Rewards apply instantly.

⸻

Reward Mechanics
	•	Passive Effect: Applied after quest 3, lasts until event ends.
	•	Extra Heart: Granted after completing all 6 quests, persists for event duration.

⸻

Technical Details
	•	Plugin API: Paper (1.20+)
	•	Data Storage: YAML or MySQL for persistence.
	•	NPCs: Citizens API for Quest Masters.
	•	Effects: Apply potion effects via Bukkit API.
	•	Permanent Hearts: Implemented using AttributeModifier (GENERIC_MAX_HEALTH).

⸻

Commands
	•	/path reset <player> → Reset path selection.
	•	/quest progress → Show current quest progress.
	•	/event start → Start event.
	•	/event stop → Stop event.

⸻

Permissions
	•	battleroyale.admin → Manage event and reset players.
	•	battleroyale.player → Default player permission.

⸻

Future Enhancements
	•	Path-based abilities/skills (e.g., Berserker Rage, Healing Burst).
	•	Leaderboards for fastest path completion.
	•	Team-based Battle Royale with class synergy.
