# 0ad_build_orders

My 0AD v0.26 (Empires Ascentdent) build orders.

These build orders are specific to one civilization and map.
However, details below the build order help you adapt these
for your situation.

## Greedy standard opening

A greedy standard opening depends on which resources are available.

## Greedy standard opening, berries present

Supply|Time|What
------|----|--------------------------------------------------------------------
10    |0:00|Civic center batch-builds 2 women, route to woodline
10    |0:00|4 women build a farmstead near berries (100 wood, 45 secs) and harvest berries afterwards
10    |0:00|4 citizen solders build a storehouse (100 wood, 40 secs)  near wood and harvest wood afterwards
12    |0:45|Farmstead: research Wicker Baskets (100 wood, 40 secs)
12    |1:00|

## Slinger rush

 * Similar to archer rush.
 * See replay in folder `slinger_rush`
 * Civilization: all slinger/crossbow civilizations:
   Athenians, Britons, Han, Ptolemies
 * Map: Tarim Basin (4 players)
 * Video: [YouTube](https://youtu.be/S2xf2a2Vrc8) [Download (.OGV)](https://richelbilderbeek.nl/0ad_a26_slinger_rush.ogv)
 * Consider using when:
   * Opponent cannot produce ranged units with a short range 
     from its civic center; i.e. only javelineers: 
     Gauls, Iberians, Macedonians, Romans, Seleucids, Spartans
   * There is few hunt close the civic center
 * Avoid using when:
   * Opponent has an archer civilization, as these have better range: 
     Carthagenians, Kushites, Mauryas, Persians
   * There is a lot of hunt close to the civic center

vs |A  |B  |C  |G  |H  |I  |K  |MC |MU |PE |PT |R  |SE |SP 
---|---|---|---|---|---|---|---|---|---|---|---|---|---|---
You|.  |.  |-  |+  |.  |+  |-  |+  |-  |-  |.  |+  |+  |+

> You (a slinger civilization) having worse (`-`), equal (`.`) or
> better (`+`) range than the opponent

Supply|Time|What
------|----|--------------------------------------------------------------------
9     |0:00|Do: Civic center: batch-produce the maximum amount of ranged units [1]
9     |0:05|Do: Move all melee unit towards the opponent [2]
9     |0:10|Do: All ranged units and women: build a farmstead near the berries
9     |0:15|Do: All ranged units building farmstead: shift-move to enemy
9     |0:20|Do: All women building farmstead: shift-harvest berries
9     |   .|Do: Let your fastest unit find the enemy base, direct all units to wait outside of range
9     |0:40|Do: Farmstead: research Wicker Baskets (100 wood, 40 secs)
15    |0:47|The batch of ranged units comes out
15    |0:47|Do: Civic center: queue building 1x woman, direct to wood [3]
15+   |1:20|All solders are near the enemy base
15+   |1:20|Do: all solders are put into the 'Box' formation
15+   |1:25|Do: all solders attack move along the edges of the enemy base [4]
15+   |   .|Do: build up an economy at home

 * [1] The arrival of this group of ranged units is the bottleneck 
   in engaging with the enemy
 * [2] The melee units are slow and need to move quickly.
       The cavalry unit needs to find the opponents' base
 * [3] You will be housed quickly. Start building houses as soon as you can.
 * [4] The attack pattern is simple:
   * General rules:
     * Stay out of range of the opponent's civic center and towers at all costs
     * Draw enemy units towards you. Move further away from the opponent's civic
       center if you have to
     * Prioritize killing units over conquering building: when your soldiers
       have arrived, there is no need for rushing anymore
   * First wave:
     * Use all your soldiers here, i.e. the melee units must soak up some damage
   * After the first wave, 
     * set all ranged units to the 'Standground' behavior
     * set all melee units to the 'Defensive' behavior
     * patrol around the edges of the enemy territory
   * After a full patrol:
     * let all ranged unit patrol behind berry bushes
     * let the melee units either take over a tower (if any), or go home

## Building the project

```
mkdir build
cmake --build .
```

## Civilization abbreviations

Character|Civilization
---------|------------
A |Athenians
B |Britons
C |Carthagenians 
G |Gauls
H |Han
I |Iberians
K |Kushites 
MC|Macedonians
MU|Mauryas 
PE|Persians
PT|Ptolemies
R |Romans
SE|Seleucids
SP|Spartans

## Civilizations' civic center ranged unit

Civ|Civic center ranged unit
---|------------------------
A  |Slingers
B  |Slingers
C  |Archers
G  |Javalineers
H  |Crossbowmen
I  |Javalineers
K  |Archers
MC |Javalineers
MU |Archers
PE |Archers
PT |Slingers
R  |Javalineers
SE |Javalineers
SP |Javalineers

## Terms

Term         |Explaination
-------------|----------------------------------------------------
Shift-move   |Set the next command to be moving towards something
Shift-harvest|Set the next command to be harvesting a resourse
