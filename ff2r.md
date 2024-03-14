---
layout: default
---

# FF2R CFGS

**all cfg here are used for tfoc server.**

**some of them not mine. I just port it into rewrite.**

[Source file - TFOC INNER CIRCLE](https://github.com/Zell3/TFOC-INNER-CIRCLE)

### Rage Server Command
```js
"rage_servercommand" // Ability name can use suffixes & prefixes
  { 
    "slot"             "" // Ability Slot

    "distance"         "" // distance (work only mode is 0)
    "duration"         "" // duration (time between excecute startcomm and end comm)
    "startcommand"     "" // command
    "startparam"       "" // parameter (ex. sm_blind @red 10 : '10' is parameter)
    "endcommand"       "" // same with startcommand
    "endparam"         "" // same with startparam
    "mode"             "" // 0 = on player , 1 = on server , 2 = on boss , 3 = boss excecute

    "plugin_name"     "ff2r_servercommandrage"
  }
```

* * *

### TFCond
#### Charge TFCond
```js
"charge_tfcondition" // Ability name can't use suffixes or prefixes, no multiple instances
{
  "arg0"        "1" // Charge slot can be 1 or 2
  "arg1"        "1.5" // Time to fully charge
  "arg2"        "5.0" // Cooldown after use
  "arg3"        "25.0" // RAGE Cost to use

  "selfconds"   "28 ; 10 ; 66 ; 7" // Boss Conditions (TFCond ; Duration)
  "allyconds"   "5 ; 2.7" // Ally conditions
  "allyrange"   "1024.0" // Ally range
  "enemyconds"  "27 ; 7.7 ; 24 ; 7.7" // Enemy conditions
  "enemyrange"  "1337.0" // Enemy range

  // HUD text Position
  "Position"    "-1.0 ; 0.88"

  // HUD - charge status
  "TEXTcharge"   "TFConditions is %i percent ready. When at 100 percent look up and stand up."    
  "RGBAcharge"   "255 ; 255 ; 255 ; 255"
  // HUD - cooldown status
  "TEXTcooldown" "TFConditions will be avaliable in %i second(s)."    
  "RGBAcooldown" "255 ; 64 ; 64 ; 255"
  // HUD - Charge uses RAGE
  "TEXTready"    "Alt-fire to use TFConds!"            
  "RGBAready"    "64 ; 255 ; 64 ; 255"
  // HUD -  Super-duper jump
  "TEXTDuper"    "Super Duper jump is ready!"                        
  "RGBADuper"    "255 ; 64 ; 64 ; 255"

  "buttonmode"    "1" // 1 for alt-fire/duck , 2 for reload

  "plugin_name"   "ff2r_tfcond"
}
```

#### Special TFCond
```js
"special_tfcondition" // Ability name can't use suffixes or prefixes, no multiple instances
{
  "slot"           "0" // Ability slot
  "selfconds"      "28 ; 32" // Conditions boss receives upon activation
  "allyconds"      "5 ; 2.7" // Ally conditions
  "allyrange"      "1024.0" // Ally range
  "enemyconds"     "27 ; 7.7 ; 24 ; 7.7" // Enemy conditions
  "enemyrange"     "1337.0" // Enemy range
  "ragemin"        "20.0" // Minimum required RAGE to use
  "ragedrain"      "0.04" // RAGE Drain RATE per tick
  "buttonmode"     "1" // Buttonmode (0=Alt-fire, 1=RELOAD, 2=SPECIAL)
  "cooldown"       "3" // Start count after stop using ability

  // HUD - NORAGE : Rage is not enough
  "POSnorage"      "-1.0 ; 0.88" // Position of text
  "TEXTnorage"     "Insufficient RAGE! You need a minimum of %i percent RAGE to use!"
  "RGBAnorage"     "255 ; 64 ; 64 ; 255" // Colour of text

  // HUD - READY : Rage is enough
  "POSready"       "-1.0 ; 0.88" // Position of text
  "TEXTready"      "Hold R to use the Condition Powerup"
  "RGBAready"      "64 ; 255 ; 64 ; 255" // Colour of text

  "plugin_name"    "ff2r_tfcond"
}
```

#### Rage TFCond
```js
"rage_tfcondition" // Ability name can use suffixes & prefixes
{
  "slot"          "0" // Ability slot
  "selfconds"     "5 ; 5.8" // Self conditions
  "allyconds"     "5 ; 2.7" // Ally conditions
  "allyrange"     "1024.0" // Ally range
  "enemyconds"    "27 ; 7.7 ; 24 ; 7.7" // Enemy conditions
  "enemyrange"    "1337.0" // Enemy range
    
  "plugin_name"    "ff2r_tfcond"
}
```

#### Tweak TFCond
```js
"tweak_tfcondition" // Ability name can't use suffixes or prefixes, no multiple instances
{
  "selfconds"    "11 ; -1.0" // Self conditions
  "allyconds"    "5 ; 20.0" // Ally conditions
  "remove allyconds on boss death"    "true" // Remove allyconds on boss death
  "apply allyconds upon respawn"      "true" // Apply allyconds to allied players when they are respawn 
  // (Only unlimited duration conditions re-apply & conditions don't re-apply if boss is dead)
                                  
  "enemyconds"   "27 ; 7.7 ; 24 ; -1.0" // Enemy conditions
  "remove enemyconds on boss death"   "true" // Remove enemyconds on boss death
  "apply enemyconds upon respawn"     "true" // Apply enemyconds to enemy players when they are respawn
  // (Only unlimited duration conditions re-apply & conditions don't re-apply if boss is dead)

  "plugin_name"    "ff2r_tfcond"
  }
```

* * *

### FOG
#### Rage Fog
```js
"rage_fog_fx" // Ability name can use suffixes & prefixes
{    
  "slot"        "0" // Ability slot
  "dalay"       "0" // Prefer using Doslot Abilities
  //colors
  "color1"      "0 0 0" // RGB colors
  "color2"      "0 0 0" // RGB colors
    
  // fog properties
  "blend"       "0" // blend
  "fog start"   "64.0" // fog start distance
  "fog end"     "384.0" // fog end distance
  "fog density" "1.0" // fog density
    
  // effect properties
  "effect type" "0" // fog effect: 0: Everyone, 1: Only Self, 2:Team, 3: Enemy Team, 4: Everyone besides self
  "duration"    "5.0" // fog duration
  
  "plugin_name" "ff2r_fog"
}
```

#### Tweak Fog
```js
"fog_fx" // Ability name can't use suffixes or prefixes, no multiple instances
{
  //colors
  "color1"      "0 0 0" // RGB colors
  "color2"      "0 0 0" // RGB colors
    
  // fog properties
  "blend"       "0" // blend
  "fog start"   "64.0" // fog start distance
  "fog end"     "384.0" // fog end distance
  "fog density" "1.0" // fog density
    
  // effect properties
  "effect type" "0" // fog effect: 0: Everyone, 1: Only Self, 2:Team, 3: Enemy Team, 4: Everyone besides self
  
  "plugin_name" "ff2r_fog"
}
```

* * *

### Special Mann up Lines
```js
"special_mann_up_lines" // Ability name can't use suffixes or prefixes, no multiple instances
{
  "plugin_name"    "ff2r_mann_up_abilities"    
}
```

* * *

### Rage Projectile
```js
"rage_projectile" // Ability name can use suffixes & prefixes
{
  "name"         "tf_projectile_rocket" // Projectile Name
  "velocity"     "1100.0" // Velocity 
  
  //The following Arguments are only required if Projectile is not spell
  "mindamage"    "" // min damage
  "maxdamage"    "" // max damage
  //"models"     "" // Overriden New Projectile Model
  "crits"        "1" // -1:Random Crits, 1:Crit, 0:No Random Crits

  "plugin_name"  "ff2r_castprojectile"    
}
```

* * *

### Revive Marker
```js
"special_revivemarker" // Ability name can't use suffixes or prefixes, no multiple instances
{
  "lifetime"      "45.0" //  Marker Lifetime
  "limit"         "3" //  Player Revive Limit
  "condition"     "" //  Player Conditions When Respawn
  "sound"         "1" //  1 = Play MvM Sounds, 0 = not
		
  "plugin_name"   "ff2r_revivemarker"
} 
```

* * *

### Rage Do Slot
```js
"rage_doslot"	// Ability name can use suffixes & prefixes
{
  "slot"        "0" // Ability Slot
  "delay"       "3.0" // Delay before first use
  "doslot"      "20" // Trigger Slot

  "plugin_name"	"ff2r_doslot"	// Plugin Name
}
```

### Dark Realm's Erandicator Abilities
#### Dark Realm's Passive
```js
"darkrealm_passive" // Ability name can't use suffixes or prefixes, no multiple instances
{
  // start round - melee
  // melee damage x (1 + (meleemultiplier * kills after round start))
  "meleemultiplier"   "0.05"
	
  // 5 kills - loose cannon
  // loose cannon damage x (1 + (cannonmultiplier * kills after 5 kills))
  "cannonmultiplier"  "0.05"      

  // 12 kills - loose cannon now have big explosion

  // 15 kills - all multiplier
  // melee damage x (1 + (meleemultiplier * kills after round start) + (allmultiplier * kills after 15 kills))
  // loose cannon damage x (1 + (cannonmultiplier * kills after 5 kills) + (allmultiplier * kills after 15 kills))
  "allmultiplier"     "0.10"

  "plugin_name"     	"ff2r_darkrealm"	// Plugin Name
}
```

#### Dark Realm's Rage Do slot
```js
"darkrealm_rage" // Ability name can use suffixes & prefixes
{
  "slot"      "0"
  "kill"      "5" // How many kills need to trigger that slot
  "doslot"    "" // Slot that will be trigger

  "plugin_name"	"ff2r_darkrealm" // Plugin Name
}
```

* * *

### Gentlemen / Spector Abilities
```js
"rage_specter" // Ability name can use suffixes & prefixes
{   
  "slot"         "0" // Ability Slot
  "duration"     "6.0" // Duration
  "range"        "800.0" 	// Range (leave blank to use default)
  "message"      "You are now Gentmen's Henchman"
  "lastman"      "true"			// prevent to change all player team if they no more player left in their team : true = yes false = no
  "playerleft"   "3"			// how many player won't get team change (needed when lastman = true : default = 1)

  "plugin_name"  "ff2r_specter"	// Plugin Name
}
```

* * *

### Hack / "Dominated" Shiranui Abilities
```js
"ability_shiranui" // Ability name can't use suffixes or prefixes, no multiple instances
{   
  "cost"      ""  // rage cost per use
  "duration"  ""  // Time being hacked - 0 means forever
  "lastman"   ""  // 1-If only one player disable hack ability 0-No disable
  
  "plugin_name"  "ff2r_shiranui"
}
```

* * *

### Aimbot
```js
"aimbot" // Ability name can use suffixes & prefixes
{
  "slot"         "0" // Ability Slot
  "duration"    "8.0" // time of ambotakam      
  "plugin_name" "ff2r_aimbot"
}
```

* * *

### Hook for player
```js
"hooks_for_players" // Ability name can't use suffixes or prefixes, no multiple instances
{ 
  "attributes"  "241 ; 0 ; 280 ; 26 ; 547 ; 0 ; 199 ; 0 ; 712 ; 1 ; 2025 ; 2 ; 2014 ; 1 ; 191 ; -7 ; 128 ; 1"
  "quality"     "8"
  "level"       "1"
  "rank"        "21"
  "show"        "1" // 0 = not show, 1 = show

  "team"        "1" // Who should get a hook? (0 = Boss + Player, 1 = Players only, 2 = Boss only)

  "plugin_name"   "ff2r_special_hooks"
}	
```

* * *

### Darthmule Condition
```js
"rage_condition" // Ability name can use suffixes & prefixes
{
  "slot"         "0" // Ability Slot
  "condition"   "" // 0 IGNITE , 1 BLEED , 2 STRIP TO MELEE , 3 BONK STUN
  "duration"    ""
  "distance"    ""

  "plugin_name" "ff2r_darthmule_stripped"
}
```

* * *

### Phatrages
#### Ioncannon
```js
"rage_ioncannon" // Ability name can use suffixes & prefixes
{
  "slot"         "0" // Ability Slot 
  "timer"       "" // Timer    (How long it takes for the ion cannon blast to hit it's target in seconds.) 
  "radius"      "" // Blast Radius    (Blast radius in units.) 
  "damage"      "" // Blast Damage    (Amount of damage delivered by the blast.) 
  "aimmode"     "0" // Aim Mode     (0 = where boss is standing. 1 = where boss is looking.)
  "rgba"        "0 0 0 255" // Colour

  "plugin_name"	"ff2r_phatrages"  
}
```

#### Delirium
```js
"rage_delirium" // Ability name can use suffixes & prefixes
{
  "slot"        "0" // Ability Slot
  "range"       ""  //Range
  "duration"    ""  //Duration

  "plugin_name"	"ff2r_phatrages"  
}
```

#### Hellfire
```js
"rage_hellfire" // Ability name can use suffixes & prefixes
{ 
  "slot"                "0" // Ability Slot
  "sound"               "" // Sound (true = No flame sound. false = Play flame sound.)  
  "damage"              "" // Damage (Amount of damage delivered by the initial fire blast.) 
  "range"               "" // Range (Radius of fire blast.) 
  "afterburn damage"    "" // Afterburn Damage (Amount of damage delivered by afterburn.) 
  "afterburn duration"  "" // Afterburn Duration (Duration of afterburn in seconds.)

  "plugin_name"         "ff2r_phatrages"  
} 
```

#### Scaleboss
```js
"rage_scaleboss" // Ability name can use suffixes & prefixes
{
  "slot"        "0" // Ability Slot
	"scale"			  "2.0" // Scale Factor (Resize the boss by this factor.) 
	"duration"		"" // Duration (Duration of resized effect in seconds.)
		
	"plugin_name"	"ff2r_phatrages"  
}
```

#### Scaleplayer
```js
"rage_scaleplayers" // Ability name can use suffixes & prefixes
{
  "slot"        "0" // Ability Slot
  "scale"       "2.0" // Scale Factor (Resize players by this factor.) 
  "duration"    "" // Duration (Duration of resized effect in seconds.) 
  "range"       "" // Range (Range of resizing effect.)

  "plugin_name"	"ff2r_phatrages"  
}
```

#### Drown
```js
"rage_drown" // Ability name can use suffixes & prefixes
{
  "slot"        "0" // Ability Slot
  "duration"    "15" // Duration (Duration of drowning effect in seconds.) 
  "range"       "600" // Range (Range of drowning effect.)

  "plugin_name"	"ff2r_phatrages"
}
```

#### Explosion
```js
"rage_explosion" // Ability name can use suffixes & prefixes
{
  "slot"        "0" // Ability Slot
  "damage"      "400" // Damage (Amount of damage delivered by fireball explosion) 
  "range"       "400" // Range (Range of fireball explosion.)

  "plugin_name"	"ff2r_phatrages"
}
```

#### Visual Effect

0 - extreme fish eye

1 - central screen crunch

2 - rainbow flashes

3 - fire flashes

4 - blue/green flashes

5 - blue/green web

6 - central fire ball

7 - opaque golden madness

8 - transparent tv static

```js
"rage_visualeffect" // Ability name can use suffixes & prefixes
{
  "effect"      "0" // Visual Effect (0-8 Choice of visual effect, see below.) 
  "duration"    "10" // Duration (Duration of visual effect in seconds.)  
  "range"       "600" // Range (Range of visual effect.)

  "plugin_name"	"ff2r_phatrages"
}
```

* * *