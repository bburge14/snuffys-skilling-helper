# Snuffy's Skilling Helper changelog

Each version's changes, newest first.

## 1.10.0 (2026-11-05)

- Skilling hover cards: Your Tool is green when it's the best you can use, orange when a better one is open to you, red only when you have none (in its metal's colour a dragon tool read as a warning)
- Skilling Helper: the Where line shows one place, no (+47 more): where you've been training it when that's one of its places (noticed as you gain XP there, by the wiki's map areas for each place, now in locations.json; kept until you train that skill somewhere else), else the best one
- Skills tab bars: brighter (level orange to green, goal gold), a pixel thicker (3) and on a nearly solid backing, so they read clearly over the skill stones
- Skilling Helper: brighter progress bars on the skill cards and the pinned skill (level, goal and milestone), on a slightly darker track
- Planner: minigames to plan with: Wintertodt, Tempoross, Hunters' Rumours, Pyramid Plunder and Volcanic Mine in their skills' Actions lists, timed by the hour at the wiki's XP rate for your level (each rate from a sentence on its wiki page, checked each time training.json is regenerated; Wintertodt's and the rumours' scale by level as their XP does; a straight line between the levels the wiki gives)
- Skilling Helper: on a supply milestone the count switches every 5 seconds between the supplies still to get and the actions to the next level, as the other counts do
- Planner: what your plan's milestones make and you then sell, alch or drop is counted as you do it: GE sales as they fill (after tax), high alchs (the item leaving and the coins coming in after you cast the spell on it) and drops (the item leaving after you choose Drop), on the milestone that makes it, as Record sales... does by hand; its money so far shows them (Dropped: worth nothing)
- Planner: with the Skilling Helper running and the plan linked to your goal, the milestone you're on is timed at your own XP/hr as the tracker counts it while you train (45.5K/hr yours; Rate from: your XP/hr now), shared live between the plugins (PluginMessage xp-rate); the Planner still shows no rate of its own
- Tree timers: at zero the tree falls with the next log, so the bar and its time also count your usual ticks between logs (shared by everyone chopping) and empty about when it falls, instead of sitting red and blinking until the next log
- Actions count says what it counts to: Actions to lvl 60 / to goal on the pinned skill, 1,026 (60) on the sidebar card; when that isn't the next level it switches every 5 seconds between it and the next level, saying which
- Pinned skill overlay: a bar whose left and right text are long together (Step: Lvl 60 with 69.5K xp left) leaves out its middle percentage too

## 1.9.0 (2026-11-04)

- Goal bar for supplies counts what's still to get (3 to get, as its step does) when there's no XP rate, instead of the XP left (300 read as 300 logs); other XP-left texts say xp
- Pinned skill overlay: a bar whose left label is long (Goal: Supplies) leaves out its middle percentage instead of running into it, as the sidebar's bar does
- Supply milestone ending partway into the level you're in kept no exact end, so the goal stayed Lvl 57 instead of the supplies: its end is now always exactly where getting them takes you; the step bar says Supplies (Step: Supplies ran into its percentage) and the Plan line says (supplies) instead of a level
- Planner: the plan reflows around its supply milestones: each supply milestone runs as far as getting its supplies takes you from where the milestone before it ends; each level milestone after one keeps its target level and starts where it ends (sooner when you bought or banked some, later when there's more to get), and one the supplies take you past is done by them (the Skilling Helper's goal goes past it too)
- Supply milestones are the supplies, not levels: the Skilling Helper's step bar (card and pinned skill) fills by how many you have of what the other plan wants, says how many are still to get, and is done when you have them all whatever level that is; the Planner's milestone card bar fills the same way; the Planner shares how many are wanted and had with the Skilling Helper
- Linked plan ending in supplies: the goal is exactly where getting them takes you (its XP), not the level it's in, and its bar says Goal: Supplies; a supply milestone's bar says Step: Supplies (Step: ~Lvl 57 ran into its percentage)
- Skilling Helper: a supply milestone counts its supplies, not its levels: the actions line says how many are still to get (the Planner works it out from your bank and inventory as you go), and its step bar runs to exactly where getting them takes you (~Lvl), on the card and the pinned skill
- Supply milestones stay linked between the Planner and the Skilling Helper: on every refresh (bank, inventory, XP), whichever Planner tab is open, each plan's supply milestones follow what's still to get in your copy and in the tracker's copy (even while yours has unsent edits), and the ones you have all the supplies of are saved for the Skilling Helper, whose goal, suggestion, highlights and pinned card go on to the next milestone; the Planner's game-screen plan does too
- Planner: a supply milestone is done as soon as you have all its supplies (cut, bought or banked): it says so, takes no levels, isn't the current one, and the next milestone starts where the one before it ended; if you use them up it comes back with what's left to get
- Planner: supply milestones follow on from each other even when you have all their supplies (bought or banked): one with nothing left to get keeps its length but moves up when the one before it gets shorter, and the ordinary one after it follows; a supply milestone ends exactly where its supplies take you (partway into its last level), so its to-go, XP and time match what's still to get and the next one starts there; the supply line's counts are exact up to 99,999 so they add up
- Training locations: the quests each place needs (from its notes and its area), checked against your quests: places you can reach first, the rest saying what they need (Planner's Where, the tracker's Where line); fishing spots for every fish; Ape Atoll's teaks last (aggressive jungle spiders keep you in combat)

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
