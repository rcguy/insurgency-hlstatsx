# HLStatsX Customized For Insurgency
Complete build of HLStatsX that includes Insurgency specific images, icons, map data, and a heatmap generator. It integrates tightly with the Insurgency Logger and HLStatsX Sourcemod plugins.

---
### HLstatsX CE Ingame Plugin (version 1.6.19)
Provides ingame functionality for interaction from an HLstatsX CE installation

 * [Plugin - hlstatsx.smx](https://github.com/jaredballou/insurgency-sourcemod/blob/master/plugins/hlstatsx.smx?raw=true)
 * [Source - hlstatsx.sp](https://raw.githubusercontent.com/jaredballou/insurgency-sourcemod/master/scripting/hlstatsx.sp)

Adds in-game support for HLStatsX servers to connect and send messages and other tasks. Adds color support, and a number of other features absent from the HLStatsX upstream version. Release ready, no known bugs.

#### CVAR List
 * "hlxce_webpage" "http://www.hlxcommunity.com" //http://www.hlxcommunity.com
 * "hlx_block_commands" "1" //If activated HLstatsX commands are blocked from the chat area
 * "hlx_message_prefix" "" //Define the prefix displayed on every HLstatsX ingame message
 * "hlx_protect_address" "" //Address to be protected for logging/forwarding
 * "hlx_server_tag" "1" //If enabled, adds \HLstatsX:CE\ to server tags on supported games. 1 = Enabled

---
### Insurgency Support Library (version 1.1.0)
Provides functions to support Insurgency and fixes logging

 * [Plugin - insurgency.smx](https://github.com/jaredballou/insurgency-sourcemod/blob/master/plugins/insurgency.smx?raw=true)
 * [Source - insurgency.sp](https://raw.githubusercontent.com/jaredballou/insurgency-sourcemod/master/scripting/insurgency.sp)

Creates hooks and events for Insurgency-specific stat logging, entities, and events. Fixes a lot of issues with missing log entries for HLStatsX, this plugin is tightly bound with my HLStatsX fork I created to handle more Insurgency-specific data and events. This is based off of Brutus' Insurgency logger, but adds support for nearly every event supported by the game, enhances support for new weapons by removing the old config file method of adding weapons, and generally kicks ass if you're looking to create stats from Insurgency. It also includes a number of natives for checking game rules and objective status. This is generally stable, I look at it as a beta release candidate right now.

#### Dependencies
 * [gamedata/insurgency.games.txt](https://raw.githubusercontent.com/jaredballou/insurgency-sourcemod/master/gamedata/insurgency.games.txt)
 * [translations/insurgency.phrases.txt](https://raw.githubusercontent.com/jaredballou/insurgency-sourcemod/master/translations/insurgency.phrases.txt)

#### CVAR List
 * "sm_inslogger_enabled" "1" //sets whether log fixing is enabled
 * "sm_insurgency_checkpoint_capture_player_ratio" "0.5" //Fraction of living players required to capture in Checkpoint
 * "sm_insurgency_checkpoint_counterattack_capture" "0" //Enable counterattack by bots to capture points in Checkpoint
 * "sm_insurgency_infinite_ammo" "0" //Infinite ammo, still uses magazines and needs to reload
 * "sm_insurgency_infinite_magazine" "0" //Infinite magazine, will never need reloading.
 * "sm_insurgency_disable_sliding" "0" //
---

[Insurgency Image Pack](http://stats.jballou.com/hlstatsimg/games/insurgency/images.zip): This is the latest bundle of weapon icons, includes award/ribbon images. Soon it will also include map images.
