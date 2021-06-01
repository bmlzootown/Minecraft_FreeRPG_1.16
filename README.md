# FreeRPG

Modified by bmlzootown to add 'support' for mod-based items. Original project can be found [**here**](https://github.com/customjack/Minecraft_FreeRPG_1.16).

## Description:
FreeRPG is a spigot 1.15+ plugin that adds an RPG skill system to minecraft. Inspired by Mcmmo, the goal of FreeRPG is to offer a free Mcmmo alternative. Each skill has a skill tree, with an additional global skill tree. The skill trees can be accessed with a very simplistic, Hypixel inspired GUI accessed using /fRPG.

![freerpg-gif](./images/FreeRPG.gif)

## Getting Started:
To install on any spigot server, simply drag the freerpg-{version}.jar file into the plugins folder.

To get started playing, type "/frpg". This will bring up the Skills GUI seen in the gif above. Clicking on any of the icons will take you to that skill's skill tree. Hovering over any of the icons or clicking on them will tell you more about the perk.

Earning experience is straightforward, mine to get mining experience, cut trees to get woodcutting experience, etc. By the default config, every level you will gain 1 passive token which can be invested in the passive skills represented by the dyes on the left. Every 100 levels, you will gain 1 skill token which can be invested in the skills represented by the terracotta skill tree. Every 1000 levels, you will gain 1 global token that can be used in the global skill tree.

To activate abilities, in most cases you can right click the corresponding tool then break a block. The 10 abilities are as follows:

Big Dig: Activated by right clicking a shovel then breaking a block. Increases dig speed drastically.
Timber: Activated by right clicking an axe then cutting a log. Will cause all logs above to break.
Berserk Pick: Activated by right clicking a pickaxe then breaking a block. Will increase mining speed drastically.
Natural Regeneration: Activated by right clicking a hoe then breaking a crop. Automatically replants all crops at a random growth stage.
Super Bait: Activated by left clicking a fishing rod then fishing. Fish are instantly pulled out of the water, without waiting to get a bite.
Rapid Fire: Activated by left clicking a bow. Arrow shots come out at maximum speed no matter how far the bow is pulled back.
Spur Kick: Activated by right clicking most items while on a horse then left clicking most items. Grants your horse a temporary speed boost.
Swift Strikes: Activated by right clicking a sword then hitting an entity. Your swings no longer have a cooldown.
Stone Solid: Activated by right clicking with an empty hand then hitting an entity. Grants resistance at the cost of being slowed down.
Great Axe: Activated by right clicking an axe then hitting an entity. Your attacks become an AOE strike that deals damage in a certain radius.

#### Player Features:
- Intuitive experience gain
- 3 different token types to be invested in each skill tree
- Tree Feller as an ability
- Fishing system completely reworked, with many new drops
- A grappling hook perk
- New potion recipes, such as Haste and Resistance
- Leaves drop table expanded
- Custom crafting recipes for mob eggs
- Custom crafting recipes for tipped arrows, without requiring dragon's breath
- Ability to check horse stats
- Much more detailed in the information page

#### Admin Features:
- Experience curve control
- Complete experience drop control
- Ability to tweak player token gain
- Ability to modify drop items and rates
- Permissions for earning exp, using abilities, and every command
- Ability to set level caps
- Ability to control custom recipes inputs and outputs
- Ability to control the custom potions effect, duration, ingredient, and color
- More to come soon...

#### Config, Permissions,Languages and Use:
- [config.yml](https://github.com/bmlzootown/Minecraft_FreeRPG_1.16/blob/master/src/main/resources/config.yml)
- [languages.yml](https://github.com/bmlzootown/Minecraft_FreeRPG_1.16/blob/master/src/main/resources/languages.yml)
- [advancedConfig.yml] (https://github.com/bmlzootown/Minecraft_FreeRPG_1.16/blob/master/src/main/resources/advancedConfig.yml)
- [Permissions](https://github.com/bmlzootown/Minecraft_FreeRPG_1.16/blob/master/src/main/resources/plugin.yml)
- [Mod Items](https://github.com/bmlzootown/Minecraft_FreeRPG_1.16/blob/master/src/main/resources/modItems.yml)


#### Commands:
```
GUI COMMANDS:
/frpg or /frpg skills - Opens skills GUI
/frpg globalGUI - manually opens the global skill tree GUI
/frpg skillTreeGUI [skillName] - manually opens a skill tree GUI
/frpg configurationGUI - manually opens the configuration GUI
/frpg skillConfigGUI [skillName] - manually opens the a skill's configuration GUI

EXPERIENCE/LEVELING COMMANDS:
/frpg expGive [playerName] [skillName] [amount] - gives any player experience in any skill
/frpg setLevel [playerName] [skillName] [newLevel] - sets the skill level for any skill of a player
/frpg statReset [playerName] [skillName] - resets a skill for a given player (this will not refund any tokens or experience)
/frpg setSouls [playerName] [amount] - Sets the amount of souls a player has
/frpg setTokens [playerName] [skillName] [skill/passive] [amount] OR
/frpg setTokens [playerName] global [amount] - sets the amount of tokens a player has in a particular stat
/frpg saveStats [playerName] OR /frpg saveStats - saves a singular player or all players' stats to their stat file. Will update the leaderboard
/frpg setMultiplier [playerName] [multiplier] - Sets the player's personal EXP multiplier (this stacks with perks, the server EXP multiplier, and basically every other multiplier).
/frpg addMultiplier [playerName] [decimal] - Changes the player's personal EXP multiplier by some positive or negative decimal (this stacks with perks, the server EXP multiplier, and basically every other multiplier).


TOGGLE COMMANDS:
/frpg flintToggle - manually toggles the "flint finder" perk
/frpg speedToggle - manually toggles the "graceful feet" perk
/frpg potionToggle - manually toggles the "potion master" perk
/frpg flamePickToggle - manually toggles the "flame pick" perk
/frpg grappleToggle - manually toggles the "grappling hook" perk
/frpg hotRodToggle - manually toggles the "hot rod" perk
/frpg veinMinerToggle - manually toggles the "vein miner" perk
/frpg megaDigToggle - manually toggles the "mega dig" perk
/frpg leafBlowerToggle - manually toggles the "leaf blower" perk
/frpg holyAxeToggle- manually toggles the "holy axe" perk

OTHER COMMANDS:
/frpg statLeaders [skillName] [page #] - produces list of highest level players in a particular stat
/frpg enchantItem [level] - tries to enchant an item in your hand with a given enchantment level
/frpg help [page #] - displays all the information above in game
/frpg info - sends the player a message with a link to a google doc that outlines every skill and general mechanics
/frpg resetCooldown [playerName] [skillName] - sets a skill's current cooldown to 0 seconds
/frpg statLookup [playerName] - shows the user all of the searched player's stat levels and server ranks
```


#### Placeholders:
```
%FreeRPG_globalLevel%
%FreeRPG_globalTokens%
%FreeRPG_personalMultiplier%
%FreeRPG_totalSkillTokens%
%FreeRPG_totalPassiveTokens%
%FreeRPG_souls%
%FreeRPG_totalEXP%
%FreeRPG_playTime%
%FreeRPG_globalLevelRank%
%FreeRPG_playTimeRank%

%FreeRPG_<skillName>_Level%
%FreeRPG_<skillName>_EXP%
%FreeRPG_<skillName>_passiveTokens%
%FreeRPG_<skillName>_skillTokens%
%FreeRPG_<skillName>_Multiplier%
%FreeRPG_<skillName>_EXPtoNext%
%FreeRPG_<skillName>_rank%

%FreeRPG_leaderboard_<leaderboardName>_<rank #>_UUID%
%FreeRPG_leaderboard_<leaderboardName>_<rank #>_playerName%
%FreeRPG_leaderboard_<leaderboardName>_<rank #>_sortedStat%
%FreeRPG_leaderboard_<leaderboardName>_<rank #>_stat2%

All the following leaderboard placeholders are more convenient expressions for the placeholders above:
%FreeRPG_leaderboard_<skillName>_<rank #>_exp%
%FreeRPG_leaderboard_<skillName>_<rank #>_level%
%FreeRPG_leaderboard_global_<rank #>_totalLevel%
%FreeRPG_leaderboard_global_<rank #>_totalEXP%
%FreeRPG_leaderboard_playTime_<rank #>_totalTimePlayed%

<leaderboardName> is any of the following:
- Any skillName, must be one word (ex. "beastMastery")
- "PlayTime"
- "global"

Adding "_formatted" to the end of most decimal placeholders will format the string to contain commas. For examples if:
%FreeRPG_leaderboard_mining_2_level% returns 12345 then
%FreeRPG_leaderboard_mining_2_level_formatted% will return 12,345
```

#### Compatibility:
FreeRPG should be compatible with most popular plugins. It has been tested with Essentials, Bssentials, World Edit, Worldguard, Silk Spawners, and PlaceholderAPI and yielded no issues. It has additionally been tested with Multiverse and has no major issues. However, player profiles for different worlds is not possible at the moment. ***Currently seems to be working with Mohist (Forge/Spigot hybrid server).***

#### Language Support:
FreeRPG fully/partially supports the following languages by default:
- English
- Hungarian (Translated by: vERKE)
- French (Translated by: Temuel)
- German (Translated by: KlenerTeufel96 of FruitLab.gg)
- Polish (Translated by: QuarVey)
- Spanish (Translated by: PibeChileno)
- Russian (Translated by:Cr1stalz_, MoKotik, and DevilPlay)
- Portuguese (Translated by: gbuueno)
- Czech (Translated by: Pieck444 and Fractvival)
- Korean (Translated by: Re_Oh)

The default server language can be set in config.yml.
Additionally, each player can pick which language they want the plugin to be represented in.
Server administrators can add their own languages to languages.yml.
If you want to to add your translation to be hardcoded into languages.yml (for anyone to use), please message me on discord or spigotmc.org.

#### Open Source:
FreeRPG is an open source project. Anyone is welcome to view, use, or re-purpose the (poorly, self written) java on the github project page under the standard MIT license.
