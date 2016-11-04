## Greyhawk Wars

1.1

* Release for TripleA engine 1.9.
* With the removal of the Medium AI, a game note warning that scrambling can sometimes crash the Medium AI has been removed. Since this bug doesn't need to be avoided, the "Scramble Rules In Effect" game option is no longer editable.



1.0.7

* The AI will sometimes acquire new territories through diplomacy.
* Each faction now has seven options for gaining control of territories through diplomacy.
* Now the PUs spent on a failed attempt at diplomacy aren't entirely wasted--your chances will improve next round. After you pay another bribe, of course.
* Three new random events have been added, and three new magical treasures.
* A unique, high-powered unit has been added for each faction. These can only be obtained through magic or mercenary territories, and are very rare.



1.0.6

* Added a new random event: plague.
* Suel's dwarves now get correct bonuses in hills and mountains.
* Players can now see whether a faction is immune to blockades by checking whether it has "Smugglers" on the tech panel.
* Placement rules for fortifications and bowmen are now similar to placement rules for heroes: they don't count against the limit on the number of new units you can place in a territory.
* Each nation now has a unique fortification image. The Pomarj and Iron League have slightly improved coats of arms.
* Custom tooltips have been added for units.
* The requirement for Honorable Victory for the Indomitable Center has been lowered to 36.
* A number of territory names have been changed, improving fidelity to source material.



1.0.5

* Giants now fire against dragons before any cavalry charge can kill the giants.
* Bowmen can now retreat rather than being left behind to die while the rest of their army retreats.
* Fortifications are more attractively priced at 8 PUs rather than 10.
* Two new magical treasures have been added, both affecting fortifications, including giving them some movement.
* Since Nyrond's extra hero kept getting killed by Great Kingdom before Nyrond could even use him, Nyrond now receives him at the end of the first round.
* Even at a reduced frequency, the flood event kept having too great an impact on the course of a game. Instead of preventing all combat movement by ground units but allowing full non-combat movement, now it simply reduces movement of ground units by half for the entire round and prevents cavalry from charging.
* The peasant revolt event was overpowered. No longer will it simply skip the faction's placement and production phases. Now, all PUs are lost, and the faction is instead able to place two free conscripts, plus an additional conscript for every four territories it controls.
* The Scarlet Brotherhood's scouts in Hold of the Sea Princes weren't very useful. They've been replaced with conscripts. And just for fun, the conscripts in Hool have been replaced with a troll.
* If a faction manages to get magic treasure in the very first round of play, they now draw from the full range of possible treasures rather than the three it was unintentionally limited to before.
* Players who were transporting their last remaining hero or leader on a boat to a friendly territory were mistakenly designated as vanquished because the triggers fired before non-combat movement. They now fire after non-combat movement, allowing the leader or hero to disembark. They still fire if he remains onboard beyond the non-combat movement phase. Similarly, if you have no heroes and your leader is captured, it used to consider you vanquished. This is no longer the case.
* Now losing a leader feels like the disaster it is. If a leader is captured or slain, that faction suffers a 10 PU penalty in production every round until the leader is rescued or revived. As with many game mechanics, this affects AI players differently since the AI doesn't understand such rules.
* Known issues are made more clear in game notes.
* Technologies can now be changed in edit mode. This only facilitates game testing and does not affect play.



1.0

* User actions now appear in priority order: I am a human, Revive, Diplomacy, then Assassinations.
* For AI players, removed the penalty for ignoring event 14 (see 0.9.7 changelog) and added a chance every round for raiders to be removed since AI almost always ignores them.
* Softened the Stack Tax for AI players, to prevent humans from crippling them by luring the AI into stacking.
* Added a new event 12, neutral dragon raid, and combined the flood and peasant revolt as event 15, alternating every other round. Done to prevent the great negative impact caused when flood or revolt events repeated.
* Damage from dragon raids (strategic bombing) is still limited by the PU value of the territory, but now each individual dragon can cause damage up to the limit, rather than the limit capping total damage.
* Bowmen have been reduced in cost from 5 to 4 PUs.
* Certain magical treasures have increased in power, for instance the Mighty Servant of Leuk-o now adds a defensive strength of 3 to fortifications, and the Spade of Colossal Excavation makes them cheaper.
* Nyrond's national power has been increased so that heroes strengthen 8 instead of 7 units, and the leader 15 instead of 12.
* The types of terrain included in Iron League's national power have been increased. Iron League human infantry now also receive bonuses and can blitz in any terrain. Iron League cavalry also receive bonuses in all terrain and can enter mountains and swamps, but can only blitz hills and forests.
* Altered diplomacy and surprise alliance events to prevent them from immediately destroying enemy leaders or heroes who may be occupying affected territories.
* Since it learned to protect them, AI will now spawn heroes less often.
* Slight rebalancing of territory PUs and starting units.


0.9.9

* Now that the Hard AI is performing so well, the default AI bonus income percentage has been reduced to zero.
* Changed "Placement Restricted By Factory" to false to disable the warning, because excess units are banked, not lost, and because mercenary territories throw off the calculation anyway.
* Added a tips section to the game notes.
* Increased giants' offensiveAttackAA and attackAA values to 2.
* Known issue: if a player leaves all remaining leaders and heroes on transports, they are hidden from the condition that triggers vanquishing and will be changed to vanquished. Added triggers that un-vanquish such a player when they return a hero or leader to a land territory. Also added explanatory notifications.
* Changed several national objectives from directOwnership to alliedOwnership, allowing their fulfillment even if an ally conquers the territories in question.
* Slight rebalancing of territory PUs and starting units.


0.9.8

* Added "isFactory" back to leaders and heroes because the Hard AI didn't recognize them as factories.
* To keep the Hard AI from using them as cannon fodder, gave leaders, heroes, and bowmen "canNotMoveDuringCombatMove". Then created a user action where human players can freely gain a custom tech which activates triggers that change "canNotMoveDuringCombatMove" to false during their turn. Alternatively, a game option can be used for the same purpose. Greyhawk is now playable with Hard AI.
* To prevent the AI from fixating on ungovernable territories, used "unitsNotAllowed" to prevent any units from entering them. This is disabled by the same "I am Human" custom tech.
* With the Hard AI now recognizing them as mobile factories, was able to remove the stacking limit on heroes, and the triggers that flipped their support abilities off during movement.
* Slight rebalancing of starting PUs and units.


0.9.7

* Made various textual changes in notes and notifications.
* Added "other" success and failure notifications for actions.
* For leaders and heroes removed "isFactory" and added "canProduceUnits" and "canBeDamaged" so that they can still produce and be bombed, but don't have the placement limits/behavior of factories (they are still isInfrastructure). (This was reversed in the next version.)
* Changed "Scramble To Any Amphibious Assault" to false, since "Scramble To Sea Only" is true, and since dragons themselves are the only air bases and can already have air battles.
* Fixed the problem of leaders sometimes getting movement 6 (it was related to the reset after flood events).
* Fixed a trigger (Magic_18b) that was allowing Iuz to receive two magic items in a single round.
* Changed the sequence, moving Purchase from before CombatMove to before Place. Consequently shifted the timing of all events to after Politics, all magic to before Purchase, and ungovernables to after Politics. This prevents a number of AI problems, including one that frequently caused Hard AI to crash. (Triggers changing territory ownership, spawning units, or removing units were the problem. The AI would make a plan and then the units it planned to do something with had disappeared.)
* Updated event 9 (rebellions) to only fire if the faction owns all the involved territories, so that other factions can't lose territories through this event.
* Changed event 9 for Pomarj to affect Welkwood and Gnarley Forest rather than Welkwood South, since for all other factions it only affects conquered, not original territories. Also removed Reyhu from Furyondy's event 9.
* Using a negative national objective, created a -10 PU penalty for ignoring event 14 (neutral raid within your original territories). Previously it wasn't worth the trouble of quashing the rebellion.
* Introduced a "stack tax" using negative national objectives. Suffer a -5 PU penalty for every territory in which you amass more than 15 non-infrastructure units. Penalties increase with stack size.
* Added a movement and placement (but not attacking) limit of 60 non-infrastructure units per territory. Stacks cannot exceed this.
* (perhaps temporarily) Added a movement and attacking limit for all heroes. A faction cannot have more than 1 hero per territory. Attempting to keep AI from bunching them up and then not being able to place its new units. (This was reversed in the next version.)
* (perhaps temporarily) Added triggers that remove the support function of leaders and heroes during movement phases, but not during purchase or battle. Attempt to keep Hard AI from thinking of them only as cannon fodder. Mixed success. (This was reversed in the next version.)
* Scrambling can be disabled as a game option, preventing Medium AI errors.


0.9.6 

* Everything has changed.