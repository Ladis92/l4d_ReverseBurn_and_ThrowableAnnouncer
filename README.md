### `ReverseBurn and ThrowableAnnouncer`
(l4d_ReverseBurn_and_ThrowableAnnouncer) by *_Mystik Spiral_*  

Smart reverse of burn damage from throwables (molotovs) if the victim is burned instantly and continuously.  
It was created to help mitigate the damage by griefers attempting to kill/incap their teammates by burning them.  

Reverses the following throwable burn types:  
Molotov.

Announces the following throwable types:  
Molotov, pipe bomb, and bile jar.  


Features:  
- Burn damage is reversed only if victim(s) are burned instantly (within 0.75 second of ignition) and continuously (takes burn damage more than once per second).  
- If player runs into fire more than 0.75 seconds after ignition, burn damage is treated normally.  
- When burn damage is reversed, during each burn cycle (approximately 6x per second):  
	* Attacker takes 70% damage for each instantly/continously burned victim.  
	* Standing burn victims lose 1PermHP which is converted to 2TempHP as incentive to move out of the fire quickly.  
	* Before ignition, any players already incapped or with only 1TotalHP do not take any burn damage.  
- Bots do not take burn damage but do move out of the fire as quickly as possible.  
- In all other scenarios, burn damage behaves normally.  

Common Scenarios:  
- Griefer attempts to kill the whole team by burning them.  
Usual end result: Griefer takes 210% damage (70% per victim x 3 victims) plus possible additional self-damage and everyone else takes relatively minor damage.  

- Player starts fire (which does not burn anyone within 0.75 seconds) and griefer runs into it.  
Usual end result: Griefer takes normal damage and player that started the fire takes no damage.  

Suggestion:  

Use this plugin in conjunction with:  

**[ReverseBurn and ExplosionAnnouncer](https://forums.alliedmods.net/showthread.php?t=331164)** (l4d_ReverseBurn_and_ThrowableAnnouncer)  to reverse explodable (gascan, fireworks, etc.) burn types.  
...and...  
**[Reverse Friendly-Fire](https://forums.alliedmods.net/showthread.php?t=329035)** (l4d_reverse_ff) to reverse throwable (molotov) burn types.  

When these plugins are combined, griefers cannot inflict friendly-fire, and it minimizes damage to victims for throwable (molotov) and explodable (gascans, fireworks, etc.) burn types.  
Although griefers will take significant damage, other players may not notice any difference in game play (other than laughing at stupid griefer fails).  

Credits:  

This plugin began life as **[Throwable Announcer](https://forums.alliedmods.net/showthread.php?t=327613)** by Marttt.  The original plugin kept track of throwable entities, when they were thrown, and announced who did it. I hooked on to that announcement to track whether that throwable (molotov) instantly burned any other players, and if so, to ensure the attacker took the vast majority of the damage. If no other players are instantly burned, then burn damage is treated normally.  

Want to contribute code enhancements?
Create a pull request using this GitHub repository:  
https://github.com/Mystik-Spiral/l4d_ReverseBurn_and_ThrowableAnnouncer  

Plugin discussion: https://forums.alliedmods.net/showthread.php?t=331164  

The phrases file (l4d_ReverseBurn_and_ThrowableAnnouncer.phrases.txt) is REQUIRED and must be copied to the "addons\sourcemod\translations" directory.
