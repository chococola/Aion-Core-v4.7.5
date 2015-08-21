**Today, I've decided to open my Aion-Core Full Source to world.** WHY? cuz **Aion Developer Community** is really dead and No one interested to develop any-more and all just wait for others to make/implement some new features and **STEAL IT**. So the Aion Project is over for me and I'll return to better game communities with Pro Coders such as **Call of Duty Series**, **BattleField3-4 Series**, ...

**Note**: I implemented Full **Commercial Licensing System (Client/Server)** for Aion-Core Community for protecting my works but **NOW I REMOVED IT** and ***This is my Full Source with all features v4.7.5.x (NO LICENSE SYSTEM)***


**I NEVER SHARE MY LICENSE SYSTEM TO WORLD AND NO ONE HAS ITS SOURCE CODE. SO ALL SHARS WITHOUT MY NAME IS FAKE.**


Here is some of new features Implemented by @GiGatR00n:

1.  Fully Source Clean-up which makes it **3x faster** than before

2.  [Idgel Dome v4.7](https://www.youtube.com/watch?v=ssAScomOwp4) is fully implemented:

		Features:
		=========

		1). All Instance features and Mobs are fully coded and working retail like.
		2). Full Drop Items (Kunax ArmorSet, WeaponSet, Accessories)
		3). Boss Skills (Ide Scale, Aggressive Shot, Slaughtering Cleave, Cleaving Massacre, Howl of Emptiness, Fierce Roar (Full), ...)
		4). Mobs Skills (Attack Skills vs. Heal and Rage Skills) even more accurate than NcSoft System
		5). Instance BUFFs (Resurrection)
		6). Environment Factors + Skills (Unstable Ide Energy, Ide Explosion, ...)
		7). ShallowWater fully coded using new mathematics formula (It more accurate than NCSoft)
		8). New AI System for controlling Boss and Mobs
		9). New Tribe "Invulnerable" for Creatures
		10). Chests (Aether Bomb, Freeze Bomb, Defensive Scroll)
		11). Rewards (AbyssPoints, GloryPoints, Boxes, ...) with Config for each of them
		12). Anti-Cheat System for Emulating Packets and getting more rewards (No one can trick to system)
		13). All Hidden NPCs fully coded and implemented as Retail.
		14). any many more ...

3.  Fully Implemented **Broker System v4.7.5.x**

		1). Config file:  "broker.properties"
		2). All Packets Fully Implemented
		3). New Selling System Implemented
		
				SellAll
				SellSplit
				
		4). New Selling Hours Implemented
		5). MySQL DB Updated to Cover New Selling System (New Field Added)
		6). Broker Config Implemented for Admins (Expired Period, Anti-Hack Punishment, ...)
		7). Fixed settle_time for Broker Items
		8). Buy/Sell/Search/ExpiredItems/SetteledAccount

		
4.  **Hotspot Teleport Service** + Config files

		1).  Config file:  "custom.properties"
		
					# ---------------------------------------------
					# HOTSPOT TELEPORT (By GiGatR00n v4.7.5.x)
					# ---------------------------------------------
					# Set the Teleportation Delay in Milliseconds
					gameserver.hotspot.teleport.delay = 10000
					# Set Teleportation Cooldown Time in Seconds
					gameserver.hotspot.teleport.cooldown.delay = 600
					
		2).  Observer to verify whether the player is in Action(Move,UseSkill,Die,Attacked,...) while Teleporting? if so, Cancel Teleportation

5.  Fully Implemented **Multi-Return Scrolls v4.7.5.x**

		1).  Config file:  "ReturnScrolls.properties"
		2).  Added Full Parser + Source for Scrolls (It can be used for other XML files too)	
		
6.  Fully implemented "**Invulnerable**" Tribe (Even in Skills)

7.  Updated **SM_ATTACK** for all new v4.7.5 to v4.8 Instances

		Note:
			 Now all two way Bosses/Monsters can attack both <Ground> and <onAir> Units
			 from v4.7.x.x Bosses like <Destroyer's Kunax> have Two types of AutoAttack

8.  95% full **npc_trade_list.xml** (Reparsed and Reworked)

9.  Fully Updated "**MathUtil Class**" to handle new features of v4.7.5.x Instances like Shallow-Watter, Poisons, ...

		Idian Depths, Idgel Dome, Danuar Reliquary, ... have these types of hidden NPCs and now we can handle all of them
		
10. Fixed Base Flag Checking to prevent attackers to capture same base

		Fixed and Updated Tribe Relation Service that cuzed Monsters attack each other wrongly
		Added new NpcType (Invulnerable) for packet SM_NPC_INFO that implemented in v4.7.5 (Used in IdgelDome and Pangea Siege)
		Fixed Base Flag Checking to prevent attackers to capture same base
	
11. Fully Updated **.support** and **//ticket**  Admin/Player Commands

		Syntax: .ticket "Your Issue"
		Syntax: //ticket <accept | peek>

		====================================
		From: GiGatR00n:65:ELYOS:gladiator
		this is first test of support system
		====================================

13. Implemented **GarbageCollector Service** to free unused heap memory (Useful when running GameServer for long period)

		Enable/Disable using gameserver.properties
		Default, Every 5-Minutes Optimization Process will be launched
	
12. Updated GarbageCollector for handling AdminCommand //reload config	
	
14. Implemented  **in-Game Admin Symbols** (for the first time without any Limitation)

		You can change any combination you want
		Even Members VIP/Premium can have double symbols
		from  **\uE000** to **\uE0CE**   you can add symbols
		
		e.g.  **Crown**: \uE0BD,   **Wings**: \uE042 \uE043
		
		\uE0BD \uE042 **Admin** \uE043 %s \uE0BD
		\uE06F \uE042 **Supporter** \uE043 %s \uE06F
		\uE04E \uE042 **Junior-GM** \uE043 %s \uE04E
		
15. All Weather-Tables v4.7.5.x (**Danuar Mysticarium**, **Unity Training Grounds**, **Legion's Danuar Mysticarium**, **Idgel Storage**)

		Updated Many NPCs Shouts such as (IDCT_Boss_ArchPriest_Hard, IDCT_Boss_DeathKnight_Hard, IDCT_Boss_ElementalFire_Hard, IDCT_Boss_Shulack_Hard, IDCTH_Boss_StatueDrakan, IDCTH_Rudra)
		Added Many Decomposable Items
	
16. **In-Game Packets Sniffing** (Show CM/SM Packets Name + Hex-Bytes in Chat Window)

		1).  Its Usage:

		   - Finding Missing Bytes
		   - Analyzing when CM/SM Packets sent/received
		   - Reordering CM/SM Packets
		   - Reconstructing Packets
		   - Filtering Packets eg. SM_MOVE, CM_CASTSPELL, CM_ATTACK
		   
		2).  Config file: "developer.properties"

				# ------------------------------
				# Packets Proccessing Settings
				# (By GiGatR00n v4.7.5.x)
				# ------------------------------
				# Display Packets Name for Developers only (Only Console Window)
				# Default: false
				gameserver.developer.showpackets.enable = false

				# Display Packets Name or Hex-Bytes in Chat Window
				# Default: false
				gameserver.developer.show.packetnames.inchat.enable = false
				gameserver.developer.show.packetbytes.inchat.enable = false

				# Total Packet Bytes should be shown in Chat Window?
				# Default: 200-Hexed bytes
				gameserver.developer.show.packetbytes.inchat.total = 200

				# Filters which Packets should be shown in Chat Windows?
				# Default: * (All Packets Shown)
				# e.g.  SM_MOVE, CM_CASTSPELL, CM_ATTACK
				gameserver.developer.filter.packets.inchat = *

				# if the Player Access Level is meet, display Packets-Name or Hex-Bytes in Chat Window 
				# Tip: Player Access-Level higher than 3 is recommended
				#
				#   10 - Server-Owner
				#   9 - Server-CoOwner
				#   8 - Root-Admin L3
				#   7 - Root-Admin L2
				#   6 - Root-Admin L1
				#	5 - Admin
				#	4 - Head-GM
				#	3 - GM
				#	2 - Jr.-GM
				#	1 - Supporter
				#	0 - Players
				#
				gameserver.developer.show.packets.inchat.accesslevel = 3

17. 100% full **Gatherable_Templates.xml** (Reparsed and Reworked)

18. Fixed Buy_Trade_in_Trade for Kaisinel & Other Shops

		Updated  CM_BUY_TRADE_IN_TRADE  +  Services to be able to purchase different kind of items
		Added **Anti-Cheat System** to Prevent Client Hack
		Fixed some missing parts on Game Server	

19. Fully Updated **Tuning Items** that cuz Client-Crash after Right-Click

20. Updated pets.xml  to  4.7.5.18  (but need to implement MERCHANT, BUFF type)

		Added Normal Pets (Ailu Claw, Cheering Dandi, Tiamat Whelp, Bottlenose Tion, Red Bulldozer of Glory)
		Added MERCHANT, BUFF Pets (Squeeble, Pinkybell, Shu-Ghost, Royal Kitter, Kennercan)
	
21. Many Quests got fixed
22. Fully Added **Plume Stat** (**Attack**|**MagicBoost** + **HP** Boosts)

		Added Opcodes too

23. Fixed **Character Deletion**.

		Fixed and Updated Packets SM_CHARACTER_LIST & AccountService
		Fixed Relog for Deletion Chars
		Fixed Java Data Types Conversion Bug

24. Added new config for "**Regular**, **Premium**, **VIP**" within  **membership.properties**  &  **gameserver.properties**
25. Fully Added "**Assured Greater Felicitous Socketing**"
26. Fully Added Opcodes, Protocols, XML Tags for **decomposable_selectitems.xml** to v4.7.5.x
27. Updated **Server Game Time Bug** to v4.7.5.x

28. Fully Updated  **skill_templates.xml**  to v4.7.5.x (90% All Skils got fixed/added)

29. Fully Updated  **item_random_bonuses.xml**  to v4.7.5.x

30. Fully Updated  **item_random_bonuses.xml**  to v4.7.5.x

31. Fully Updated  **recipe_templates.xml**   to v4.7.5.x

32. Fully Updated  **flypath_template.xml**,  **npc_teleporter.xml**   to v4.7.5.x

33. Fully Updated  **polymorph_panels.xml**  to v4.7.5.x

34. Fully Fixed **Item Remodel Service v4.7.5.x**

		Opcodes Changed

35. Fully Updated  **instance_cooltimes.xml**  to v4.7.5.x

36. Fully Updated  **world_maps.xml**  to v4.7.5.x

37. Fully Implemented **Skill's Animations** v4.7.5.x

38. Many Opcodes got updated to v4.7.5.x

and so on

Don't ask any question regarding code, bugs, compiling, ... Just use as is (**NO SUPPORT**)

The last Words:
If you'r really Pro Coder (Java & C++) and want to assist me, Call me on skype: **GiGatR00n**
