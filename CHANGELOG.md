# Snuffy's Skilling Helper changelog

Each version's changes, newest first.

## 1.8.0 (2026-11-04)

- Training locations: fishing spots, every fish's places from the wiki's spot kinds (the guides' picks first: Fishing Guild for sharks, Otto's Grotto for barbarian fishing, Prifddinas and Shilo for fly fishing...); the tracker's Where line for guide methods by the fish they catch
- Training locations: locations.json (scripts/update_training_locations.py, from each tree, rock, stall and creature's wiki page, the training guides' picks first with why) shown on each Planner milestone's tooltip (Where) and the tracker's Where line for plan milestones and guide methods with no places

## 1.7.0 (2026-11-04)

- Settings: names and choices fit the sidebar (shorter labels and names, saved keys unchanged), and the settings test now lays out each plugin's panel at the sidebar's width and fails on anything cut short
- Tracker: Set as active goal and its gold dot only with Highlight For on the active goal
- Goal items: tools for gathering goals worked out first and on their own, each production goal separately, and a problem with one is logged (Goal tools for / Goal items for <skill>) instead of leaving every goal with no highlights
- Tracker: a plan milestone is translated into the goal's terms from its action (Maple logs: every maple tree and an axe; Raw shark: the fish and its harpoon; a creature: its trap), the wiki guide's method adding its places; between milestones or before the first, the goal follows the next one instead of nothing (no suggestion meant no outlines or tool highlights)
- Skilling hover card: felling axes (and infernal, 3rd age and gilded axes and pickaxes) count as your tool at their tier; Best For You only for a better tier
- Tracker: an active goal (right-click a goal > Set as active goal, a gold dot marks it) and Highlight For (every goal, or only the active one) for the outlines and item highlights
- Tracker: a plan milestone the wiki's guide has no method for (Maple logs) gets its trees, rocks or spots from the game's objects, so they're outlined and its tools (an axe) highlighted

## 1.6.0 (2026-11-03)

- Tracker: fold each card to its goal bar (- / + at its top-left, remembered per skill)
- Tracker: training what your plan's milestone says (Maple tree for Maple logs) no longer offers to track it, even when the wiki's guide has no method for it

## 1.5.0 (2026-11-03)

- Tracker and Planner: Follow per skill (your plan, your pick for a one-off, the wiki, or the usual order) on both goal cards, the others kept to switch back; sending a plan follows it, a pick follows the pick. Supply milestones go by what the other plan still needs: passed another way they stay open (Levels done, supplies to get), and say how many are for the other plan and how many for their levels
- Planner and tracker: sending a plan clears a Track for goal pick too (it came before the plan, so the tracker kept suggesting it); the goal card says when a pick is what the tracker follows, with Follow the plan instead

## 1.4.0 (2026-11-03)

- Planner: tooltips in sections (gold headers, values in columns, gains green, losses red); each milestone's Sell by (setting, GE or high alch, the better marked, an orange line when the other pays more); Record sales... takes what you got each; so far counts what's not sold yet at today's worth (cash and net)

## 1.3.0 (2026-11-03)

- Planner: high alch values (Sell Products By: whichever pays more by default, GE or high alch; alch less a nature rune) and Record sales... per milestone (sold on the GE, high alched) for its net so far. Launcher Dev: suggests Patch, Minor or Major from the changes since each plugin's last push (a removed setting is major, new settings, classes or a lot of code minor)
- Planner: edits to the plan sent to the tracker are a draft until Send changes (or Undo back to what the tracker has), so trying things never moves your goal; the plan card and goal card say when changes aren't sent
- Planner: estimated XP rates for every action the wiki gives none (a typical count an hour, banking included, times its XP; marked est.), a Pace per milestone (wiki guide, normal, or faster ways like 1-tick karambwans, 2-tick teaks, 3-tick granite), Suggest a plan can keep your milestones and fill only the levels they leave open, and the tracker stays in step with the plan it follows (an older copy shows on the goal card with ways to sync)
- Planner: a plan from the Skilling Helper's goal follows its suggestions when no method is set, starts a set method at its level with the climb filled in, and remembers what it was made from: when the goal or method changes, the goal card offers to update it (saying what changes)
- Planner supplies: the climb to a supply's level is filled in from the wiki's suggestions (ordinary milestones, noted), and a supply you can't do yet, the material row and the milestone waiting on it say so

## 1.2.0 (2026-11-03)

- Planner supplies: a second supply no longer replaces the first (onto a milestone of the same method, or after the other supplies), supplies already in this skill's plan aren't listed, and a milestone says what it keeps for which plan (left out of its sales and net)

## 1.1.4 (2026-11-03)

- Planner: GE buy limits in Timers (how much of each limit is used, when it resets, and whether a stuck offer is the limit or your price), buy time in a plan's materials; hover cards stay away from other plugins' panels under the mouse
- Planner plans: milestones show progress (bar, % and actions done) and tick off as Done when passed, with a game chat message naming the next one and one at the goal

## 1.1.3 (2026-11-02)

- Plugin Hub feedback: RuneLite's AudioPlayer, and one plugin per pull request

## 1.1.2 (2026-11-02)

- Plugin Hub: build=standard in each plugin's runelite-plugin.properties

## 1.1.1 (2026-11-02)

- Planner: dailies are only your own, with examples until you add one
- Plugins use each other's data only while both run
- Planner: a plan overlay when the Skilling Helper isn't installed

## 1.1.0 (2026-11-02)

- GemCrab: the radar shows after hopping at a cove; screenshot captions
- In-game screenshots for the Skilling Helper, PvM/Slayer, GemCrab and Alerts pages
