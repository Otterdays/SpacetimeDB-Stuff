<!-- PRESERVATION RULE: Never delete or replace content. Append or annotate only. -->

# SPACETIMEDB GAME IDEAS

> ADHD/autism-friendly format
>
> - Short punchy bullet points
> - Clear headers
> - Bite-sized chunks
> - Easy to scan

---

## Categories

- [🔥🔥 INSANE GAMES](#-insane-games) ⭐ NEW
- [🔥 The Sickest Games](#-the-sickest-games)
- [👥 Party Games (2-8 players)](#-party-games)
- [⚔️ Competitive Games](#-competitive-games)
- [🌍 MMO & Persistent World](#-mmo--persistent-world)
- [🛠️ Templates & Frameworks](#-templates--frameworks)
- [📊 By Player Count](#-by-player-count)
- [💸 Money Makers](#-money-makers)
- [🏃 Start Here](#-start-here)

---

# 🔥🔥 INSANE GAMES ⭐

_The ones that make you say "wait that's actually genius"_

---

## I1. THE LAST CITY ON EARTH

**Pitch**: Nuclear war happened. You're the mayor of the last standing city. 1000 players compete to be the leader. Build, defend, make hard choices.

**The Hook**:

- Every choice has consequences that ripple
- Other cities (bots) are "rebuilding" - they compete with you
- Your decisions are recorded in history
- If your city fails, it's GAME OVER for everyone

**What happens**:

- Each day: population grows, resources deplete, threats approach
- Players vote on major decisions: "Build a wall" vs "Expand farms"
- Events happen: raiders, disease, trade caravans
- Resources: food, water, power, medicine, defense
- If ANY resource hits zero = city collapse

**Why SpacetimeDB**:

- City state syncs to all 1000 players
- Vote results must be atomic
- Event scheduler triggers disasters
- History log for "yearbook"

**Money**: Free-to-play + $9.99/month for mayor tools

---

## I2. INFINITE JAILBREAK

**Pitch**: Roguelike prison escape. Each run is a new prison. Get arrested in one run, escape in the next.

**The Hook**:

- 100-cell block, you're prisoner OR guard (random each run)
- Guards: patrol, catch contraband, maintain order
- Prisoners: work together, find exploits, escape
- Your "sentence" from last run becomes your starting item in next
- Earned perks persist across runs

**What happens**:

- Day/night cycle: work time vs free time
- Contraband smuggling system
- Guard rotations (AI)
- Multiple escape routes (vents, tunnels, guard bribing)
- If prisoner escapes = bonus for all prisoners next run
- If guards stop all escapes = bonus for guards next run

**Why SpacetimeDB**:

- Block state syncs in real-time
- Contraband tracking (who has what)
- Guard AI coordination
- Run history/perks persist

**Money**: Free + $4.99/character unlock + cosmetics

---

## I3. POLITICAL MAFIA

**Pitch**: You're a corrupt politician. Make deals, blackmail, betray. The town doesn't know who to trust.

**The Hook**:

- Everyone has SECRET DEALS
- Resources are "political capital" - votes, money, dirt
- Scandals break randomly
- Last honest politician wins (no really)

**What happens**:

- 12 players, each is a "politician"
- Each has a secret alignment: honest OR corrupt
- Corrupt: make deals, blackmail, steal
- Honest: expose corruption, investigate, gather allies
- Votes happen every "session" - politicians get voted out
- If all honest survive = honesty wins
- If 1 corrupt remains = corruption wins

**Why SpacetimeDB**:

- Secret state synced but hidden
- Vote tracking
- Blackmail system (player-to-player leverage)
- Deal making (contracts between players)

**Money**: $2.99/game + skin packs (corrupt politician skins)

---

## I4. THE GAME OF STORIES

**Pitch**: Collaborative storytelling game. Someone starts a story, others continue. But choices matter - and you can "bet" on story directions.

**The Hook**:

- AI dungeon master creates scenarios
- Players vote on actions
- Betting system: bet "story points" on outcomes
- Winners influence next chapter
- Stories are saved, ranked, remixed

**What happens**:

- 4-8 players per story
- AI presents: "You enter a dark forest..."
- Players vote on actions: "Sneak through" vs "March in boldly"
- Everyone bets on winning choice
- Winner gets narrative control
- Story continues, new scenarios generated
- Stories become "canon" in game world

**Why SpacetimeDB**:

- Story state persists across sessions
- Betting system atomic
- Vote sync
- Story library database

**Money**: Free + $1.99/story pack + premium narratives

---

## I5. ONE LIFE FPS

**Pitch**: You die, you're done. No respawn. No do-overs. True permadeath FPS.

**The Hook**:

- One life. One death. Server keeps running without you.
- Your body stays where you died (can be looted)
- New players spawn at random safe zones
- Server history: "KillerOfBob was last seen at Mile Marker 7"

**What happens**:

- Spawn at safe zone
- Loot, craft, explore
- Real-time PvP
- Die = ghost mode (can spectate but not interact)
- New spawn = new character
- Accumulated knowledge: "I know where that guy camps"

**Why SpacetimeDB**:

- Death state is permanent
- Ghost mode observation
- Server-wide death history
- Loot persistence on corpses

**Money**: Free + $9.99/hero unlock (premade characters with backstory)

---

## I6. MASSIVE CAVEMEN (Prehistoric Survival)

**Pitch**: You and 500 others are early humans. Build civilization from scratch. Discover fire. Evolve.

**The Hook**:

- Starts in stone age (no tools, no fire)
- Must discover: fire, wheels, agriculture, metalworking
- Each discovery unlocks new tech tree
- Players specialize: hunters, builders, healers, shamans
- Tribes form, compete, merge

**What happens**:

- Year-based progression (1 year = 1 real hour)
- Discoveries require player actions + time
- Fire: someone must tend flame for 10 minutes
- Wheel: someone must experiment with logs
- Agriculture: someone must plant, wait, harvest
- First to discover gets bonus for their tribe
- Multiple tribes compete to reach modern age

**Why SpacetimeDB**:

- Discovery tree state
- Tribe membership
- Year/timeline scheduler
- Tech progress tracking

**Money**: Free + $4.99/tribe cosmetics + discovery packs

---

## I7. ZOMBIE VIRUS (Real Evolution)

**Pitch**: Zombie outbreak but the virus EVOLVES. Your actions change how it spreads.

**The Hook**:

- Virus starts slow (slow zombies)
- If too many killed: virus mutates (fast zombies)
- If too many survive: virus mutates (smart zombies)
- Players influence evolution through actions
- No winning - just surviving

**What happens**:

- 100 players, 1 city
- Virus spreads through NPCs first
- Players can: fight, research cure, fortify, escape
- Research progress: cure % goes up when players experiment
- Each mutation: new zombie type
- Cure complete = all zombies die (good ending)
- All players die = virus wins (bad ending)
- Neither = virus becomes endemic (survival mode continues)

**Why SpacetimeDB**:

- Virus mutation state
- Research progress
- Player infection tracking
- Event scheduler for mutations

**Money**: Free + $7.99/mutation pack + cosmetic zombies

---

## I8. THE IMPOSTER

**Pitch**: Werewolf but you're IN the game world. See other players. Hear them. Find the imposter.

**The Hook**:

- 10 players in a map (real 3D, not top-down)
- One player is "The Imposter" - they look identical
- Task holders must complete tasks scattered around map
- Imposter can kill (knock out) task holders
- Other players hear screams, see bodies
- Vote to accuse at any time
- Wrong accusation = imposter wins
- Correct accusation = survivors win

**What happens**:

- First-person (or third-person) view in map
- Complete tasks: click buttons, move objects, activate switches
- Imposter: can fake tasks, must kill without being seen
- Bodies disappear after 30 seconds
- Emergency meetings: gather at locations, vote
- Chat and voice allowed (imposter can lie)

**Why SpacetimeDB**:

- Player positions sync in real-time
- Task completion state
- Kill detection (line-of-sight)
- Vote atomic

**Money**: Free + $3.99/character skin + map packs

---

## I9. TOWER DEFENSE BUILDER

**Pitch**: You and 20 others are building towers. Then waves of enemies attack. See if your defenses hold.

**The Hook**:

- Phase 1: BUILD (15 minutes) - work together to place towers, walls, traps
- Phase 2: DEFEND (15 minutes) - enemies attack, your builds are tested
- Phase 3: SCORE - how long did you survive? Leaderboard
- Builds persist - challenge other players' defenses

**What happens**:

- Grid-based building
- Tower types: arrow, cannon, frost, slow, AoE
- Wall types: wood, stone, reinforced
- Trap types: spike, pit, tar
- Enemy waves: goblins, orcs, trolls, dragons
- Enemy AI targets weakest point
- Your build is rated: "How many waves survived?"

**Why SpacetimeDB**:

- Build state persists
- Wave scheduling
- Enemy pathfinding
- Leaderboard sync

**Money**: Free + $2.99/tower pack + enemy pack

---

## I10. COLONY SHIP (Generation Ship)

**Pitch**: You were born on a colony ship. You'll die before arrival. Your kids will continue the journey.

**The Hook**:

- Ship takes 100 "years" (accelerated time) to reach destination
- Players are "generations" - new players replace those who "die"
- Each generation makes decisions that affect next
- Your actions have consequences for your grandchildren
- End goal: reach destination with viable population

**What happens**:

- 50 players per ship
- Each "year": resources deplete, events happen
- Decisions: ration food, explore ship sections, medical priorities
- Babies born (new players) replace deaths
- Your character's stats/memories pass to "children" (new players)
- Ship can fail: starvation, mutiny, disease
- Ship can succeed: new civilization on new world

**Why SpacetimeDB**:

- Ship state persists across generations
- Inheritance system (parent to child)
- Event scheduler
- History log

**Money**: Free + $9.99/month + ship customization

---

## I11. MASSIVE SNOWBALL FIGHT

**Pitch**: Two teams, 500 players each. Build forts, make snowballs, have the most EPIC snowball fight ever.

**The Hook**:

- Large snowy map (ski resort theme)
- Team-based: Red vs Blue
- Build forts, towers, ramps
- Stockpile snowballs
- Capture zones for snowball upgrades (bigger, faster, explosive)
- Match is 30 minutes

**What happens**:

- Building phase (first 5 min): build your base
- Battle phase: fight for control
- Zones give: powerups, snowball upgrades, artillery
- Special snowballs: rapid fire, homing, ice wall breaker
- Team with most captures at end wins

**Why SpacetimeDB**:

- 500v500 real-time
- Building persistence
- Projectile sync
- Zone control state

**Money**: Free + $4.99/snowball pack + team cosmetics

---

## I12. NEON HEIST (Tactical)

**Pitch**: Plan and execute heists. 5 heist types. Real-time. Tactical.

**The Hook**:

- 4 players: Mastermind, Hacker, Muscle, Ghost
- Each has unique abilities
- Plan phase: discuss, assign roles, set timers
- Execute phase: real-time, must adapt
- Get caught = arrested (lose money, keep gear)
- Escape = keep loot

**What happens**:

- Bank heist: vault cracking, silent alarms
- Casino: high security, multiple paths
- Museum: time locks, laser grids
- Prison: break someone out
- Jewelry store: quick smash and grab
- Money from heists buys better gear
- Reputation unlocks harder heists

**Why SpacetimeDB**:

- Heist state machine
- Role abilities
- Timer synchronization
- Loot distribution

**Money**: Free + $14.99/heist pack + weapon skins

---

## I13. SKELETON INVASION (PvE Survival)

**Pitch**: You're a village. Waves of skeletons attack. Every night is harder. How long can you survive?

**The Hook**:

- 20 players defend a village
- Day: prepare, gather resources, upgrade
- Night: skeletons attack from all sides
- Each night: harder waves
- If village falls = game over, start over

**What happens**:

- Resource gathering: wood, stone, iron
- Building: walls, towers, traps
- Upgrading: better weapons, stronger walls
- Skeleton types: basic, fast, tank, mage
- Boss skeleton every 5 nights
- Village persists between sessions (if survived)

**Why SpacetimeDB**:

- Village state persists
- Wave scheduling
- Resource tracking
- Building persistence

**Money**: Free + $5.99/upgrade pack + skeleton types

---

## I14. BATTLE OF THE WORLDS

**Pitch**: Historical battle re-enactment. 500v500. Medieval, WW2, whatever.

**The Hook**:

- Massive historical battles
- You play a soldier in the army
- Commander (player) gives orders
- Must follow orders or be court-martialed
- Army with most objectives wins

**What happens**:

- Choose side: Allies vs Axis (WW2), Romans vs Barbarians, etc
- Commander assigns squads to objectives
- Soldiers: move, shoot, take cover, revive teammates
- Objectives: capture point, defend position, escort tank
- Commanders vote on overall strategy

**Why SpacetimeDB**:

- 500v500 real-time combat
- Commander orders
- Squad coordination
- Objective state

**Money**: Free + $9.99/battle pack + vehicle skins

---

## I15. WEREWOLF SIMULATOR (You ARE The Wolf)

**Pitch**: You play as the werewolf hunting humans. Not the other way around.

**The Hook**:

- Werewolf perspective (first person)
- Humans have flashlights, weapons, cars
- You can transform: human (fast, stealth) vs wolf (strong, visible)
- Hunt in a large forest/map
- Game ends when all humans escape OR all humans dead

**What happens**:

- Your goal: kill humans before they escape
- Humans: find car keys, get to extraction
- You: track by scent, break through barricades
- Human abilities: shoot, trap, barricade
- Wolf abilities: sprint, pounce, howl (summon AI wolves)
- Kill enough humans = victory

**Why SpacetimeDB**:

- Wolf position sync
- Human tracking (scent trails)
- Barricade state
- Extraction point state

**Money**: Free + $6.99/wolf skin pack + map packs

---

## I16. GHOST TOWN (Building Game)

**Pitch**: Ghost town needs rebuilding. Players come and go. Your contributions last.

**The Hook**:

- Persistent town that evolves over months
- Players arrive, build something, leave
- Their builds remain
- Town grows organically based on contributions
- "Wow, that player built the beautiful fountain in the town square"

**What happens**:

- Abandoned ghost town (pre-built废墟)
- Players visit for limited time (2 hours/day free, unlimited with subscription)
- Build: houses, shops, decorations, infrastructure
- Earn "town credits" for building
- Spend credits on better tools
- Town becomes beautiful over time

**Why SpacetimeDB**:

- Persistent building state
- Player visit scheduling
- Town credit economy
- Leaderboard of contributors

**Money**: Free 2hr/day + $9.99/month unlimited

---

## I17. STICK FIGURE WARFARE

**Pitch**: Stick figure armies. Millions of them. Real-time battles. You're the general.

**The Hook**:

- Not controlling individuals - you're the general
- Draw orders: "Send 1000 to attack here"
- Watch the battle unfold
- Millions of stick figures clash

**What happens**:

- Draw movement lines on map
- Select units: infantry, archers, cavalry, siege
- Assign formations: line, column, circle
- Watch battle in fast-forward
- Units fight automatically
- Strategy matters more than micro

**Why SpacetimeDB**:

- Order drawing sync
- Unit pathfinding
- Combat resolution
- Battle replay

**Money**: Free + $4.99/army pack + map packs

---

## I18. REAL-TIME DUNGEON CRAWLER

**Pitch**: You explore a dungeon. 1000 other players are in there too. See them, fight near them, compete for loot.

**The Hook**:

- Massive procedurally generated dungeon
- 1000 players can be in at once
- Players from different guilds
- Boss fights require cooperation OR competition for loot
- Death = drop some loot (can be stolen)

**What happens**:

- Enter dungeon freely
- Find loot, fight monsters, clear rooms
- Party up with strangers or go solo
- Boss rooms: compete for kill OR work together
- PvP enabled in some zones
- Escape with loot OR die trying

**Why SpacetimeDB**:

- Massive player sync
- Loot ownership
- Boss aggro
- Dungeon state

**Money**: Free + $9.99/month + cosmetic skins

---

## I19. KINGS AND KNIGHTS (Castle Defense)

**Pitch**: You're the king. Your castle is under attack. Make decisions. Can you survive?

**The Hook**:

- Top-down castle view
- Knights (AI) defend walls
- You give orders: where to reinforce, when to sally forth
- Enemy waves get harder
- Your castle upgrades based on your decisions

**What happens**:

- Day: gather resources, build defenses, train knights
- Night: enemy waves attack
- You: click to direct knights, trigger abilities
- Boss every 10 waves
- Your castle is YOUR castle - persists between sessions
- Guilds can attack other castles

**Why SpacetimeDB**:

- Castle state persistence
- Knight AI coordination
- Wave scheduling
- Guild castle battles

**Money**: Free + $7.99/castle upgrade pack

---

## I20. CHAIN REACTION (Physics Sandbox)

**Pitch**: Place objects. Watch the chain reaction. Score points for making the biggest boom.

**The Hook**:

- Physics sandbox
- Place: dominoes, catapults, explosives, ramps, balls
- Trigger and watch
- Score: how far does the chain go?
- Share your creation
- See other players' creations trigger

**What happens**:

- Drag-and-drop objects
- Click to trigger
- Physics simulation runs
- Score based on chain length
- Save and share creations
- Daily challenge: "Use these 50 objects to score highest"

**Why SpacetimeDB**:

- Creation persistence
- Physics sync
- Leaderboard
- Creation library

**Money**: Free + $2.99/object pack + creation packs

---

## I21. TRENCH WARFARE WWI

**Pitch**: You're in the trenches. Your squad must cross no-man's land. Will you make it?

**The Hook**:

- Realistic WWI setting
- Cross no-man's land to enemy trenches
- One-way trip (no respawn until objective)
- Your squad: 10 players
- Enemy: 10 players + AI

**What happens**:

- Plan phase: discuss strategy, assign roles
- Execute: sprint, crawl, take cover, throw grenades
- Realistic: one bullet kills
- Must reach enemy trench to win round
- Multiple rounds, each team gets to attack

**Why SpacetimeDB**:

- Squad position sync
- One-hit-kill combat
- Objective state
- Round management

**Money**: $14.99/game + weapon customization

---

## I22. ANIMAL RESCUE (Cozy)

**Pitch**: Cute animal rescue game. Save animals, heal them, release them.

**The Hook**:

- Wholesome, cozy, relaxing
- Animals get injured, you rescue them
- Heal them in your shelter
- Release them when healthy
- Animals remember you

**What happens**:

- Animals spawn injured in the world
- Find them, bring back to shelter
- Mini-games to heal: set broken bones, feed, comfort
- Healthy animals can be released
- Released animals occasionally visit with gifts
- Leaderboard: animals saved

**Why SpacetimeDB**:

- Animal state (injured, healing, healthy)
- Shelter inventory
- Release tracking
- Gift system

**Money**: Free + $4.99/shelter upgrade + cosmetic animals

---

## I23. ULTIMATE TAG

**Pitch**: You're IT. 20 players. Giant map. 5-minute rounds. How long can you stay free?

**The Hook**:

- One player is IT
- Everyone else runs
- IT can sprint faster but gets tired
- Players can tag each other to pass IT
- Last person standing (not IT) at end wins

**What happens**:

- Random player starts as IT
- Giant map: city, forest, maze
- Power-ups: speed boost, freeze, teleport
- IT timer: if IT doesn't tag someone in 60s, random IT
- End of round: everyone not IT wins

**Why SpacetimeDB**:

- 20-player position sync
- IT state
- Power-up spawning
- Round timer

**Money**: Free + $1.99/power-up pack + map packs

---

## I24. UNDERCOVER AGENT

**Pitch**: Deep cover espionage. Complete missions as a spy. But you don't know who's on your team.

**The Hook**:

- 8 players, some are spies, most are agents
- Agents complete missions together
- Spies sabotage from within
- Missions succeed/fail based on votes
- Vote on who to trust
- Last spy standing wins

**What happens**:

- Missions appear: "Hack the mainframe"
- Players volunteer to go on mission
- On mission: all participants do a task (puzzle)
- Spies can fail the task (sabotage)
- Majority vote decides mission success
- If missions keep failing = spies win

**Why SpacetimeDB**:

- Mission state
- Vote tracking
- Spy identification (hidden)
- Task completion

**Money**: $4.99/game + mission packs

---

## I25. MEGA CONSTRUCTOR (Minecraft meets Besiege)

**Pitch**: Build vehicles. Test them. Share them. Compete with them.

**The Hook**:

- Physics-based building
- Build cars, planes, robots, anything
- Test in real-time
- Share creations
- Race, fight, or solve challenges with your builds

**What happens**:

- Voxel-based building
- Add wheels, engines, wings, weapons
- Test drive/fly
- Publish to community
- Play challenges: "Fastest car", "Can this bridge hold?"
- Compete with other players' builds

**Why SpacetimeDB**:

- Creation persistence
- Physics simulation
- Leaderboard
- Creation library

**Money**: Free + $4.99/blueprint pack + premium builds

---

## I26. SURVIVAL ISLAND

**Pitch**: You wake up on a deserted island. 50 others are there too. Work together or die.

**The Hook**:

- Island survival game
- No PvP, PvE only
- Find resources, build shelter, survive
- Events: storms, predator attacks, disease
- Weekly challenges: "Survive 7 days"

**What happens**:

- Resource gathering: wood, stone, food, water
- Building: shelter, tools, defenses
- Crafting: weapons, tools, medicine
- Events: random challenges
- Leaderboard: longest survival
- Death = new character, new island

**Why SpacetimeDB**:

- Survival state
- Resource tracking
- Event scheduling
- Leaderboard

**Money**: Free + $5.99/survival kit + island pack

---

## I27. SPY VS SPY (Classic)

**Pitch**: Based on the comic. Two spies infiltrate a building. Steal the briefcase. Escape.

**The Hook**:

- Two players, one building
- Stealth-based
- Set traps, avoid traps
- First to grab briefcase and escape wins

**What happens**:

- Same building, different starting positions
- Move through building
- Set traps: banana peel, spring, bear trap
- Avoid enemy traps
- Grab briefcase
- Find exit
- Can also disable enemy traps

**Why SpacetimeDB**:

- Position sync
- Trap state
- Objective state
- Escape detection

**Money**: $4.99 + $2.99/building pack

---

## I28. TOWER OF DOOM (Roguelike)

**Pitch**: 4 players. 100 floors. Procedurally generated. Will you reach the top?

**The Hook**:

- Co-op roguelike
- 100 floors, each harder
- Between floors: shop, rest, upgrade
- Death = restart from floor 1
- Leaderboard: highest floor reached

**What happens**:

- 4 players work together
- Floor types: combat, puzzle, trap, boss
- Combat: enemies scale with floor
- Puzzle: co-op required
- Boss: every 10 floors
- Upgrades: permanent, persist across runs
- Meta-progression: unlock new characters

**Why SpacetimeDB**:

- Floor state
- Player coordination
- Upgrade persistence
- Leaderboard

**Money**: $14.99 + $4.99/floor pack + character unlock

---

## I29. PANDEMIC (Board Game Digital)

**Pitch**: Digital adaptation of Pandemic. 4 players, viruses spreading, cure before it's too late.

**The Hook**:

- Classic board game mechanics
- 4 roles with unique abilities
- Viruses spread across map
- Must cure all 4 before outbreak count hits limit
- Lose if too many outbreaks OR can't cure

**What happens**:

- Role selection: medic, scientist, dispatcher, etc
- Each turn: 4 actions + draw cards + infections
- Travel, treat, cure, build research stations
- Event cards for special abilities
- Win: cure all diseases
- Lose: outbreak chain reaction

**Why SpacetimeDB**:

- Board state
- Role abilities
- Card deck
- Outbreak tracking

**Money**: $9.99 + $2.99/expansion pack

---

## I30. DEAD BY DAYLIGHT (Clone)

**Pitch**: 4 survivors vs 1 killer. Repair generators. Escape. Don't get caught.

**The Hook**:

- 4 players are survivors
- 1 player is killer
- Survivors: fix 5 generators, open exit, escape
- Killer: hunt survivors, sacrifice to hook
- Survivors lose if hooked 3 times

**What happens**:

- Survivors: move, repair, heal, hide, sprint
- Killer: move faster, lunge, place traps
- Generators scattered around map
- Fixed generators = progress
- Fixed 5 = exit gates open
- Killer can close gates, see scratch marks

**Why SpacetimeDB**:

- Survivor/killer position sync
- Generator state
- Hook/sacrifice tracking
- Exit state

**Money**: Free + $9.99/killer skin + map pack

---

## I31. AMONG US (Clone)

**Pitch**: Crewmates complete tasks. Impostors sabotage and kill. Find the impostors.

**The Hook**:

- 10 players, 1-2 impostors
- Complete tasks to win (crew)
- Kill and sabotage to win (impostors)
- Vote out suspected impostors
- Wrong votes = impostors closer to winning

**What happens**:

- Move around map
- Complete mini-game tasks
- Report bodies OR call emergency meeting
- Discuss, vote, eject
- Impostors: fake tasks, vent, kill, sabotage
- Game ends: tasks complete OR impostors equal crew

**Why SpacetimeDB**:

- Player positions
- Task state
- Body tracking
- Vote system

**Money**: Free + $1.99/cosmetics + map packs

---

## I32. FORTNITE (Clone)

**Pitch**: Battle royale with building. 100 players. Last one standing.

**The Hook**:

- Classic BR mechanics
- Plus building: walls, ramps, floors
- Materials: wood, brick, metal
- Zone shrinks
- Loot, fight, build, survive

**What happens**:

- Drop from battle bus
- Loot buildings
- Build structures
- Zone damage
- Storm circles
- Last alive wins

**Why SpacetimeDB**:

- 100-player sync
- Building state
- Loot state
- Zone management

**Money**: Free + $9.99/battle pass + skin packs

---

## I33. PHANTOM ABYSS (Co-op Dungeon)

**Pitch**: Enter the abyss. Find treasures. Escape alive. The abyss has other teams.

**The Hook**:

- 4 players per team
- Procedural dungeon
- Other teams are IN the same dungeon
- Can help OR hinder
- Most treasure wins

**What happens**:

- Enter dungeon
- Find treasure, traps, monsters
- Other teams: can ally OR steal
- Timer: must escape before time runs out
- Treasure value determines winner
- Die in dungeon = lose all treasure

**Why SpacetimeDB**:

- Multi-team dungeon state
- Treasure tracking
- Escape detection
- Team coordination

**Money**: $14.99 + $4.99/dungeon pack

---

## I34. ROLLERBALL (Sports)

**Pitch**: Team sport: skate, hit, score. Like roller derby meets bumper cars meets hockey.

**The Hook**:

- 6v6 teams
- Skate around arena
- Hit ball into opponent's goal
- Bump opponents (no rules)
- Penalty box for fouls

**What happens**:

- Movement: roller skates
- Hit ball with body or stick
- Bump other players
- Goal scoring
- Penalty system
- Season mode with rankings

**Why SpacetimeDB**:

- Player positions
- Ball physics
- Goal detection
- Penalty tracking

**Money**: Free + $4.99/team customization + arena packs

---

## I35. NINJA WARRIOR (Obstacle Course)

**Pitch**: Race through obstacle courses. First to the top wins.

**The Hook**:

- Mount climbing obstacle course
- Race 4 players
- Obstacles: swinging, climbing, balancing
- Fall = respawn at last checkpoint
- First to top wins

**What happens**:

- Pick character
- Join race
- Climb obstacles
- Fall, respawn
- Leaderboard for fastest times
- Weekly challenge: new course

**Why SpacetimeDB**:

- Position sync
- Obstacle state
- Checkpoint detection
- Timer sync

**Money**: Free + $2.99/character + course packs

---

## I36. TUG OF WAR (Massive)

**Pitch**: 500 players on each side. Pull the rope. Break the other team's will.

**The Hook**:

- Tug of war with massive teams
- Real force calculation (players pulling harder = rope moves)
- Stamina system
- Team coordination

**What happens**:

- Join red or blue team
- Click to pull (hold)
- Your pull strength = based on timing
- Team must coordinate
- Rope moves toward stronger side
- Pull past threshold = win

**Why SpacetimeDB**:

- 1000-player pull calculation
- Rope position
- Stamina tracking
- Team coordination

**Money**: Free + $2.99/team skin

---

## I37. WIZARD DUEL

**Pitch**: First-person wizard duel. Cast spells. Dodge. Defeat your opponent.

**The Hook**:

- 1v1 wizard battles
- First-person view
- Cast spells: fireball, ice, lightning, shield
- Dodge, block, counter
- Best of 3 rounds

**What happens**:

- Pick spell loadout (3 spells)
- Duel 1v1
- Cast, dodge, block
- Health bar
- First to deplete opponent wins
- Ranking system

**Why SpacetimeDB**:

- Position sync
- Spell state
- Health tracking
- Round management

**Money**: Free + $4.99/spell pack + wizard skins

---

## I38. KART RACING

**Pitch**: Mario Kart style racing. Items, drifts, chaos.

**The Hook**:

- 12 players per race
- Tracks with hazards
- Items: shells, banana, boost
- Drift for boost
- First across finish wins

**What happens**:

- Race on tracks
- Collect item boxes
- Use items against opponents
- Drift around corners for boost
- Boost pads on track
- First 3 across finish = points for season

**Why SpacetimeDB**:

- Kart positions
- Item state
- Drift boost
- Lap tracking

**Money**: Free + $4.99/kart + track packs

---

## I39. SIEGE (Vehicle)

**Pitch**: Vehicles vs walls. Destroy the castle. Or defend it.

**The Hook**:

- Attackers: tanks, helicopters, infantry
- Defenders: walls, turrets, soldiers
- Real-time siege
- Destroy objective to win

**What happens**:

- Choose faction: attacker or defender
- Attacker: deploy vehicles, infantry
- Defender: fortify, place turrets
- Battle rages
- Destroy objective = win
- Hold long enough = win

**Why SpacetimeDB**:

- Vehicle positions
- Building state
- Objective state
- Team coordination

**Money**: Free + $9.99/faction pack + vehicle skins

---

## I40. WEREWOLF ONLINE

**Pitch**: Classic werewolf with AI moderator. Play anytime.

**The Hook**:

- 5-20 players
- AI narrates the game
- Roles: werewolf, villager, seer, witch, etc
- Night: wolves kill, seer checks
- Day: discuss, vote to eliminate
- Find all wolves = villagers win
- Wolves equal villagers = wolves win

**What happens**:

- Join game
- Get assigned role (hidden)
- Night phase: perform role action
- Day phase: discuss, vote
- AI moderator narrates
- Continue until win condition

**Why SpacetimeDB**:

- Role assignment
- Night actions
- Vote tracking
- AI narration

**Money**: Free + $1.99/role pack + cosmetic skins

---

## I41. BATTLE SHIPS (Artillery)

**Pitch**: Classic battleship game. Real-time. Shoot, dodge, sink.

**The Hook**:

- 2v2 naval battles
- Position hidden, only shots reveal
- Aim, fire, adjust
- Sink enemy ships to win

**What happens**:

- Position on grid
- Move ships
- Fire cannons
- Shells arc (mortar style)
- Hit detection on grid
- Sink all enemy ships to win

**Why SpacetimeDB**:

- Ship positions
- Shot trajectory
- Hit detection
- Team coordination

**Money**: Free + $3.99/ship pack + map packs

---

## I42. RUMBLE (Sumo Wrestling)

**Pitch**: 2 players in a ring. Push, dodge, survive. Fall out = lose.

**The Hook**:

- 1v1 sumo matches
- Simple controls: left, right, dash, grab
- Push opponent out of ring
- Best of 3 rounds

**What happens**:

- Enter ring
- Dash, grab, push
- Don't fall out
- Best of 3
- Ranking system
- Tournament mode

**Why SpacetimeDB**:

- Player positions
- Ring boundary
- Grab mechanics
- Round state

**Money**: Free + $2.99/wrestler + arena packs

---

## I43. CHESS BOXING

**Pitch**: Alternate between chess and boxing. Think AND fight.

**The Hook**:

- Rounds: 1 round chess, 1 round boxing, repeat
- Boxing: punch to score
- Chess: checkmate OR get KO'd
- Win either way = win match

**What happens**:

- 4 rounds
- Odd rounds: chess (move timer)
- Even rounds: boxing (hit to score)
- Win by chess checkmate OR boxing knockout
- Points accumulate across rounds

**Why SpacetimeDB**:

- Chess state
- Boxing state
- Round management
- Timer sync

**Money**: Free + $3.99/character + ring packs

---

## I44. PICKLEBALL MIXER

**Pitch**: Realistic pickleball. Play against AI or real players.

**The Hook**:

- 2v2 doubles
- Real physics
- Serve, return, volley
- First to 11, win by 2

**What happens**:

- Form team or matchmake
- Serve and rally
- Score points
- Best team wins
- Season rankings

**Why SpacetimeDB**:

- Ball physics
- Player positions
- Score tracking
- Serve rotation

**Money**: Free + $4.99/court pack + paddle skins

---

## I45. HIDE AND SEEK (Massive)

**Pitch**: 50 players. One seeker. Hide well.

**The Hook**:

- One seeker counts
- Others hide
- Found = join seeker
- Last found wins

**What happens**:

- Large map (city, forest, etc)
- Seeker counts (eyes closed)
- Players hide
- Timer ends, seeker hunts
- Found players join seeker team
- Last player standing wins

**Why SpacetimeDB**:

- Hider positions
- Seeker state
- Found detection
- Round management

**Money**: Free + $2.99/map pack

---

## I46. KEEP AWAY (Sports)

**Pitch**: 2 teams. One ball. Don't let the other team touch it.

**The Hook**:

- 5v5 keep-away
- Ball carrier can't run over certain line
- Tag by touching = turnover
- Score by reaching end zone

**What happens**:

- Grab ball
- Run with ball
- Get tagged = turnover
- Reach end zone = score
- Most points wins

**Why SpacetimeDB**:

- Ball state
- Player positions
- Tag detection
- Score tracking

**Money**: Free + $3.99/field pack + uniform skins

---

## I47. QUAKE-STYLE ARENA

**Pitch**: Fast FPS. Rocket jumping. Power-ups. Pure skill.

**The Hook**:

- Arena shooter
- Rocket jump mechanics
- Weapon pickups
- Power-ups
- Deathmatch or team modes

**What happens**:

- Spawn in arena
- Find weapons
- Fight
- Power-ups spawn
- Most kills wins
- Ranked matchmaking

**Why SpacetimeDB**:

- Player positions
- Weapon state
- Power-up spawning
- Kill tracking

**Money**: Free + $9.99/weapon pack + map packs

---

## I48. SLEDGEHAMMER FIGHT

**Pitch**: One weapon. One hit kills. Everyone has a sledgehammer.

**The Hook**:

- 20 players
- Sledgehammer only
- One hit = death
- Last player alive wins

**What happens**:

- Spawn in arena
- Find opponents
- Swing hammer
- Get hit = death
- Respawn as ghost
- Spectate until round ends
- Last alive wins round

**Why SpacetimeDB**:

- Player positions
- Swing detection
- Death state
- Round management

**Money**: Free + $2.99/arena + cosmetic ghosts

---

## I49. CAPTURE THE FLAG

**Pitch**: Classic CTF. 6v6. Grab enemy flag. Bring to base.

**The Hook**:

- Two teams
- Capture enemy flag
- Return to base
- Don't lose your flag

**What happens**:

- Grab enemy flag
- Run to your base
- Touch your flag to score
- Enemy can tag you to return flag
- Most captures wins

**Why SpacetimeDB**:

- Player positions
- Flag state
- Tag detection
- Score tracking

**Money**: Free + $3.99/map pack + uniform skins

---

## I50. WORM WARFARE

**Pitch**: Turn-based artillery. Dig, aim, fire. Classic Worms gameplay.

**The Hook**:

- Turn-based
- Aim and fire weapons
- Dig terrain
- Gravity and physics
- Last worm wins

**What happens**:

- Teams of worms
- Take turns
- Aim, set power
- Fire weapons
- Terrain destruction
- Last standing wins

**Why SpacetimeDB**:

- Turn state
- Projectile physics
- Terrain state
- Health tracking

**Money**: $9.99 + $3.99/weapon pack + map packs

---

---

# 🔥 THE SICKEST GAMES

*The "holy sh*t that's cool" ones\*

---

## 1. 1000 PLAYER BATTLE ROYALE

**Pitch**: Literally 1000 players in ONE match. Not 100. ONE THOUSAND.

**What happens**:

- 1000 players drop in
- Map is MASSIVE (size of small country)
- Vehicles, planes, boats - all real-time
- Zone shrinks over 30 minutes
- Last one standing wins

**Why SpacetimeDB**:

- Traditional servers choke at 100
- Scales horizontally across zones
- Each zone has own state machine
- Reducers handle eliminations atomically
- Views filter what's relevant (don't send 999 players to your client)

**Features**:

- Massive map with multiple biomes
- Dynamic weather
- Vehicle physics
- Loot distribution system
- Spectator mode (can watch 10,000+)

**Money**: $4.99/match + skins + battle pass

**MVP Scope**: 100 players first, scale up

---

## 2. PERSISTENT WORLD (Legacy Server)

**Pitch**: A world that NEVER resets. Everything you build stays. Your grandchildren inherit YOUR buildings. Generations build together.

**What happens**:

- MMORPG but world is player-built
- Build cities, kingdoms, roads, farms
- History is recorded: "King Arthur built this in Year 1"
- Archaeology: dig up ancient player structures
- World evolves over YEARS

**Why SpacetimeDB**:

- True persistence - data NEVER wipes
- Massive state that grows over years
- Event history for archaeology feature
- Real-time building sync across thousands

**Features**:

- Territory claiming
- Building permissions
- History logs
- Archaeology tool
- Generational inheritance system

**Money**: $14.99/month + cosmetic shop + name change

---

## 3. SPACE MMO (One Galaxy, Thousands Of Players)

**Pitch**: Eve Online but accessible. Build stations, form corporations, conquer territories, trade across star systems.

**What happens**:

- 1000+ star systems
- Build stations, gates, infrastructure
- Corporations control territory
- Player-driven economy
- Fleet battles with 500+ ships
- Real-time travel between systems

**Why SpacetimeDB**:

- Massive state (thousands of ships, stations)
- Complex economy with real-time prices
- Territory control with instant updates
- Fleet coordination without lag

**Features**:

- Star map with territory control
- Blueprint system for manufacturing
- Market orders and trading
- Corporation management
- Alliance system
- Ship customization

**Money**: $14.99/month + skins + corp fees

---

## 4. REAL-TIME HORROR (The Monster Is Human)

**Pitch**: 8 players trapped. One is THE MONSTER. Nobody knows who. Find clues. Barricade doors. Survive.

**What happens**:

- 7 survivors vs 1 monster (player-controlled)
- Monster: invisible, possesses objects, psychological terror
- Dynamic lighting - only seen in mirrors
- Sound is KEY: footsteps, breathing, whispers
- Survive 20 minutes OR banish the monster

**Why SpacetimeDB**:

- Monster position hidden but state exists
- Scheduled events for "haunting" moments
- Atomic possession mechanics
- Real-time audio/visual horror timing

**Features**:

- Possession system (possess objects, NPCs)
- Evidence gathering
- Barricade building
- Communication system (walkie talkies)
- Sanity meter
- Escape routes

**Money**: $9.99/game + monster skin packs

---

## 5. DRAWING BATTLE ROYALE

**Pitch**: 100 players. 60 seconds to draw. Everyone sees your drawing LIVE as you draw. Vote on best. Winner moves on.

**What happens**:

- 100 players, one prompt: "Draw a sad cat"
- 60 seconds to draw
- Others see strokes appear in real-time
- Vote, bottom 50% eliminated
- Repeat until 1 winner
- Clips of best drawings saved

**Why SpacetimeDB**:

- Drawing strokes sync in real-time
- Voting must be atomic
- Timer state critical
- Elimination updates instantly

**Features**:

- Canvas tools (brush, colors, eraser)
- Prompt database
- Voting system
- Elimination bracket
- Drawing replays
- Clip sharing

**Money**: Free + cosmetics + word packs

---

## 6. MASSIVELY MULTIPLAYER RHYTHM GAME

**Pitch**: 1000 players dancing in a virtual concert. Everyone's moves sync to the beat. Collective score creates visual effects.

**What happens**:

- Choose a song
- 1000 players on the dance floor
- Same notes, same timing
- Collective score = visual effects
- Climax: synchronized explosion of moves
- Compete for "best dancer"

**Why SpacetimeDB**:

- 1000+ timing inputs sync PERFECTLY
- Beat detection triggers effects globally
- Leaderboard per song updates in real-time
- Audio sync state critical

**Features**:

- Song library
- Note charts (like DDR)
- Group combos
- Visual effects engine
- Avatar customization
- Performance replays

**Money**: Free + $1.99/song + cosmetic outfits

---

## 7. GIANT ROBOT BATTLE (Mecha 50v50)

**Pitch**: 50 players on each side. You are ONE robot. Walk, run, shoot missiles, swing swords. Commander gives orders.

**What happens**:

- Choose class: speed, heavy, balanced
- 50v50 combat on massive maps
- Commander gives orders on map
- Objectives: destroy command center, hold points
- Upgrade parts between matches
- Seasonal story/lore

**Why SpacetimeDB**:

- 100 players in combat state
- Projectile/beam sync
- Damage calculation atomic
- Upgrade persistence

**Features**:

- Mech customization
- Ability system
- Commander interface
- Squad coordination
- Upgrade system
- Cosmetics

**Money**: $12.99/month + mech skins + weapon packs

---

## 8. OVERCOOKED ONLINE

**Pitch**: Overcooked but online with randoms. 4 players per kitchen. Orders come in. Fire, floods, sliding floors.

**What happens**:

- Join kitchen with 3 other players
- Orders with timers
- Stations: cutting, cooking, plating, delivery
- Hazards: fire, floods, collapsing floors
- Chat with text pings or voice
- Leaderboards for fastest service

**Why SpacetimeDB**:

- Order timers sync perfectly
- Station states update instantly
- Player positions sync
- Atomic dish completion

**Features**:

- Kitchen layouts
- Ingredient system
- Order queue
- Timer system
- Scoring system
- Level editor

**Money**: $7.99/game + recipe packs

---

## 9. TANK MMO (100 vs 100)

**Pitch**: Massive tank warfare. 100 players per side. Realistic physics. Commander gives orders. Artillery support.

**What happens**:

- Choose tank: heavy, medium, light, artillery
- Form squads of 4
- Commander gives orders on map
- Realistic ballistics
- Capture territory over time
- Campaign mode: win the war

**Why SpacetimeDB**:

- 200+ simultaneous players in combat
- Projectile physics sync
- Squad/commander coordination
- Territory state updates

**Features**:

- Tank classes
- Squad system
- Commander map
- Artillery calculator
- Territory control
- Campaign progression

**Money**: $14.99/month + tank skins + war bonds

---

## 10. PIRATE EMPIRE

**Pitch**: Be a pirate. Form a crew. Raid ships. Plunder ports. Build your empire. Alliance or betray.

**What happens**:

- Create pirate crew (guild)
- Sail massive ocean
- Raid merchant ships
- Attack ports for treasure
- Crews ally or go to war
- Treasure hunts: follow clues
- Become Pirate King

**Why SpacetimeDB**:

- Ship positions sync across huge map
- Crew management
- Loot distribution after raids
- Alliance/war coordination

**Features**:

- Ship building
- Crew management
- Treasure map system
- Port capturing
- Alliance system
- Reputation system

**Money**: Free + $9.99/month for captains + cosmetic sails

---

## 11. 100 PLAYERS vs ONE GIANT BOSS

**Pitch**: 100 players team up to fight a massive boss. Complex patterns. Players must coordinate. Phase changes.

**What happens**:

- Sign up for raid
- Boss has 4 phases
- Each phase: different mechanics
- Raid chat for coordination
- Loot drops for contributors
- Leaderboard: fastest kills

**Why SpacetimeDB**:

- Boss state syncs to 100 players
- Damage contribution tracking
- Loot distribution
- Phase transitions

**Features**:

- Boss AI system
- Phase mechanics
- Damage meters
- Loot system
- Raid chat
- Leaderboards

**Money**: Free + $4.99/skip queue + cosmetics

---

## 12. HAUNTED HOTEL (You Be The Ghost)

**Pitch**: You are the hotel manager. Guests come. The hotel is haunted. You control the ghosts. Scare them.

**What happens**:

- Host mode: control ghosts, set traps
- Guest mode: survive until morning
- 8 guests, 1 host per session
- Ghost abilities: possession, telekinesis, whispers
- Guest abilities: cleanse, hide, find cursed objects
- Leaderboard for best hosts

**Why SpacetimeDB**:

- Ghost state hidden from guests
- Event triggers sync
- Scare timing critical
- Session management

**Features**:

- Ghost possession
- Trap placement
- Object physics
- Evidence collection
- Mini-games (rituals)
- Room layouts

**Money**: $4.99/session as host + ghost packs

---

## 13. ESCAPE THE ALIENS

**Pitch**: Aliens invaded. 100 players. 3 real-time days to evacuate. Aliens evolve based on player actions.

**What happens**:

- 100 players, 3 "days" (2 hours each)
- Day: scavenge, build, prepare
- Night: alien attacks get worse
- Aliens adapt to tactics
- Get to evacuation ship or game over
- Server-wide outcome recorded

**Why SpacetimeDB**:

- Day/night cycle scheduling
- Alien AI state management
- Evacuation queue coordination
- Persistent world changes

**Features**:

- Alien evolution system
- Base building
- Resource gathering
- Crafting system
- Evacuation mechanics
- Event calendar

**Money**: $9.99/campaign + evolution packs

---

## 14. PERSISTENT ZOMBIE APOCALYPSE

**Pitch**: Entire server is one survival world. Day 1: infection begins. The world changes forever.

**What happens**:

- 500 players per server
- Infection starts in one city
- Players can become zombies (PvP)
- Base building persists
- Horde events: thousands attack
- Server achievements: "Cure discovered Year 2"

**Why SpacetimeDB**:

- Persistent world state
- Zombie AI coordination
- Base building persistence
- Event scheduling for hordes

**Features**:

- Zombie infection
- Base building
- Horde events
- Crafting system
- Faction system
- World evolution

**Money**: Free + skins + base insurance

---

## 15. DOMINO EFFECT

**Pitch**: Place a domino. It falls. Triggers something. Triggers something. Build Rube Goldberg machines across the entire game world.

**What happens**:

- Build with physics objects
- Connect to other players' creations
- Watch chains trigger in real-time
- Competition: longest chain wins
- Daily "drop" events: all chains run
- World records for longest chains

**Why SpacetimeDB**:

- Physics state atomic updates
- Chain triggers propagate correctly
- World-wide state
- Real-time trigger visualization

**Features**:

- Physics builder
- Object library
- Chain sharing
- World map
- Event system
- Leaderboards

**Money**: Free + $2.99/object packs + premium chains

---

## 16. FOOD FIGHT

**Pitch**: Two teams. Chaotic cooking battle. Throw food. Sabotage opponents. Serve customers.

**What happens**:

- 4v4 teams
- Cook: make food, serve customers
- Fighter: throw food, sabotage enemies
- Customers with orders
- Score: cooking + fighting
- Wild ingredients appear randomly
- Arena hazards: oil slicks, fires

**Why SpacetimeDB**:

- Two parallel game modes
- Score atomic updates
- Ingredient spawn scheduling
- Arena state

**Features**:

- Cooking system
- Combat system
- Customer AI
- Ingredient spawning
- Arena hazards
- Team coordination

**Money**: Free + $2.99/character skins + ingredient packs

---

## 17. DETECTIVE AGENCY

**Pitch**: Multiple detectives working same case. Share evidence. Interview witnesses. The killer might be watching.

**What happens**:

- 6 detectives per case
- Evidence board: pins, connections, notes
- Interview NPCs with schedules
- Real-time chat
- Killer can submit fake evidence
- Vote on suspects
- Solve or fail

**Why SpacetimeDB**:

- Evidence state shared in real-time
- Chat coordination
- Timer synchronization
- Case library

**Features**:

- Evidence board
- NPC interview system
- Chat system
- Vote system
- Case generator
- Time pressure

**Money**: $7.99/case pack + detective cosmetics

---

## 18. REALITY HACK

**Pitch**: Modify the game world with code. "Make all trees pink" - trees turn pink. Share your hacks.

**What happens**:

- Simple coding interface
- Modify game rules in real-time
- Changes affect everyone
- Share hacks with codes
- Weekly challenges
- Hacks can counter other hacks
- Sandbox mode

**Why SpacetimeDB**:

- Command execution atomic
- State modifications sync
- Hack library persisted
- Voting for best hacks

**Features**:

- Block-based coding
- Effect library
- Share system
- Challenge modes
- Sandbox area
- Leaderboards

**Money**: Free + $4.99/hack packs + creator program

---

## 19. LIVE GAME SHOW HOST

**Pitch**: Become a TV game show host. Design your own games. Invite friends or strangers. Control everything.

**What happens**:

- Host tools: questions, wheels, game flow
- Multiple modes: trivia, betting, elimination
- Audience mode: random people join
- Stream to Twitch directly
- Spectators bet in-game currency
- Replay with highlights

**Why SpacetimeDB**:

- Host actions broadcast instantly
- Wheel spin atomic
- Score state to all viewers
- Scheduled countdown timers

**Features**:

- Question builder
- Wheel spinner
- Game flow designer
- Audience system
- Betting system
- Replay system

**Money**: $9.99/month for hosts + ad revenue

---

## 20. WASTELAND SURVIVAL

**Pitch**: Post-apocalyptic. Huge open world. Scavenge, craft, build bases, form factions. The world tells stories.

**What happens**:

- Explore open wasteland
- Find loot: weapons, meds, tech
- Build persistent base
- Form factions
- Radiation storms sweep map
- Vaults to explore
- Crafting system
- Server history

**Why SpacetimeDB**:

- Massive persistent world
- Faction management
- Event scheduling
- Loot table coordination

**Features**:

- Open world exploration
- Base building
- Faction system
- Radiation events
- Vault dungeons
- Crafting system

**Money**: Free + $9.99/month + loot boxes

---

# 👥 PARTY GAMES

_Games for 2-8 players_

---

## 21. TRIVIA NIGHT LIVE

**Pitch**: Host trivia games with friends. Live scoreboard, buzzer rounds, custom question packs.

**What you get**:

- Live scoreboard
- Buzzer system (who answered first)
- Custom question packs
- Team mode
- Multiple rounds

**Why SpacetimeDB**: Buzzer submissions atomic. Views show live scores.

**Money**: $9.99/game host subscription

---

## 22. GAME NIGHT ORGANIZER

**Pitch**: Organize game nights. Scheduling, reminders, invite tracking, group chat.

**What you get**:

- Event scheduling
- RSVP tracking
- Reminders
- Group chat
- Game library

**Why SpacetimeDB**: RSVP updates sync instantly.

**Money**: $4.99/month per group

---

## 23. BOARD GAME LOBBY

**Pitch**: Find opponents for any board game. Matchmaking, lobby chat, spectator mode.

**What you get**:

- Game matchmaking (chess, Catan, etc.)
- Lobby with chat
- Turn timers
- Spectator mode
- Game library

**Why SpacetimeDB**: Player state real-time. Reducers handle turns.

**Money**: $5/month + Twitch integration

---

## 24. ESCAPE ROOM CO-OP

**Pitch**: Host escape rooms online. Teams solve puzzles together. Host can adjust difficulty live.

**What you get**:

- Pre-built puzzle rooms
- Host controls (hints, timer, difficulty)
- Team voice/text chat
- Clue sharing system

**Why SpacetimeDB**: Puzzle state syncs to all players.

**Money**: $14.99/room rental

---

## 25. TABLETOP RPG COMPANION

**Pitch**: DM manages combat, initiative, loot for online TTRPG sessions. Players see state update live.

**What you get**:

- Initiative tracker
- Combat log
- Loot distribution
- Character sheets
- Dice roller

**Why SpacetimeDB**: Combat state updates live.

**Money**: $9.99/DM/month

---

## 26. CARD BATTLE ROYALE

**Pitch**: 8+ players, last card holder wins. Live negotiations, alliances, backstabbing.

**What you get**:

- Live player elimination
- Negotiation phase
- Hidden role mechanics
- Spectator mode

**Why SpacetimeDB**: Player state real-time. Reducers handle elimination.

**Money**: $4.99/game + cosmetics

---

## 27. TRUST NO ONE (Social Deduction)

**Pitch**: 6-8 players complete missions while hiding secret agendas.

**What you get**:

- Secret objectives
- Trust scores visible to all
- Sabotage tools
- Mission phases

**Why SpacetimeDB**: Trust scores update live. Reducers handle objectives.

**Money**: $9.99/month + custom mission packs

---

## 28. CULT OF THE UNKNOWN GOD

**Pitch**: Players are cultists trying to summon an eldritch god before being discovered.

**What you get**:

- Ritual points
- Investigator role
- Eldritch events
- Final summoning ritual

**Why SpacetimeDB**: Ritual progress indexes by player. Events trigger at intervals.

**Money**: $4.99/campaign + ancient one expansions

---

## 29. HOTEL MURDER MYSTERY

**Pitch**: 6-12 players in a hotel. One is a killer. Clues appear in real-time.

**What you get**:

- Room exploration
- Real-time clue drops
- NPC interviews
- Accusation phase

**Why SpacetimeDB**: Clues sync instantly. Scheduled tables trigger drops.

**Money**: $12.99/case + custom scenarios

---

## 30. CORPORATE ESPIONAGE

**Pitch**: Players infiltrate a corporation as employees. Compete for promotions while sabotaging rivals.

**What you get**:

- Daily work tasks
- Corporate politics
- Sabotage system
- Board events

**Why SpacetimeDB**: Promotion votes atomic. Scheduled board events.

**Money**: $9.99/month + corporate skin packs

---

# ⚔️ COMPETITIVE GAMES

_PvP games with rankings_

---

## 31. TRADING CARD GAME MATCHMAKING

**Pitch**: Quick-match TCG with real-time combat. No server hosting needed. Private tournaments.

**What you get**:

- Deck builder
- Matchmaking queue
- Real-time card combat
- Private tournament mode
- Ranked ladder

**Why SpacetimeDB**: Combat state atomic. Views filter match history.

**Money**: $9.99/month + card pack purchases

---

## 32. REAL-TIME FANTASY SPORTS DRAFT

**Pitch**: Draft day feels like a war room. Real-time player availability, countdown timers, trade talks.

**What you get**:

- Live player availability grid
- Pick countdown timers
- Trade proposals
- Waiver wire management
- Live scoring

**Why SpacetimeDB**: Scheduled tables manage pick timers.

**Money**: $19.99/league/season

---

## 33. SPORTS WATCH PARTY

**Pitch**: Watch sports with friends online. Reactions sync in real-time. Prediction games score you points.

**What you get**:

- Sync'd video playback
- Emoji reaction storms
- Prediction contests
- Spatial voice chat
- Leaderboards

**Why SpacetimeDB**: Reaction feeds sync instantly.

**Money**: $9.99/month (ad-free + rewards)

---

## 34. COMPETITIVE PROGRAMMING ARENA

**Pitch**: Code fights in real-time. See opponent's code as they type. Watch execution visualize.

**What you get**:

- Real-time code streaming
- Execution visualization
- Instant leaderboard updates
- Live chat + moderation
- Multiple languages

**Why SpacetimeDB**: Reducers handle submission atomicity.

**Money**: $9.99/contest + sponsorships

---

## 35. ESPORTS TOURNAMENT PLATFORM

**Pitch**: Run esports tournaments. Live brackets, match tracking, spectator POV feeds.

**What you get**:

- Live bracket management
- Match result submission
- Spectator view (watch POVs)
- Anti-cheat hooks
- Prize distribution

**Why SpacetimeDB**: Reducers handle match results.

**Money**: $500/tournament + prize pool cut

---

## 36. PUZZLE RACES

**Pitch**: Race friends on daily puzzles. See their progress in real-time. Who finishes first?

**What you get**:

- Daily puzzle drops
- Real-time ghost progress
- Custom puzzle packs
- Weekly leaderboards

**Why SpacetimeDB**: Progress updates sync live.

**Money**: $4.99/month + puzzle pack store

---

## 37. RHYTHM GAME

**Pitch**: Dance/sync games together. See everyone's inputs. Compete on accuracy.

**What you get**:

- Sync'd beat charts
- Real-time accuracy scores
- Custom song uploads
- Performance replays

**Why SpacetimeDB**: Input timing atomic. Views show combo multipliers.

**Money**: $9.99/month + song store

---

## 38. REAL-TIME BOSS RUSH

**Pitch**: Speedrun bosses with friends. Shared lives. One dies, everyone resets.

**What you get**:

- Shared health pool
- Boss patterns
- Time attack
- Death counter
- Leaderboards

**Why SpacetimeDB**: Health state syncs instantly.

**Money**: Free + cosmetics

---

## 39. 1V1 FIGHTING GAME

**Pitch**: Simple fighting game. Quick matches. Ranked ladder. Character select.

**What you get**:

- Character roster
- Move list
- Ranked matchmaking
- Replay system
- Combo trials

**Why SpacetimeDB**: Hit detection atomic. Frame data syncs.

**Money**: Free + character skins

---

## 40. REAL-TIME CHESS VARIANTS

**Pitch**: Chess but with crazy variants. 960, atomic, crazyhouse. Quick matches.

**What you get**:

- Multiple variants
- Quick match queue
- Rated games
- Analysis tools
- Puzzles

**Why SpacetimeDB**: Move validation atomic.

**Money**: Free + premium variants

---

# 🌍 MMO & PERSISTENT WORLD

_Large-scale persistent games_

---

## 41. MEDIEVAL KINGDOM BUILDER

**Pitch**: 8-12 players compete to build the most prosperous medieval kingdom.

**What you get**:

- Build farms, mines, markets, barracks
- Trade resources with neighbors
- Form alliances or declare wars
- Weekly events

**Why SpacetimeDB**: Index lookups on resources. Procedures handle trade.

**Money**: $12/month + special building packs

---

## 42. SPACE STATION SIMULATION

**Pitch**: 4-8 players manage a failing space station. Systems are failing. Coordinate or die.

**What you get**:

- Power grid management
- Life support distribution
- Repair drones
- Security breaches
- Evacuation

**Why SpacetimeDB**: Sensor data streams from all players.

**Money**: $19.99/campaign + station customization

---

## 43. BLACK MARKET STOCK EXCHANGE

**Pitch**: Players are traders in an underground market dealing in contraband, data, and favors.

**What you get**:

- Real-time price fluctuations
- Snitch system
- Heist opportunities
- Front businesses

**Why SpacetimeDB**: Index lookups on commodity prices.

**Money**: $9.99/month + insider trading data packs

---

## 44. TIME TRAVEL PARADOX

**Pitch**: Players work together across different time periods to solve puzzles.

**What you get**:

- Players in 2024, 1924, 1824
- Actions in past affect future
- Paradox system
- Final puzzle coordination

**Why SpacetimeDB**: Views show era-specific state.

**Money**: $14.99/campaign + time period expansions

---

## 45. CREW OF THE NEBUCHADNEZZAR

**Pitch**: 4-player co-op looter shooter. Heist locations, fight guards, escape with loot.

**What you get**:

- Class roles (Tank, DPS, Support, Stealth)
- Loot extraction system
- Real-time heist planning
- Escalating enemies

**Why SpacetimeDB**: Real-time position sync. Loot atomicity.

**Money**: $19.99/heist pack + weapon cosmetics

---

## 46. DRAGON'S HOARD

**Pitch**: Players are dragons. Raid other players' lairs. Guard your own. Hatch eggs.

**What you get**:

- Real-time raid defense
- Egg hatching timers
- Treasure types
- Alliance system

**Why SpacetimeDB**: Scheduled tables manage hatch timers.

**Money**: $9.99/month + dragon customization

---

## 47. CARD GAME TOURNAMENT ROYALE

**Pitch**: 100 players start. Table-based card game elimination. Last table standing wins.

**What you get**:

- 10 players per table
- Winners advance
- Tribute system
- Final table high stakes

**Why SpacetimeDB**: Table rankings update in real-time.

**Money**: $5/tournament entry + card backs

---

## 48. WAR SIMULATION (50+ Players)

**Pitch**: Two factions battle over territory. Troop movements, resource management, base building.

**What you get**:

- Troop movement on map
- Resource nodes
- Base damage visible
- Territory control

**Why SpacetimeDB**: Massive sync of unit positions.

**Money**: $19.99/faction pack + cosmetics

---

## 49. CITY BUILDER MMO

**Pitch**: Build a city. Invite friends. Compete for population. Weekly challenges.

**What you get**:

- Zone placement
- Building placement
- Population tracking
- Weekly events
- Friend visits

**Why SpacetimeDB**: Building state persists. Events sync.

**Money**: Free + premium buildings

---

## 50. FANTASY RPG ADVENTURE

**Pitch**: Persistent RPG. Level up. Gear up. Raid dungeons. Trade with players.

**What you get**:

- Character progression
- Loot system
- Party system
- Dungeon raids
- Player trading

**Why SpacetimeDB**: Character state persists. Loot atomic.

**Money**: Free + cosmetics + XP boosts

---

# 🛠️ TEMPLATES & FRAMEWORKS

_Build-your-own game kits_

---

## 51. FPS MULTIPLAYER KIT

**Pitch**: Complete FPS template. Movement, shooting, scoring. Plug in your art.

**What you get**:

- Movement (running, jumping, crouching)
- Weapons (rifle, shotgun, sniper)
- Scoring and leaderboards
- Matchmaking
- Respawn system

**Money**: $199 one-time + hosting

---

## 52. TPS MULTIPLAYER KIT

**Pitch**: Third-person shooter template. Camera systems, cover mechanics, abilities.

**What you get**:

- TPS camera system
- Cover mechanics
- Ability system
- Role selection
- Match flow

**Money**: $249 one-time

---

## 53. MOBA FRAMEWORK

**Pitch**: Build your own League of Legends. Map, abilities, items, matchmaking.

**What you get**:

- 1 map (5v5)
- Ability system
- Item shop
- Minion AI
- Matchmaking
- Spectator mode

**Money**: $499 one-time + $99/month hosting

---

## 54. BATTLE ROYALE TEMPLATE

**Pitch**: Build your own PUBG. Zone, loot, inventory, matchmaking.

**What you get**:

- Zone system
- Loot spawning
- Inventory system
- Player stats
- Matchmaking
- Spectator mode

**Money**: $399 one-time

---

## 55. CARD GAME FRAMEWORK

**Pitch**: Build any card game. TCG, deckbuilder, solitaire.

**What you get**:

- Card database system
- Deck builder UI
- Card effects engine
- Turn system
- AI opponent
- Multiplayer sync

**Money**: $149 one-time

---

## 56. RTS FRAMEWORK

**Pitch**: Build your own Starcraft. Units, buildings, resources, fog of war.

**What you get**:

- Unit selection/movement
- Building placement
- Resource gathering
- Fog of war
- Unit AI
- 1v1 matchmaking

**Money**: $349 one-time

---

## 57. AUTO-BATTLER FRAMEWORK

**Pitch**: Build your own TFT. Units, synergies, items, rounds.

**What you get**:

- Unit database
- Synergy system
- Item system
- Round progression
- AI opponents
- Lobby system

**Money**: $199 one-time

---

## 58. TURN-BASED RPG FRAMEWORK

**Pitch**: Build your own Final Fantasy. Battles, parties, inventory, save system.

**What you get**:

- Turn-based battle system
- Party management
- Inventory system
- Save/load
- Shop system
- Quest tracker

**Money**: $249 one-time

---

## 59. ROGUELIKE FRAMEWORK

**Pitch**: Build your own Hades. Procedural dungeons, unlocks, meta-progression.

**What you get**:

- Procedural dungeon generator
- Room templates
- Enemy AI
- Meta-progression
- Unlock system
- Run history

**Money**: $179 one-time

---

## 60. VISUAL NOVEL ENGINE

**Pitch**: Build dating sims. Dialogue trees, sprites, backgrounds, choices.

**What you get**:

- Dialogue system
- Sprite management
- Background system
- Choice branches
- Save states
- Character routes

**Money**: $99 one-time

---

## 61. BOARD GAME ENGINE

**Pitch**: Build any board game. Catan, Monopoly, Chess.

**What you get**:

- Turn manager
- Rules engine (configurable)
- Dice/cards/spawners
- Victory conditions
- AI players
- Online multiplayer

**Money**: $149 one-time

---

## 62. PROCEDURAL WORLD GENERATOR

**Pitch**: Infinite terrain. Realms. Biomes. Generated on-the-fly.

**What you get**:

- Noise-based terrain
- Biome blending
- Chunk system
- LOD management
- Seed sharing
- Real-time modification

**Money**: $129 one-time

---

## 63. AI BEHAVIOR TREE ENGINE

**Pitch**: Advanced NPC AI. Decision trees, state machines, behavior trees.

**What you get**:

- Visual behavior tree editor
- State machine system
- Pathfinding integration
- Perception system
- Action system
- Debug tools

**Money**: $199 one-time

---

## 64. ECONOMY SIMULATION ENGINE

**Pitch**: Player-driven economies. Resources, crafting, trade, inflation.

**What you get**:

- Resource system
- Crafting recipes
- Trade system
- Market simulation
- Price history
- NPC merchants

**Money**: $149 one-time

---

## 65. COMBAT SYSTEM TOOLKIT

**Pitch**: Complete combat system. Melee, ranged, abilities, effects, hit detection.

**What you get**:

- Melee combat
- Ranged combat
- Ability system
- Hit detection
- Effects/particles
- Damage calculations

**Money**: $179 one-time

---

---

# 📊 BY PLAYER COUNT

| Players | Games                                                            |
| ------- | ---------------------------------------------------------------- |
| 2       | FPS Kit, TPS Kit, Chess Variants, 1v1 Fighting                   |
| 2-4     | Overcooked, Food Fight, Detective Agency, Trivia Night           |
| 4-6     | Horror, Heist Sim, Space Station, Escape Room, TTRPG             |
| 4-8     | Card Battle Royale, Trust No One, Cult of Unknown, Haunted Hotel |
| 6-12    | Drawing Battle, Hotel Murder, Corporate Espionage                |
| 8-12    | Realm Wars, Zombie Outbreak                                      |
| 10-20   | Pirate Empire, Time Travel                                       |
| 20-50   | Tank MMO, Giant Robot Battle, War Simulation                     |
| 50-100  | Boss Battle, War Sim                                             |
| 100+    | 1000 Player BR, Persistent World, Space MMO, Rhythm Game         |
| 1000+   | MMORPG, Rhythm Game, Persistent World                            |

---

# 💸 MONEY MAKERS

| Rank | Game             | Why                       |
| ---- | ---------------- | ------------------------- |
| 1    | Space MMO        | Eve Online makes billions |
| 2    | Persistent World | Subscriptions forever     |
| 3    | 1000 Player BR   | Mass appeal               |
| 4    | MMORPG           | Standard MMO model        |
| 5    | Drawing Battle   | Low cost, high retention  |

---

# 🏃 START HERE

| #   | Game             | Why Easy                  |
| --- | ---------------- | ------------------------- |
| 1   | Drawing Battle   | Simple concept, clear MVP |
| 2   | Detective Agency | Text/chat-based mostly    |
| 3   | Food Fight       | Simple mechanics          |
| 4   | FPS Kit          | Well-documented template  |
| 5   | Trivia Night     | Straightforward to build  |

---

_Last updated: 2026_

---

# 📎 APPENDIX: Legacy “Idea Cards” (more structured)

Pulled forward from `DOCS/legacy/SPACETIMEDB_IDEAS_AAA.md` to make future additions easier to scope, price, and pitch.

## Example cards (condensed)

### Eclipse City: Real-Time Open-World MMO-lite
- **Pitch**: persistent districts; 100–200 players/shard; player-run economy + governance
- **What you get**: storefronts/district ownership; realtime city events; live NPC economy; governance panels
- **SpacetimeDB fit**: region tables + atomic transactions; scheduled events; per-district views/subscriptions
- **Monetization**: district premiums; city services microtx; cosmetic map skins
- **MVP scope**: 2 districts; ~50 players/shard; basic storefronts/events + core governance

### Neon Hyperrace: Real-Time Online Racing
- **Pitch**: anti-grav racing with realtime track hazards + rivalry interactions
- **SpacetimeDB fit**: realtime position updates; track-state tables; subscriptions for leaderboards/replays
- **Monetization**: race passes; cosmetics; track packs
- **MVP scope**: limited tracks; core collision + lap timing

### Astral Heist: Real-Time Space Heist
- **Pitch**: 5–6 player crew heists with simultaneous actions + realtime alert cascades
- **SpacetimeDB fit**: atomic loot distribution reducers; event-driven security alerts; scheduled reinforcements
- **Monetization**: heist packs; cosmetics; DLC ships
- **MVP scope**: 1 ship; 2 heists; a couple loadouts/roles
