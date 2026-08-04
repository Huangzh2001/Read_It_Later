---
url: https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics
tags:
  - video
status: readed
date: 2026-08-04T11:09:03+08:00
---
![Advanced entity position mechanics - Dwarf Fortress Wiki](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics)
  

**v50 Steam/Premium information for editors**

- v50 information can now be added to pages in the **main namespace**. v0.47 information can still be found in the **DF2014** namespace. [See here](https://dwarffortresswiki.org/index.php/Dwarf_Fortress_Wiki:V "Dwarf Fortress Wiki:V") for more details on the new versioning policy.
- [Use this page](https://dwarffortresswiki.org/index.php/Dwarf_Fortress_Wiki_talk:Versions#v50_migration "Dwarf Fortress Wiki talk:Versions") to report any issues related to the migration.

This notice may be cached—the current version can be found [here](https://dwarffortresswiki.org/index.php/MediaWiki:Sitenotice).

# Advanced entity position mechanics

[Jump to navigation](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#mw-head)[Jump to search](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#searchInput)

[xTATTEREDx](https://dwarffortresswiki.org/index.php/Dwarf_Fortress_Wiki:Quality#Tattered "Dwarf Fortress Wiki:Quality")  · [+FINE+](https://dwarffortresswiki.org/index.php/Dwarf_Fortress_Wiki:Quality#Fine "Dwarf Fortress Wiki:Quality")  · [*SUPERIOR*](https://dwarffortresswiki.org/index.php/Dwarf_Fortress_Wiki:Quality#Superior "Dwarf Fortress Wiki:Quality")  · [≡EXCEPTIONAL≡](https://dwarffortresswiki.org/index.php/Dwarf_Fortress_Wiki:Quality#Exceptional "Dwarf Fortress Wiki:Quality")  · [☼MASTERWORK☼](https://dwarffortresswiki.org/index.php/Dwarf_Fortress_Wiki:Quality#Masterwork "Dwarf Fortress Wiki:Quality")

|[Modding](https://dwarffortresswiki.org/index.php/Modding "Modding")<br><br>---|
|---|
|[Tokens](https://dwarffortresswiki.org/index.php/Token "Token")|
|[Audio](https://dwarffortresswiki.org/index.php/Audio "Audio")[Biome](https://dwarffortresswiki.org/index.php/Biome_token "Biome token")[Graphics](https://dwarffortresswiki.org/index.php/Graphics_token "Graphics token")[Tile page](https://dwarffortresswiki.org/index.php/Graphics#Tile_Page "Graphics")[Interaction](https://dwarffortresswiki.org/index.php/Interaction_token "Interaction token")[Mod info](https://dwarffortresswiki.org/index.php/Mod_info_token "Mod info token")[Plant](https://dwarffortresswiki.org/index.php/Plant_token "Plant token")[Speech](https://dwarffortresswiki.org/index.php/Speech_file "Speech file")[Sphere](https://dwarffortresswiki.org/index.php/Sphere#Sphere_tokens "Sphere")[Syndrome](https://dwarffortresswiki.org/index.php/Syndrome#The_anatomy_of_a_syndrome "Syndrome")[World](https://dwarffortresswiki.org/index.php/World_token "World token")|
|Body tokens|
|[Body](https://dwarffortresswiki.org/index.php/Body_token "Body token")[Body detail plan](https://dwarffortresswiki.org/index.php/Body_detail_plan_token "Body detail plan token")[Bodygloss](https://dwarffortresswiki.org/index.php/Bodygloss "Bodygloss")[Tissue](https://dwarffortresswiki.org/index.php/Tissue_definition_token "Tissue definition token")|
|Creature tokens|
|[Creature](https://dwarffortresswiki.org/index.php/Creature_token "Creature token")[Creature mannerism](https://dwarffortresswiki.org/index.php/Creature_mannerism_token "Creature mannerism token")[Personality facet](https://dwarffortresswiki.org/index.php/Personality_facet "Personality facet")[Creature variation](https://dwarffortresswiki.org/index.php/Creature_variation_token "Creature variation token")[Procedural graphics layer](https://dwarffortresswiki.org/index.php/Procedural_graphics_layer "Procedural graphics layer")|
|Descriptor tokens|
|[Descriptor color](https://dwarffortresswiki.org/index.php/Descriptor_color_token "Descriptor color token")[Color](https://dwarffortresswiki.org/index.php/Color "Color")[Descriptor pattern](https://dwarffortresswiki.org/index.php/Descriptor_pattern_token "Descriptor pattern token")[Descriptor shape](https://dwarffortresswiki.org/index.php/Descriptor_shape_token "Descriptor shape token")|
|Entity tokens|
|[Entity](https://dwarffortresswiki.org/index.php/Entity_token "Entity token")[Ethic](https://dwarffortresswiki.org/index.php/Ethic "Ethic")[Language](https://dwarffortresswiki.org/index.php/Language_token "Language token")[Value](https://dwarffortresswiki.org/index.php/Personality_value "Personality value")[Position](https://dwarffortresswiki.org/index.php/Position_token "Position token") ([Variable positions](https://dwarffortresswiki.org/index.php/Variable_positions "Variable positions"))|
|Job tokens|
|[Building](https://dwarffortresswiki.org/index.php/Building_token "Building token")[Labor](https://dwarffortresswiki.org/index.php/Labor_token "Labor token")[Reaction](https://dwarffortresswiki.org/index.php/Reaction "Reaction")[Skill](https://dwarffortresswiki.org/index.php/Skill_token "Skill token")[Unit type](https://dwarffortresswiki.org/index.php/Unit_type_token "Unit type token")|
|Item tokens|
|[Item type](https://dwarffortresswiki.org/index.php/Item_token "Item token")[Item definition](https://dwarffortresswiki.org/index.php/Item_definition_token "Item definition token")[Ammo](https://dwarffortresswiki.org/index.php/Ammo_token "Ammo token")[Armor](https://dwarffortresswiki.org/index.php/Armor_token "Armor token")[Instrument](https://dwarffortresswiki.org/index.php/Instrument_token "Instrument token")[Tool](https://dwarffortresswiki.org/index.php/Tool_token "Tool token")[Trap component](https://dwarffortresswiki.org/index.php/Trap_component_token "Trap component token")[Weapon](https://dwarffortresswiki.org/index.php/Weapon_token "Weapon token")|
|Material tokens|
|[Material type](https://dwarffortresswiki.org/index.php/Material_token "Material token")[Material definition](https://dwarffortresswiki.org/index.php/Material_definition_token "Material definition token")[Inorganic material definition](https://dwarffortresswiki.org/index.php/Inorganic_material_definition_token "Inorganic material definition token")|
|---<br><br>Lua|
|[Scripting](https://dwarffortresswiki.org/index.php/Lua_scripting "Lua scripting")[Examples](https://dwarffortresswiki.org/index.php/Lua_script_examples "Lua script examples")[Functions](https://dwarffortresswiki.org/index.php/Lua_functions "Lua functions")|
|[v](https://dwarffortresswiki.org/index.php/Template:V50_modding "Template:V50 modding") · [t](https://dwarffortresswiki.org/index.php?title=Template_talk:V50_modding&action=edit&redlink=1 "Template talk:V50 modding (page does not exist)") · [e](https://dwarffortresswiki.org/index.php?title=Template:V50_modding&action=edit)|

  

## Contents

- [1Introduction](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Introduction)
    - [1.1What is an entity? What is a position?](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#What_is_an_entity.3F_What_is_a_position.3F)
- [2Position levels (Site/Civ) and their interaction](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Position_levels_.28Site.2FCiv.29_and_their_interaction)
    - [2.1Table of interaction between different position levels](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Table_of_interaction_between_different_position_levels)
    - [2.2Other interactions](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Other_interactions)
- [3General](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#General)
    - [3.1Civ-level nobles living at your site](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Civ-level_nobles_living_at_your_site)
    - [3.2Fortress mode, world-gen and their differences](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Fortress_mode.2C_world-gen_and_their_differences)
    - [3.3Units holding multiple positions in multiple entities](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Units_holding_multiple_positions_in_multiple_entities)
- [4Specific Tags and functions](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Specific_Tags_and_functions)
    - [4.1[PRECEDENCE]](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#.5BPRECEDENCE.5D)
    - [4.2[RESPONSIBILITY]ies](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#.5BRESPONSIBILITY.5Dies)
        - [4.2.1World-gen effects of the [RESPONSIBILITY] of available positions](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#World-gen_effects_of_the_.5BRESPONSIBILITY.5D_of_available_positions)
        - [4.2.2[DELIVERS_MESSAGES]](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#.5BDELIVERS_MESSAGES.5D)
        - [4.2.3Outpost Liaisons and Diplomats](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Outpost_Liaisons_and_Diplomats)
        - [4.2.4[TRADE]](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#.5BTRADE.5D)
    - [4.3[NUMBER]](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#.5BNUMBER.5D)
        - [4.3.1Automatic spreading of assumed, non-singular positions](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Automatic_spreading_of_assumed.2C_non-singular_positions)
        - [4.3.2[AS_NEEDED]](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#.5BAS_NEEDED.5D)
    - [4.4[REPLACED_BY], [REQUIRES_POPULATION], [REQUIRES_MARKET]](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#.5BREPLACED_BY.5D.2C_.5BREQUIRES_POPULATION.5D.2C_.5BREQUIRES_MARKET.5D)
        - [4.4.1Effect of replacement (and on [LAND_HOLDER]s)](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Effect_of_replacement_.28and_on_.5BLAND_HOLDER.5Ds.29)
        - [4.4.2What doesn't work](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#What_doesn.27t_work)
    - [4.5[CONQUERED_SITE]](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#.5BCONQUERED_SITE.5D)
- [5Availability and visibility](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Availability_and_visibility)
    - [5.1Availability of (new) positions](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Availability_of_.28new.29_positions)
    - [5.2Visibility of positions](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Visibility_of_positions)
- [6 Evaluation of Positions](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#_Evaluation_of_Positions)
- [7Gaining a position](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Gaining_a_position)
    - [7.1Who can take a position](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Who_can_take_a_position)
    - [7.2Appointment](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Appointment)
        - [7.2.1Automatic appointment in world-gen and on the civ level](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Automatic_appointment_in_world-gen_and_on_the_civ_level)
        - [7.2.2Manual appointments by players in fortress mode](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Manual_appointments_by_players_in_fortress_mode)
    - [7.3Election](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Election)
        - [7.3.1 Election Day](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#_Election_Day)
        - [7.3.2Election Eligiblity](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Election_Eligiblity)
        - [7.3.3Skills](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Skills)
    - [7.4Assumption](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Assumption)
    - [7.5Succession](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Succession)
        - [7.5.1Eligibility for succession](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Eligibility_for_succession)
        - [7.5.2Site and civ combined succession](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Site_and_civ_combined_succession)
        - [7.5.3Succession [BY_HEIR]](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Succession_.5BBY_HEIR.5D)
        - [7.5.4Premature Succession](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Premature_Succession)
            - [7.5.4.1Multiple succession chains](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Multiple_succession_chains)
            - [7.5.4.2Working triggers](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Working_triggers)
            - [7.5.4.3Non-working (triggers)](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Non-working_.28triggers.29)
- [8Losing a position](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Losing_a_position)
- [9Embarkment](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Embarkment)
- [10Land Holders](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Land_Holders)
    - [10.1Functioning of the regular landholder chain](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Functioning_of_the_regular_landholder_chain)
    - [10.2Appointment](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Appointment_2)
    - [10.3Succession](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Succession_2)
        - [10.3.1Impossibilities for succession by a site-position](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Impossibilities_for_succession_by_a_site-position)
    - [10.4Nomination](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Nomination)
    - [10.5Levels](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Levels)
    - [10.6Moving landholders](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Moving_landholders)
    - [10.7Replacement by a generic civ-position](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Replacement_by_a_generic_civ-position)
    - [10.8Landholder with fixed number](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Landholder_with_fixed_number)
    - [10.9Responsibilities](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Responsibilities)
- [11Military](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Military)
    - [11.1Squad management](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Squad_management)
    - [11.2Squad assignment](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Squad_assignment)
    - [11.30-squads](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#0-squads)
- [12Further testing](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Further_testing)
- [13Oddities (Bugs)](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Oddities_.28Bugs.29)
- [14Examples](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Examples)
    - [14.1The Founder](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#The_Founder)
    - [14.2Marriage bar](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Marriage_bar)
    - [14.3The Archduke](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#The_Archduke)

# Introduction

[Discussion thread on the forum](http://www.bay12forums.com/smf/index.php?topic=182239.0)

This page documents observed and tested behavior of entity positions in Dwarf Fortress that is not fully described elsewhere on the wiki. It focuses on advanced interactions between position tokens, including appointment, succession, election, and responsibility handling, across both civilization-level and site-level entities.

The mechanics described here are based on empirical testing in world generation and fortress mode, supplemented where necessary by raw analysis. In several cases, the game’s behavior is determined by evaluation order and interaction between multiple tags, rather than by individual tokens in isolation.

This page is intended for modders and advanced players who are designing or debugging custom entity position structures. It does not restate basic position mechanics, but instead highlights edge cases, non-obvious interactions, and behaviors that may appear inconsistent or undocumented.

Unless stated otherwise, the described behavior applies to current versions of the game and may differ from older releases.

## What is an entity? What is a position?

An [entity](https://dwarffortresswiki.org/index.php/Entity "Entity") is an organizational structure that can have relationships with other entities, usually known as a [civilization](https://dwarffortresswiki.org/index.php/Civilization "Civilization") or a "[site](https://dwarffortresswiki.org/index.php/Site "Site") government" in the game, but ie. merchant [companies](https://dwarffortresswiki.org/index.php/Company "Company"), [mercenary orders](https://dwarffortresswiki.org/index.php/Mercenary#Mercenary_Orders "Mercenary"), [guilds](https://dwarffortresswiki.org/index.php/Guild "Guild"), [religious organizations](https://dwarffortresswiki.org/index.php/Religion "Religion"), bandits and necromancer towers are also entities (and necromancer towers use the same entity type as "site governments"). An entity can have positions - in most cases, these are hardcoded and generated by the game, but as for civilizations and sites, the [raw files](https://dwarffortresswiki.org/index.php/Raw_file "Raw file") can be customised.

A position is a special relationship between a unit and an entity. The unit holding a position has a larger influence over that entity than other citizens. Positions are mostly known as [nobles](https://dwarffortresswiki.org/index.php/Nobles "Nobles"), but in this article. the technical term is used.

# Position levels (Site/Civ) and their interaction

There are two basic types of positions that are customizable: **civ(ilization)** level and **site level**. Positions with the tag [SITE] are at site level, positions without the tag [SITE] are at 'civ level'. These two types of nobles can be considered **loosely related systems**. There are a few places where they can interact with each other.

Civ-level positions are in charge of the civilization as a whole, managing national [trade](https://dwarffortresswiki.org/index.php/Trade "Trade"), laws, and [wars](https://dwarffortresswiki.org/index.php/War "War"). These are, for example, the vanilla [monarch](https://dwarffortresswiki.org/index.php/Monarch "Monarch"), [diplomat](https://dwarffortresswiki.org/index.php/Diplomat "Diplomat") and [general](https://dwarffortresswiki.org/index.php/General "General"). (Note that the general doesn't really do anything, except creation of additional pets in world-gen for the general and possibly raising the animal training knowledge of the civilization to "general familiarity".)

**[LAND_HOLDER]** nobles are also positions at civ-level. These units are members of the national government, but have gained authority over some land or site. Once they do, they move to that place, but their position is still regarded as a civ-level position.

Site-level position holders are members of a site government (subsidiary to the civilization), and manage local affairs in that location. These are, for example, the [mayor](https://dwarffortresswiki.org/index.php/Mayor "Mayor"), the [sheriff](https://dwarffortresswiki.org/index.php/Sheriff "Sheriff") and the [broker](https://dwarffortresswiki.org/index.php/Broker "Broker").

## Table of interaction between different position levels

In this table, the possible interactions between different position levels are summarized. The header row shows the positions defining the tokens.

The left column shows the position type that is referred to. Example:

|referred position-type|LAND_HOLDER|
|---|---|
|civilization|(baron is) APPOINTED_BY:MONARCH|

color coding:  

- Exists in vanilla  
    
- Possible with mods  
    
- Not possible  
    
- possible to some extent.  
    
- not yet fully investigated.  
    

|referred position-type|Civilization|SITE|LAND_HOLDER|CONQUERED_SITE|
|---|---|---|---|---|
|Civilization|APPOINTED_BY  <br>COMMANDER  <br>REPLACED_BY  <br>SUCCESSION|APPOINTED_BY  <br>COMMANDER  <br>REPLACED_BY  <br>SUCCESSION **(1)**|APPOINTED_BY  <br>COMMANDER  <br>REPLACED_BY  <br>SUCCESSION|APPOINTED_BY  <br>COMMANDER  <br>REPLACED_BY  <br>SUCCESSION|
|SITE|APPOINTED_BY  <br>COMMANDER  <br>REPLACED_BY  <br>SUCCESSION **(2)**|APPOINTED_BY  <br>COMMANDER  <br>REPLACED_BY  <br>SUCCESSION|APPOINTED_BY **(3)**  <br>COMMANDER  <br>REPLACED_BY  <br>SUCCESSION **(4)**|APPOINTED_BY  <br>COMMANDER  <br>REPLACED_BY  <br>SUCCESSION|
|LAND_HOLDER|APPOINTED_BY  <br>COMMANDER  <br>REPLACED_BY **(6)**  <br>SUCCESSION|APPOINTED_BY  <br>COMMANDER  <br>REPLACED_BY  <br>SUCCESSION **(5)**|APPOINTED_BY  <br>COMMANDER  <br>REPLACED_BY **(7)**  <br>SUCCESSION **(8)**|APPOINTED_BY  <br>COMMANDER  <br>REPLACED_BY  <br>SUCCESSION|
|CONQUERED_SITE|APPOINTED_BY  <br>COMMANDER  <br>REPLACED_BY  <br>SUCCESSION|APPOINTED_BY  <br>COMMANDER  <br>REPLACED_BY  <br>SUCCESSION|APPOINTED_BY  <br>COMMANDER  <br>REPLACED_BY  <br>SUCCESSION|APPOINTED_BY  <br>COMMANDER  <br>REPLACED_BY  <br>SUCCESSION|

Remarks:

1. Works only in world-gen, if a unit with that civ-position is present at the site.
2. Works only in world-gen, the site-position holding unit will then move to the capital.
3. Is completely ignored
4. Works only in world-gen.
5. Works only in world-gen.
6. Won't appear at all
7. This is necessary for the landholder chain to work properly, it doesn’t work otherwise.
8. This works only outside of the landholder chain, so when landholders are simply regarded as civ-level nobles. might also work in world-gen

## Other interactions

Unfortunately, interactions with positions of other entities don't seem possible, such as APPOINTED_BY: HIGH_PRIEST. With [VARIABLE_POSITIONS], positions are automatically created with codes like CUSTOM_LAW_MAKER_2, but interaction with these positions don't seem to work, either. For more info on those, see [Variable positions](https://dwarffortresswiki.org/index.php/Variable_positions "Variable positions")

# General

## Civ-level nobles living at your site

Nobles from your civilization can come to live at your fortress. This happens in vanilla with landholders such as [Baron](https://dwarffortresswiki.org/index.php/Baron "Baron"), [Count](https://dwarffortresswiki.org/index.php/Count "Count") and [Duke](https://dwarffortresswiki.org/index.php/Duke "Duke"), with the Monarch, but sometimes also with non-landed LAND_HOLDERS.

When a civ-level noble becomes a [citizen](https://dwarffortresswiki.org/index.php/Citizen "Citizen") at your location, their position is shown among the site-level positions in your [nobles screen](https://dwarffortresswiki.org/index.php/Nobles_screen "Nobles screen"). They appear to function as a site-level noble. They may have [demands](https://dwarffortresswiki.org/index.php/Demand "Demand"), [mandates](https://dwarffortresswiki.org/index.php/Mandate "Mandate"), [squads](https://dwarffortresswiki.org/index.php/Squad "Squad") and the like. They can appoint nobles at the site-level.

Even if they have certain site related [RESPONSIBILITY]ies, they will not do the tasks that go with them.

## Fortress mode, world-gen and their differences

Their are a few differences in how positions function between fortress mode (normal play mode) and the world generation (world-gen).

In **fortress mode**, the player has some control over the appointment of nobles, limited by elections, automatic filled-in positions and succession rules. Pre-fortress mode, which is referred to as **world-gen**, the game will always attempt to assign nobles whenever possible. It is subjected to the same rules as in fortress-mode, but there are some exceptions. In **[World activities](https://dwarffortresswiki.org/index.php/World_activities "World activities")**, which is the thing that happens in the world while you play fortress mode, it seems as if the same rules are applied as fortress mode.

A difference between player-fortress-mode and world-gen, is causes by visibility (see below). Positions that are not visible by the player and thus not available for assignment, will be available in world-gen and will thus be automatically assigned.

In fortress mode, a position that is both [ELECTED] and [APPOINTED_BY], cannot be appointed by the player and is also not elected, and can thus not be filled. But in world-gen sites however, these positions are automatically filled.

Positions with [AS_NEEDED] are almost never created and filled in world-gen (depending on their [RESPONSIBILITY]ies), but can always be used in player mode.

A position can, in fortress mode, be filled by the same unit. A unit can gain multiple positions in fortress mode, for example because of [elections](https://dwarffortresswiki.org/index.php/Elections "Elections"). This will not happen in world-gen mode: a unit can only have one position. See also remarks on 'embark' and 'Losing a position'.

In world-gen, [SUCCESSION] between civ-levels and [SITE-]levels may happen. This will not happen in fortress mode, or even off-site in [World activities](https://dwarffortresswiki.org/index.php/World_activities "World activities").

In fortress mode, premature SUCCESSION may happen. This will not happen in world-gen mode.

## Units holding multiple positions in multiple entities

A unit can hold multiple positions in its civilisation or in its site-entity, however in world-gen a unit will not hold multiple positions in one site-entity or in one civilisation (note that in world-gen a unit can hold multiple variable positions of the same entity, if the entity is ie. an outcast group). It is however possible - in world-gen - for a unit to hold multiple positions as long as the positions belong to different civilizations / site-entities (ie. it is possible for a militia commander of a site-entity to later on also become a monarch of the parent civilization, while staying a militia commander), if a unit holds a position of two different site-entities (the unit will usually have left one of the groups, without relinquishing the position). Only at player-managed sites can units be holding multiple positions (of the site-entity) at once. It is currently unknown, whether it is possible in world-gen for a unit to have a civ-level position in two different civilisations (but it probably is possible, as a a unit can belong to multiple civilizations and a unit usually does not relinquish a position, when the unit gets another position, as long as the entities of both positions are not the same).

In world-gen, if there are too many positions to be filled, they simply stay empty until more units are available. E.G, a unit at a site might inherit a civ-level position and still remain a member of the local government. When this happens however, they move to the capital. If a unit gains a new position, either inherited or otherwise, it drops the previous one (of that civilisation or site-entity) - the unit will not drop any positions unrelated to the entity of the new position (ie. a CUSTOM_OUTCAST_FACTOR will not relinquish that position, if the unit becomes the ruler of a civilization and a militia commander will also not necessarily relinquish the position, if the unit becomes also the monarch of the corresponding civilization). If a unit assumes a civ-position in fortress mode, it leaves the current position.

If a unit holds the same site-position multiple times, it has no additional effect.

If a unit holds multiple different positions of the same entity, it has all those positions' responsibilities and properties, stacked up. Presumably, the demands for those combined positions are determined by the highest.

A unit holding a position with a succession token can be assigned another position with a (different) succession token.

A unit holding a position with a squad-position cannot hold another squad-position. It is dropped from the first of those, when the second position is assigned. A unit holding a position with a succession token cannot be assigned to a squad-position - the unit is simply not available. It works the other way around, though.

# Specific Tags and functions

## [PRECEDENCE]

The first defined position with precedence of 1 counts as the ruler of the civ. See also: [PRECEDENCE](https://dwarffortresswiki.org/index.php/Position_token#PRECEDENCE "Position token").

If the precedence is omitted or has a negative value, the game sets 0 as precedence, which seems to have no effect whatsoever. When a unit has multiple positions, the name of the position with the highest rank in precedence is shown behind the unit's name.

If you omit precedence entirely, or set it to [PRECEDENCE:NONE], the position name will not be shown after the unit’s name. Your *Urist Mason* will remain simply *Mason*. This can be useful for positions that are unimportant or purely functional. The position will also not appear in the civilisation overview of your site on the world map. The position name is shown in messages, but remains hidden on the nobles screen as well. To make it visible there, use [LAND_NAME].

## [RESPONSIBILITY]ies

Both civ and [SITE] positions can carry responsibilities. However, not all responsibilities are active for both types: some function only for civ positions, others only for site positions. When a civ noble arrives at a site and takes up residence, they do not perform responsibilities that are intended for SITE nobles. As a result, these responsibilities neither trigger their associated tasks nor unlock related game mechanics. For example, a civ-level manager living in a fortress will not perform management duties there and doesn't unlock the management-screen, even with an assigned office. This behavior applies to the following [SITE]-level responsibilities:

- [RESPONSIBILITY:ACCOUNTING]
- [RESPONSIBILITY:BUILD_MORALE]
- [RESPONSIBILITY:HEALTH_MANAGEMENT]
- [RESPONSIBILITY:LAW_ENFORCEMENT]
- [RESPONSIBILITY:MANAGE_PRODUCTION]
- [RESPONSIBILITY:MEET_WORKERS]
- [RESPONSIBILITY:TRADE] (functions differently)

Other responsibilities may be affected as well, but have not yet been fully tested.

### World-gen effects of the [RESPONSIBILITY] of available positions

It is possible to cause civs and individual sites to change their behavior substantially when they reach a certain size, by controlling nobles.

- If a site can only appoint a position with [MILITARY_GOALS] after reaching a particular size, that site will not send armies on missions until the required size is reached.
- A civ-level [LAW_MAKING] position is required for the civilization to have any kind of cohesion. Without it, sites will be constantly embroiled in territorial disputes and civil wars will be commonplace.
- [MILITARY_STRATEGY] positions go out and tame wild animals. This makes your civ gain those animals as domesticated and also brings them in sieges.
- The [Personality](https://dwarffortresswiki.org/index.php/Personality_facet "Personality facet") of the position's holder determines how they lead the civ.

### [DELIVERS_MESSAGES]

The only [AS_NEEDED]-position that is created in worldgen based on responsibility is that of the site-level responsibility [DELIVERS_MESSAGES].

### Outpost Liaisons and Diplomats

Civ-positions with the responsibility [ESTABLISH_COLONY_TRADE_AGREEMENTS] ([Outpost Liaisons](https://dwarffortresswiki.org/index.php/Outpost_Liaison "Outpost Liaison")) will meet with the site-noble who has responsibility for [RECEIVE_DIPLOMATS] and the highest rank of precedence (i.e. the lowest precedence value). Usually this is the [Expedition leader](https://dwarffortresswiki.org/index.php/Expedition_leader "Expedition leader").

Once a [LAND_HOLDER] is assigned to the site, civ-positions with the responsibility [MAKE_TOPIC_AGREEMENTS] ([Diplomats](https://dwarffortresswiki.org/index.php/Diplomat "Diplomat")) will meet with **civ**-level nobles present at the site who have the [RECEIVE_DIPLOMATS] responsibility. If multiple eligible nobles are available, one is selected at random. If no eligible noble is present, the diplomat leaves angrily. If the landholder is no longer present at the site, diplomats will not arrive at all.

It appears that Outpost Liaisons and Diplomats are chosen for a diplomatic mission based on availability. When multiple candidates exist, the position defined last in the raws is most often selected.

### [TRADE]

Civ-level nobles with [TRADE] will arrive with the caravan, just as the Outpost Liaison. Their behavior is no longer active in the vanilla game, but the mechanics are still present. See [Guild representative](https://dwarffortresswiki.org/index.php/40d:Guild_representative "40d:Guild representative") for more details. This civ-noble will only meet with the SITE noble with [TRADE], usually the [Broker](https://dwarffortresswiki.org/index.php/Broker "Broker").

If two civ-nobles exist with both [TRADE] and [ESTABLISH_COLONY_TRADE_AGREEMENTS], they both arrive at the same time. Even if both tokens are assigned to a single position, if more than one instance of that position exists, two of them will arrive. However in that case, somehow the elevation of the site and appointment of landholder isn't offered.

If the SITE-noble they intend to meet has both [TRADE] and [RECEIVE_DIPLOMATS], only one meeting will proceed and the other is cancelled. However, when two SITE-nobles are available, each with either [TRADE] or [RECEIVE_DIPLOMATS], both meetings will proceed and both civ-nobles will attempt to negotiate a trade agreement. It is not known what happens if these agreements are accepted or refused.

In the trade depot, the last defined position with the [TRADE] responsibility is shown as broker. However when requesting a trader, the first defined position with [TRADE] will actually go there to do the trade.

## [NUMBER]

A position might be defined with a number. In that case, as many as defined can be available. If the positions become available, in world-gen and when embarking, they are all filled-in completely.

If the ruling position (with PRECEDENCE of 1) has a NUMBER higher than 1, a random unit of the ones holding these positions is shown as ruler in the embark screen.

A [NUMBER] of 0 (zero) has the same effect as 1.

### Automatic spreading of assumed, non-singular positions

If there are civ positions that have a NUMBER higher then '1' and which are assumed (not APPOINTED_BY or ELECTED) but are **not DUTY_BOUND**, these are automatically spread among the civilisation, based on population. If there are a number of **20** available slots of that position, they spread among a civilization with a combined population of, for example, 1000 of which your fortress has 100 (10%), **2** of your fortress' citizens will assume that position. This may probably also work with elected and appointed positions, but that may be depending on the death of the current holders and this needs more testing. Assumption works within a day, anyway.

### [AS_NEEDED]

These positions can be created automatically by the game in world-gen. This, however, only works with:

- [LAND_HOLDER]'s
- squad commanders (needs more testing)
- Messengers at sites

For all other types of positions, they're not created in world-gen, even if they are defined with RESPONSIBILITY's. For example, even in war, the game wouldn't create a MILITARY_GOALS position, if they have AS_NEEDED as number.

However, in fortress mode / player mode, these positions can be created by the player at will.

Positions with AS_NEEDED need to be created first, before any symbols are assignable as 'symbols' (objects) for the position holder to carry or wear.

Positions with AS_NEEDED cannot be created and then ELECTED in fortress mode. It only works with APPOINTED_BY.

## [REPLACED_BY], [REQUIRES_POPULATION], [REQUIRES_MARKET]

The token [REPLACED_BY:position] means that once the replacing position meets its requirements for activation, the 'to-be-replaced' position will disappear. This is defined in [REQUIRES_POPULATION] or [REQUIRES_MARKET]. The tags are closely related to each other and seem to only have a meaningful function if combined. Nobles with [REQUIRES_POPULATION] require the population to have a specific size. Nobles with [REQUIRES_MARKET] are only activated in market sites, such as fortresses or towns. [REQUIRES_POPULATION] and [REQUIRES_MARKET] can be combined, activating that position once both requirements are met.

The [REQUIRES_MARKET] can be used to differentiate positions between hamlets and hillocks, and larger sites. IThe market always is build the year after the site is founded. So a position that is to be replaced, will be gone immediately.

The [REQUIRES_POPULATION]-tag works on the civ-level as well as on site-level, but those systems are in this mechanic strictly separated. Site-level positions cannot be replaced by civ-level positions and visa versa. This makes sense, because they both depend on their own population-count. When using REQUIRES_POPULATION on civ-level, it counts the total population of the civilisation.

See also: [Evaluation of positions](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Evaluation_of_Positions "Advanced entity position mechanics")

### Effect of replacement (and on [LAND_HOLDER]s)

Replacement is immediate and complete - the current holding unit loses the position, even before SUCCESSION_BY_POSITION rules are applied. A position with a number of 1 will replace all the slots of a position with a higher number of slots.

Even if the next position is available but not visible, replacement still takes place. If a position is replaced, it is completely gone - it cannot be appointed, succeeded, elected or assumed any longer. The unit immediately loses its position.

In legends, replacement is mentioned as: "(unit name) ceased to be (position name)" The replacement of an AS_NEEDED position empties the position's slot forever. In fortress mode, it may seem as if you can create new slots and appoint new units in the nobles screen, but this is reversed as soon as you close the window.

The landholder chain uses [REPLACED_BY] differently. It does not clear the position completely, but uses it for succession to the next level's position. [REPLACE_BY] is required to let that system work properly. This also means that the way in which landholders succeed (replace + as_needed) does not work in any other way.

Replacement between LAND_HOLDERS and other site- or civ positions does not work in any way. Only the vanilla replacement sequence between levels of LAND_HOLDERs does work. If the token is omitted for landholders, the landholder chain is broken, so replacement is required for the landholder system to work.

[REQUIRES_POPULATION] also does not work for [LAND_HOLDER], when you set [NUMBER] to 1. The position is not created when the required population is reached.

### What doesn't work

**Attention: If a position cannot be appointed, for example because of 'mutual appointment', it still exists according to replacement mechanics and will replace other positions if so defined. If a certain position(a) will be replaced by the baron's assistant, which can only be appointed by the [LAND_HOLDER] baron, than that position(s) still will be replaced from the start of the game, even if no baron or their assistant is ever present.**

A position that is replaced by a somehow non-fillable position is still replaced. This counts for mutual-appointing positions, replacement by not-yet-assigned landholders, replacement by AS_NEEDED positions, or replacement by not-yet-appointed positions.

Replacement does not work if the replaced position is a [LAND_HOLDER], even with civ-positions. In that case, the LAND_HOLDER's position is not replaced. It does not matter if AS_NEEDED is used, or a fixed number, and it also does not matter what type of position the replacer is. So this only works (correctly) with positions that become available by REQUIRES_POPULATION.

## [CONQUERED_SITE]

This tag determines which position is used to assign a [Forced administrator](https://dwarffortresswiki.org/index.php?title=Forced_administrator&action=edit&redlink=1 "Forced administrator (page does not exist)").

In legends mode, this is visible as an event describing the reconquest of the site: a new group is formed and the forced administrator is installed as its ruler.

All positions defined with this tag are assigned during this process, meaning multiple positions can be appointed at once.

The holder of a position marked with [CONQUERED_SITE] cannot appoint any other [SITE] positions, unless the civilization has site variable positions, in which case the forced administrator can appoint such site variable positions (allthough the variable positions for that site need to be created first and such creation only happens during world-gen, but not normal world activities).

Combining [CONQUERED_SITE] with [SITE] causes the position to function both as a forced administrator and as a normal site position available in fortress mode. However, this provides no meaningful additional mechanics and is effectively inferior to using [SITE] alone:

- [APPOINTED_BY] lines are completely ignored, meaning that the roles are automatically assumed.
- [SUCCESSION] is likewise ignored.
- the [CONQUERED_SITE]-position cannot appoint other [CONQUERED_SITE], [SITE] or combined positions.

There have been remarks that reclaiming a fortress is unplayable because of the lack of regular nobles. Unfortunately, it seems that it can't be fixed by modding.

# Availability and visibility

## Availability of (new) positions

Warning: Do not mistake "availability" for "visibility"!

Of all the possible positions existing in your site's entity, there may only be some available.

- Positions with [REQUIRES_POPULATION] require the population to have a specific size.
- Positions with [REQUIRES_MARKET] will only appear in "large" sites (which may have different rules for different site types). This tag has no effect in fort mode.
- Positions that are appointed by positions that have an AS_NEEDED number. The appointable positions only become available after an appointer position-slot is created. This works also on civ-level. If a position is appointed by a Land-holder, it only becomes available, when that level of landholder is created.

Only the replaced positions are culled and are no longer available. A position that requires a certain population will become available, even if it doesn't have [APPOINTED_BY] or [ELECTED]. In that case, see 'automatic assignment' and 'assumption'

In fortress mode, in some cases 'succession' is evaluated immediately after a position becomes available. See: Succession.

## Visibility of positions

A position might be available, but can still be invisible for the player in the [nobles screen](https://dwarffortresswiki.org/index.php/Nobles_screen "Nobles screen"). The positions with their respective holders are visible for players:

- All site-positions that are already filled-in (even if they could not be re-filled-in considering current conditions)
- Site positions that are appointable by a filled-in site position
- Site positions that are appointable by a filled-in civ position, when that civ positions holder becomes a citizen of your fortress.
- Civ positions of units that are also a citizen of your fortress.

If a position becomes available, for example because a certain pop number has been reached, or if it is available from the start(like expedition leader), as long as it cannot be appointed, it still is INVISIBLE for the player.

It might strike someone as odd if a position becomes filled automatically in fortress mode when that position is not even visible. This might be the case if the current holder of a non-appointable position dies or succeeds another position. Regardless of player visibility, these positions will be automatically filled in if the necessary requisitions are met. It might happen with the expedition leader.

A situation with a non-visible but available position, is for example when a position is solely appointed by the expedition leader, when the expedition leader's position is left vacant. It can no longer be appointed by the player and is invisible. Then, it gets automatically assumed, proving that the position still was available.

A position that is both [APPOINTED_BY] and [ELECTED] is visible, but players cannot interact with it.

# [Evaluation of Positions](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Evaluation_of_Positions)

The game does not continuously check whether positions should become available, elected or be [REPLACE_BY]. This is well-known behavior—for example with the [mayor](https://dwarffortresswiki.org/index.php/Mayor "Mayor"), who does not appear automatically when the required population ([REQUIRES_POPULATION]) is reached. Instead, positions must somehow be evaluated. This applies in several other situations as well

**Cases that require a trigger:**

- Election of a newly created position
- Election after the current holder dies
- Automatic assumption of a newly created position (this may take up to a day)
- New citizens (such as migrants) considering available positions
- Premature succession of a newly created position

**Cases that do not wait for a trigger:**

- Succession following the death of the previous holder
- Automatic assumption of existing positions that have become vacant

**Triggers that cause the game to reevaluate noble positions:**

- Succession of a [SITE]-position due to the death of the current holder
- [Election Day](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Election_Day "Advanced entity position mechanics")
- Automatic assumption of a [SITE]-position that becomes vacant
- (Re)assigning any site position manually
- Settlement elevation on the LAND_HOLDER track (e.g. gaining a [Baron](https://dwarffortresswiki.org/index.php/Baron "Baron") or [Count](https://dwarffortresswiki.org/index.php/Count "Count"))

# Gaining a position

There are several ways a unit can gain a position:

- Appointment: A unit is appointed by another unit or by the player.
- Election: A unit is elected by and among the members of the entity
- Assumption: A position is neither elected or appointed: a random unit just simply 'takes' the position
- Succession: a unit is the valid successor of this position(A), either by its current position(B) or because they are that position(A)-holder's heir.

Available positions will automatically be assigned to a random civ member when a new site/civ is created.

## Who can take a position

- If so defined, a unit needs to be the right caste and/or class - it does not seem to work with creature types.
- The unit needs to be an adult member of the site or its parent civ's government; that is also CAN_LEARN or INTELLIGENT (SLOW_LEARNER cannot take positions) or otherwise is able to think.

## Appointment

Positions that have an [APPOINTED_BY:position] token require that position to exist, to be available and appointed. Any position that is APPOINTED_BY can be appointed if the appointer's position is filled in. For site-positions to be appointed, it is required that the appointer is present at that location.

If the appointing unit is temporarily not present, or if that position is not filled, positions depending on it cannot be appointed. This is the case with [militia captains](https://dwarffortresswiki.org/index.php?title=Militia_captains&action=edit&redlink=1 "Militia captains (page does not exist)"), when the [militia commander](https://dwarffortresswiki.org/index.php/Militia_commander "Militia commander") is on a [mission](https://dwarffortresswiki.org/index.php/Mission "Mission").

A site position cannot appoint a civ position _or_ LAND_HOLDER in any way whatsoever.

Civ-level positions can appoint other civ-level positions and site-level positions can appoint other site-level positions.

Contrary to what has been said elsewhere, civ-level nobles also can appoint site-level nobles. They need to be at the site to do so. Landholders can appoint both site-level and civ-level nobles. These systems are therefore not as separate as was assumed.

**Mutual appointment** cannot take place. If these are the only requisites of the position, then the positions will never appear or get filled. These unfillable positions can be put to good use, for example, to replace a position that is no longer needed without creating a new one.

**Self appointment** doesn't normally work. If you have a position that is only appointed by itself, it is never appointed and also cannot be assumed. However, if the position has a number higher than 1, and is filled by multiple units (for example by another position that is now empty), than those units can re-assign or appoint each other from that their shared position.

If an APPOINTED_BY token refers to a non-existing position's code, the effects are as if the appointment token doesn't exist at all.

### Automatic appointment in world-gen and on the civ level

Outside of fortress mode, the game will always attempt to appoint nobles whenever possible, as long as these positions are **available**, even if they are invisible to the player. It shows this message in legends: "(unit name) has been appointed to the position of (position name)"

In world-gen, all positions become available and are automatically appointed, taking population- and appointment-requirements into consideration.

Positions that are REPLACED_BY are culled and won't be filled.

If a citizen of your fortress holds a civ-level position that can appoint another civ-level position, the appointment will happen automatically and without player intervention. It may happen that another citizen of your fortress is appointed by that unit, creating civ-level position holders in your fortress, but it is unknown what is required to force this effect.

### Manual appointments by players in fortress mode

In fortress mode, the positions that need to be appointed stay empty on embark. and it is the player's job to appoint those. A player can appoint a unit to any available position, according to the hereabove mentioned conditions. The player takes the role of the automatic appointment-system, but has no direct control over elections, successions and replacement. There are some differences in what is possible at world-gen sites and at player-controlled sites.

- A position that is appointed by a unit present as a fortress citizen, can be appointed, re-appointed or left vacant. This means also by civ-level nobles living as a citizen in your fortress; not when they are only visiting, like the diplomat.
- A position whose appointing positions are all either vacant or [REPLACED_BY] can no longer be appointed. If the position is already filled, it cannot be reappointed or vacated; the current holder simply remains in office.
- A position that is APPOINTED_BY a unit present as the land_holder of your site, can be appointed, reassigned or left vacant.
- A position that has SUCCESSION BY_HEIR or BY_POSITION can 'initially' be appointed and also re-appointed or left vacant, but as soon as the [nobles](https://dwarffortresswiki.org/index.php/Nobles "Nobles") screen closes, _it can no longer be replaced or left vacant_. From then on, the succession-rules determine who gains that position when the current holder loses the position. This works even if the SUCCESSION:BY_POSITION-position is vacant or replaced.
- A position that is ELECTED nor APPOINTED_BY, can always be (re-)appointed by the player. This is the case with the [Expedition leader](https://dwarffortresswiki.org/index.php/Expedition_leader "Expedition leader"). If it is left vacant however, it cannot be appointed, but will be assumed shortly after.
- A position that is both ELECTED and APPOINTED_BY, cannot be appointed by the player. Contrary to world-gen sites, its slot is visible, but it doesn't show the +-sign. This is either by AS_NEEDED or by a fixed number. Even if the position somehow gets filled (re)assignment is never possible
- A player can appoint a number of units to a position, as much as the NUMBER token dictates. If it is AS_NEEDED, the player may create as many slots as they like, also contrary to world-gen sites.
- A civ-position can never be appointed, even if the appointing civ noble is a citizen of your fortress. A civ position also never can be re-assigned or left vacant, would that position be defined as appointed by a site-position.

## Election

Read more in [Elections](https://dwarffortresswiki.org/index.php/Elections "Elections"). The message that is shown is: "(creature name) has been elected to the position of (position name)"

In worldgen, there is no functional difference between ELECTED and non-appointment, except that elected nobles tend to have high social skills and/or skills related to the position, while non-elected ones are assigned randomly. See: [Elections](https://dwarffortresswiki.org/index.php/Elections "Elections")

A succession goes before an election.

A position that is both ELECTED and APPOINTED_BY never gets elected. Even if the appointees' position somehow gets filled, (re)-elections won't happen. So, it doesn't seem possible to have an elected position become available when a certain other position becomes filled.

An ELECTED civ-(or LAND_HOLDER) position at your site will never be (re)-elected in fortress mode. So real (re-)election only works with SITE-positions.

### [Election Day](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#Election_Day)

Election Day takes place on the 17th of Summer. On this day, a full reevaluation is performed, including all currently elected positions, which are subject to re-election. Contrary to the information on [Elections](https://dwarffortresswiki.org/index.php/Elections "Elections"), nothing occurs at the start of a season.

Positions that are both [APPOINTED_BY] and [ELECTED] will not be re-elected on Election Day when assigned through [SUCCESSION].

### Election Eligiblity

Any citizen may stand for election. Eligibility cannot be restricted using [ACCEPTED_CREATURE], [REJECTED_CREATURE], [ACCEPTED_CLASS], [REJECTED_CLASS], or [GENDER]. Units currently having a [SUCCESSION]-position even may be elected for a position with a [SQUAD]-token, which is otherwise impossible to assign or even succeed.

### Skills

In elections, skills are taken into account for the tokens of the position which is elected.

|   |   |
|---|---|
Relevant skills per position token
|Position Token|Relevant skills|
|Responsibility [[DELIVER_MESSAGES]](https://dwarffortresswiki.org/index.php/Position_token#DELIVER_MESSAGES "Position token")|[Ambusher](https://dwarffortresswiki.org/index.php/Ambusher "Ambusher"), [Observer](https://dwarffortresswiki.org/index.php/Observer "Observer") and [Social skills](https://dwarffortresswiki.org/index.php/Social_skill "Social skill")|
|Responsibility [[ACCOUNTING]](https://dwarffortresswiki.org/index.php/Position_token#ACCOUNTING "Position token")|[Record keeper](https://dwarffortresswiki.org/index.php/Record_keeper "Record keeper")|
|Responsibility [[ESPIONAGE]](https://dwarffortresswiki.org/index.php/Position_token#ESPIONAGE "Position token")|[Schemer](https://dwarffortresswiki.org/index.php/Schemer "Schemer")|
|Responsibility [[HEALTH_MANAGEMENT]](https://dwarffortresswiki.org/index.php/Position_token#HEALTH_MANAGEMENT "Position token")|[Diagnostician](https://dwarffortresswiki.org/index.php/Diagnostician "Diagnostician")|
|Responsibility [[MAKE_INTRODUCTIONS]](https://dwarffortresswiki.org/index.php/Position_token#MAKE_INTRODUCTIONS "Position token")|[Social skills](https://dwarffortresswiki.org/index.php/Social_skill "Social skill")|
|Responsibility [[MAKE_PEACE_AGREEMENTS]](https://dwarffortresswiki.org/index.php/Position_token#MAKE_PEACE_AGREEMENTS "Position token")|[Social skills](https://dwarffortresswiki.org/index.php/Social_skill "Social skill")|
|Responsibility [[MAKE_TOPIC_AGREEMENTS]](https://dwarffortresswiki.org/index.php/Position_token#MAKE_TOPIC_AGREEMENTS "Position token")|[Social skills](https://dwarffortresswiki.org/index.php/Social_skill "Social skill")|
|Responsibility [[MANAGE_PRODUCTION]](https://dwarffortresswiki.org/index.php/Position_token#MANAGE_PRODUCTION "Position token")|[Organizer](https://dwarffortresswiki.org/index.php/Organizer "Organizer")|
|Responsibility [[MEET_WORKERS]](https://dwarffortresswiki.org/index.php/Position_token#MEET_WORKERS "Position token")|[Social skills](https://dwarffortresswiki.org/index.php/Social_skill "Social skill")|
|Responsibility [[RECEIVE_DIPLOMATS]](https://dwarffortresswiki.org/index.php/Position_token#RECEIVE_DIPLOMATS "Position token")|[Social skills](https://dwarffortresswiki.org/index.php/Social_skill "Social skill")|
|Responsibility [[RELIGION]](https://dwarffortresswiki.org/index.php/Position_token#RELIGION "Position token")|[Social skills](https://dwarffortresswiki.org/index.php/Social_skill "Social skill")|
|Responsibility [[TAME_EXOTICS]](https://dwarffortresswiki.org/index.php/Position_token#TAME_EXOTICS "Position token")|[Animal trainer](https://dwarffortresswiki.org/index.php/Animal_trainer "Animal trainer")|
|Responsibility [[TRADE]](https://dwarffortresswiki.org/index.php/Position_token#TRADE "Position token")|[Social skills](https://dwarffortresswiki.org/index.php/Social_skill "Social skill") and [Appraiser](https://dwarffortresswiki.org/index.php/Appraiser "Appraiser")|
|[[SQUAD]](https://dwarffortresswiki.org/index.php/Position_token#SQUAD "Position token")-token|[Tactician](https://dwarffortresswiki.org/index.php/Tactician "Tactician") and [Leader](https://dwarffortresswiki.org/index.php/Leader "Leader")|

## Assumption

A position that is not APPOINTED_BY nor ELECTED, or is appointed by positions that are not available in your site or civ, will be assumable by a random dwarf. If it has responsibilities that require certain skills, then these are taken into consideration on embark, but not when the position is assumed during the actual game.

Normally, one to three units will take the into consideration to assume a position. Most of the time when there are multiple open positions, only a single unit will assume all of them. However, a position that has REJECTED_CREATURE, REJECTED_CLASS, ALLOWED_CREATURE or ALLOWED_CLASS will be filled with all different units, even if the creature or class mentioned is irrelevant. It seems that this forces the game to loop over all the available units.

The message that is shown in Legends mode is: "(unit name) has assumed the position of (position name)". This may also take place in fortress mode, which then shows this message to the player.

If an assumable position becomes empty, it will be assumed within a day. This is the case when you leave the position of expedition-leader vacant. It also happens with entities.

Assumable positions that become empty will not be assumed if that position has a valid [SUCCESSION] -successor. In that case, the successor inherits the position.

Even positions that are somehow invisible because they cannot be directly APPOINTED_BY players, can be assumed.

When you embark, the assumable positions are automatically assigned to a random unit. If there are multiple of these positions at embark, they all are assigned to the same unit. If there are enough positions available, multiple units may gain a position, but often no more than three different ones.

If a dwarf in fortress mode assumes a position, that already has another position, it will leave the current position empty. When that position also is assumed, then this will continue until all positions have a dwarf appointed to them, with no other position.

A unit that already has a position with a [SUCCESSION] token won't take assumable positions into consideration that have a [SQUAD] token. This can be used by the modder to prevent unwanted loss of current positions.

A position that has an appointer which got replaced because of REPLACED_BY, will not become assumable. Also, positions that have an AS_NEEDED appointer that is not yet filled (or ever), will also not be assumed.

## Succession

If a position-holder dies or advances to a new position via succession, the position will be granted to another unit based on the [SUCCESSION] tag. If they have an heir or the succeeding position exists, that unit will be assigned. If not, a new one will be appointed according to the usual rules. The message that is shown is: "(creature name) being the rightful heir, has inherited the position of (position name)"

The succeeding creature will also lose its previous position. When succession is defined using BY_POSITION, the unit naturally loses the referenced position. However, it also loses any other positions it may hold. If a unit could simultaneously inherit multiple positions, the last-defined succession overrides the earlier one, clearing the previously acquired position

Succession works both at site-level and at civ-level, both in world-gen and in fortress-mode. Succession by position on the civ-level is also visible and functional in fortress-mode. If both civ-level nobles are a citizen of your fortress, succession is applied visually. Vanilla example: The [druid](https://dwarffortresswiki.org/index.php/Druid "Druid") is succeeded by the [acolyte](https://dwarffortresswiki.org/index.php/Acolyte "Acolyte"). This means that as soon as the druid dies, the acolyte takes over.

When a position that is succeeded by position becomes available, immediately it is checked if a position-successor is available and the position is filled with that unit. Even if this is an [ELECTED] position, succession goes first. When elections eventually do happen, succession plays no role.

It is possible to assign multiple levels of [SUCCESSION:BY_POSITION] in different positions, creating a line of positions where the death of one causes all those "below" them to advance.

A position can have multiple tokens with position-succession. It looks to be random which one is used. It is not always:

- The first or last defined token
- The first or last appointed unit
- the oldest or youngest
- one with a higher or lower precedence
- a unit with relevant skills

When a position is defined with a Succession-type, that unit cannot have another position that has a Squad-type. If the succession-position itself has a squad, than it can be assigned another position with a squad, but then it will loose the previous succesion position. See further details by "Squad"

Assumed positions can also be succeeded by position, if the current holder dies.

If the successor is an AS_NEEDED position, the used unit will leave a vacant position-slot on its removal by succession. This empty slot remains a real slot, which will only be cleaned up if you (un)appoint a unit to this position-series. It isn't cleaned up after regular position validation.

A civ-level position of a unit living at your site might be inherited by a unit holding that does not currently live at your site. This, unfortunately, moves that position to a unit off site. This may also happen with the landholder of your site, for example when it is succeeded by another civ-level position. This currently poses an unsolved challenge.

### Eligibility for succession

Succession is restricted by the tokens [ACCEPTED_CREATURE], [REJECTED_CREATURE], [ACCEPTED_CLASS], [REJECTED_CLASS] and [GENDER].

### Site and civ combined succession

Succession can work when combining site positions with civ-level positions or land_holders, but only in world-gen mode. In fortress mode, it only works with combining the same level of nobles, with Landholders regarded as civ-level. So, in fortress mode, a site's position cannot succeed a landholder's position and it cannot succeed another type of civ-level position, and vice versa.

This won't work even if the positions:

- are AS_NEEDED or having a fixed number.
- Are LAND_HOLDERs.

### Succession [BY_HEIR]

When a heir is needed for succession, all children and then other relatives are validated. They cannot take the position if their status does not allow it, for example if they have become a member of another civilisation. See: "Who can take a position". If the unit has no valid heir on that location, the position may go to a unit living on another site. This may cause the title of Landholder of some land to be inherited by a unit living somewhere else. That might be a problem, because then you lose your landholders.

### Premature Succession

There are cases where [SUCCESSION:BY_POSITION] is applied prematurely: at the moment a position is first created and becomes appointable or assumable, rather than after a current holder leaves. In this situation, the succession mechanism assigns a holder immediately, without any player interaction.

When a position becomes available for the first time, the game checks whether a valid successor-by-position exists. If so, that unit is assigned instantly. It can affect positions that would normally be appointed or elected by the player, causing succession to trigger before the player has any opportunity to intervene.

This behavior occurs only in Fortress mode, but can be applied both on [SITE]-positions as well in civ-positions. That last one however is a bit harder to control. Example: [The Archduke](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#The_Archduke "Advanced entity position mechanics")

This premature succession only occurs the first time a position becomes available (i.e. when it is created and becomes appointable or assumable). Even if the position remains vacant and the conditions for succession improve later, premature succession will not trigger again. From that point onward, only normal succession rules apply.

Using premature succession, a position that has [ELECTED], [APPOINTED_BY], or both, can be filled directly. Notably, positions that combine [ELECTED] and [APPOINTED_BY] are normally impossible to fill through regular mechanics. Premature succession bypasses both election and appointment entirely, making this combination uniquely reachable through this mechanism.

No initial election takes place, and no subsequent elections will ever occur for that position. Succession always takes precedence over election, both in premature succession and in normal succession cases.

This behavior applies only in Fortress mode, not during world generation. World-gen uses simplified and more efficient mechanics, and this interaction does not occur there. Premature succession can affect both site-level and civilization-level positions.

#### Multiple succession chains

Multiple succession chains may be defined and are resolved in the order they appear in the raws.

If a position has both:

- a direct succession chain (A → C), and
- a multi-step chain (A → B → C),

and intermediate positions are vacant, resolution proceeds according to raw order. A common outcome is:

1. The direct succession (A → C) is applied first, assigning A to C.
2. The remaining chain then advances (A → B).
3. If C still has empty slots, the final step (B → C) may occur.

If position B is already filled, behavior depends entirely on raw definition order:

- nothing may happen, or
- B may move to C first, followed by A moving to B.

#### Working triggers

Premature succession is triggered when a succeedable position is created under the following conditions:

- The succeedable position is created because its [REQUIRES_POPULATION] threshold is reached. This applies even if the position is not [APPOINTED_BY]. Premature succession takes priority over automatic assumption (e.g. the mayor declaring themselves within a day).
    - The position must either be assumable or appointed by an existing position. When said appointer-position also just has been created, the premature succession of the succeedable position happenes, even when the appointer-position is empty.
- The succeedable position can be [APPOINTED_BY] another position of the same level (site or civ) that has just been created because its [REQUIRES_POPULATION] was reached.
- The succeedable position can be appointed by another [SITE] [AS_NEEDED] position that has just been created and filled.
- The succeedable (site or civ) position is [APPOINTED_BY] the [LAND_HOLDER] position, which has just been created due to site elevation. This typically resolves when the diplomat leaves the map, at which point the landholder position becomes active.
- If all other requirements are met, premature succession can occur immediately after unpausing following embark, for positions with [REQUIRES_POPULATION:7].

#### Non-working (triggers)

Premature succession does **not** occur in the following cases:

- An [AS_NEEDED] succeedable position slot is manually created by the player while its succeeding position is already filled. [AS_NEEDED] positions must always be appointed after creation.
- The succeeding position is filled after the succeedable position becomes available. The moment of creation is the decisive trigger; filling the source position later is too late.
- The succeedable position can be appointed by another site or civ position with a fixed number of slots that has just been appointed. In this case, the succeedable position is just available for appointment itself, nothing more
- Any situation occurring during world generation.
- The succeeding position is [REPLACED_BY] the succeedable position. In this case, replacement removes the unit from the source position first, leaving no holder available for the succession mechanism to use.
- The position is [APPOINTED_BY] a civ-level position, that just became a citizen of your fortress. It must be noted that those civ-level positions were active all that time and the succeedable position could be appointed even before. The monarchs arrival does not trigger premature succession
- A [SQUAD]-position cannot inherit another [SQUAD]-position. This also means that premature succession will not work in this case.

# Losing a position

A unit can lose a position when:

- It dies
- It succeeds another position, even if it has nothing to do with the previous position.
- It is assigned to another SQUAD-holding position
- It is convicted of a crime.
- Another unit is ELECTED for the position
- It is convinced by an adventurer to give up its position, or is overthrown in a coup.
- Its position becomes replaced
- Another unit is appointed by the player, or the position is left vacant.
- It has assumed another position (of the same entity), as this always leaves the previous position vacant.

Note: A unit does not lose a position when the unit leaves the group (entity). Neither will a unit lose a position, if the corresponding entity is considered to be dead.

# Embarkment

Two types of positions are automatically filled by embark.

- Positions without [APPOINTED_BY] or [ELECTED] (assumable). All these positions, even with a NUMBER higher than 1, are all filled with one to three dwarves. Contrary to assumption, this doesn't take into account any limitations. REJECTED_CLASS, ALLOWED_CLASS, REJECTED_CREATURE, ALLOWED_CREATURE and GENDER are applied, but without the normal spread you may expect with assumptions. Also it doesn't look at [SUCCESSION] and [SQUAD] limitations.
- Positions that are elected are filled-in by the normal election rules.

Positions that have a defined appointer are never initially filled at embark.

All positions that don't have [REQUIRES_POPULATION] or with a [REQUIRES_POPULATION] of 7 or lower, will be available at embark.

# Land Holders

A Landholder is a **special civ-level noble** who gets a certain piece of land to hold, when that land is elevated to a certain level, determined by the [LAND_HOLDER] tag, and by the landholder triggers in the game's settings. In vanilla, these are the baron, the count and the duke.

A unit gaining the landholder position does not migrate to that specific named land. In world-gen, they stay just where they are, probably at the capital. In fortress mode, you can suggest a citizen for the role. So for the time being that works.

Succession is then a real issue. If you use BY_HEIR, its solved when that landholder has children living at your site. But when its not the case, the title just goes to anyone randomly. Succession BY_POSITION works, but only in the civ-chain, and there's no way to guarantee a civ-holder is at your site at that time. Even with 'automatic spread' positions, it goes to one of them randomly.

## Functioning of the regular landholder chain

The distinct difference between a landholder and a regular civ-level noble, is that a landholder may gain the position of landholder "of (sitename)" They are then seen as ruler of a particular site.

For a land_holder position to function as such, it has a few requirements:

- NUMBER:AS_NEEDED
- The first landholder-number of 1 is defined.
- No SITE (so civ) tag in that position.
- REPLACED_BY the next level landholder

If a landholder is defined with differentiating properties, it will function like a regular noble. A higher-up landholder that lacks the required tokens or connections will then not be used in elevation.

If a fortress meets the trigger for a new LAND_HOLDER tier when a caravan leaves, then the next time the outpost liaison or equivalent arrives, they will offer to make you an official colony, which will allow you to select all positions for that LAND_HOLDER level. Each time they appear, the outpost liaison will only promote your fortress one tier up the LAND_HOLDER track.

The landholder's LAND_NAME is not required for the functioning of this system. If omitted, messages will be shown with a more generic text.

## Appointment

This mechanism differs from the regular methods of position management. It ignores all regular appointment- and election rules, so it more or less functions like automatic assignment. A landholder is, in vanilla, appointed by the monarch. Changing this doesn't seem to do anything. If they are appointed by a site-position, a not-yet-existing civ-position, or not appointed at all: the system keeps working as usual.

A landholder can appoint civ-positions and site positions. This works as expected: the positions only are appointed then when that landholder becomes available on civ-level or when he arrives at that site for site-level positions.

If your rank of landholder is the first of its rank in the realm, and is the sole appointer of some civ-position, then immediately as it gains the title, it will appoint the empty civ-slots. This may happen on your site, but the frequency and certainty is hard to determine.

## Succession

Succession rules are applied to some extent:

- In world-gen it works according to succession rules, and site-positions can be used here. This means that a site position or a civ-position can inherit a landholder position, and vice versa.
- In fortress mode, once a landholder has been appointed, it then can inherit civ-level positions, and vice versa. This means that your baron can become king.
- Succession rules do not apply within the [LAND_HOLDER] chain; a count will not inherit a baron's land. This is because succession does not work well with the AS_NEEDED token.
- Premature succession works in fortress mode with landholders. If a unit gets a landholder's position and that landholder is the appointer of an as yet empty position, which is defined as succeeding from a third one, then the succession is immediately applied. The landholder themselves can even be the successor of a newly created position.
- A landholder's position is, in fortress mode, not successionable by a site-position or vice versa

### Impossibilities for succession by a site-position

It would be very beneficial if the landholder can be succeeded by a [SITE]-position. So far, the following tests have not lead to positive results:

- making landholder and site-position both non-[DUTY_BOUND]
- make the site-position be [APPOINTED_BY] the landholder and/or the monarch
- give landholder and site-position [REJECTED_CREATURE]
- Let the monarch live at your site when succession could happen.
- Let the site-position be [REPLACED_BY] the landholder.

If the vanilla [SUCCESSION:BY_HEIR]-tag is omitted, a seemingly random unit somewhere in the realm is assigned this position.

## Nomination

The player is able to nominate a unit to become the LAND_HOLDER, but this only works with units of [LAND_HOLDER] level 1. The player can select all units, only limited by the PRECEDENCE of the current units' positions.

A unit that has a position with a PRECEDENCE lower or equal to that of the landholder's position, cannot be selected. This means that a baron (or count) from another site or the monarch cannot be selected, because their precedence is lower or equal.

The GENDER token does not work here: also units with the wrong gender (sorry) can be selected.

## Levels

In mods, up to 10 levels of LAND_HOLDER may be defined.

If a landholder is replaced by a wrong landholder number (1 replaced by 3), then the number 3 is still correctly attached to the settlement.

If the current landholder has the highest available landholder number, then the next elevation will not happen - the diplomat will not elevate your fortress to a higher position, even if that position might be REPLACED_BY a lower landholder.

These chains do work:

- 1 -> 2a - > 2b -> 3
- 1 -> 3 -> 2 -> 4

These chains do not work:

- 2 -> 3 (need to start at 1)
- 1 -> 4 -> 2 -> 3 (stops after 4 as the highest)
- 1a -> 2, 1b -> 2 (only 1a and 2 work, 1b is not used)

## Moving landholders

It may happen that a land-holder no longer lives at the site which they are the landholder of, specifically when the current landholder dies, leaving the title to an heir living somewhere else.

To prevent this from happening, you can make their succession from heir and make sure that their kids live at your site. Or, you can make their position succeeded by another civ position, and make it so that this civ position is somehow available on your site. But if multiple of these positions exist, it cannot be guaranteed that a citizen of your fortress will inherit the title.

In world gen, a landholder lacking the DUTY_BOUND-token will also move to the site they like, according to legends mode.

## Replacement by a generic civ-position

If a landholder is replaced by an AS_NEEDED non-landholder civ-position, then this will work: the current landholder loses that title upon settlement-elevation and gains that civ-title. However, the civ-title lacks the landholder-property of being attached to the land. It will not show the name of the settlement alongside the position's name. So no "minister of Shovelmounts"

If a landholder is replaced by a general AS_NEEDED civ-position, that itself is also replaced by a generic AS_NEEDED civ-position, then firstly the elevation is executed and also the unit gains that new position. However, he immediately loses it, because an AS_NEEDED position that is replaced by another position can be filled initially, but units wont be able to hold that title.

## Landholder with fixed number

A landholder's position that has a fixed number will be created and filled directly when the civilisation is born, so this position slot is then not available for the regular landholder-mechanic and will also not be used. That landholder will thus not be attached to a settlement.

It doesn't matter if the landholder's position is connected to the regular landholder's-chain with the REPLACE_BY token.

## Responsibilities

When given a certain [RESPONSIBILITY], a landholder may function as a regular civ-level noble. If the position has [TRADE] or [OUTPOST_NEGOTIATING] responsibilities, then the landholder functions both as a diplomat and as an actual land holder. A landholder with the [MILITARY_STRATEGY] responsibility will travel around taming creatures in world-gen, according to legends mode.

Besides that, the responsibilities work the same as with any other on-site living position-holder, civ or otherwise.

# Military

## Squad management

In the vanilla game, the Squad interface only becomes available after a militia commander has been appointed. Until then, the window displays:You must appoint somebody first to create a squad.

What’s surprising is how this is determined internally. In the entity raw definition, **only the last two positions that include a [SQUAD] token are checked** to decide whether the interface is accessible at all. As a result, if your hierarchy defines commanders A through E, appointing **Commander D or E** unlocks squad formation, while appointing A–C does nothing.

In other words, squad availability is not tied to _having a militia commander_, but to _which specific positions happen to be last in the raw list_—a notably hacky implementation.

These 'last two' are always the last two **available positions.** So if they get [REPLACED_BY] or become available because of [REQUIRES_POPULATION], the game adapts to those.

## Squad assignment

Squads can be assigned, even if the leader position has no holder.

A specific unit can only have one position associated with a squad. If it gains another 'squad holding position', it is unassigned from the first one. This does not work with a 0-squad, so only 1+squads are taken into consideration. This technique can possibly be used to distribute all positions equally among all citizens. It does however not work with election and assumption.

If a civ-level position is associated with a squad and it gets a site-level squad-holding position assigned, it loses the current civ-position.

Squads can get really messed up, if you make the position (or multiple) either elected or not-elected and not-appointed, then this can cause the game to assign multiple squads to the same unit. Automatic assignment and election does not take squads into account, but the nobles screen does. This can cause the positions to be cleared as the game figures out that they have more than one position, and immediately get elected or assumed again.

Positions that cannot have a squad-position:

- A site- or civ-position with a [SUCCESSION] token cannot be appointed a squad-holding-position. The other way around, however, does work. For example, if a site-position with a [SUCCESSION]-token is appointed to a unit that has already a position with [SQUAD]. But when that squad position is assigned to another unit, it cannot be assigned back.
- A position with [SUCCESSION] can also not be assigned as a **member** of a squad.
- A squad-holding position with a formed squad cannot be appointed to another squad holding position.

If a position has at least one squad member, it cannot be left vacant. First, the squad has to be disbanded, then the position may be cleared.

## 0-squads

A 0-Squad is defined in a position as [SQUAD:0:member:members]. It does not seem to do anything useful as of now.

- It cannot be used to activate the [military interface](https://dwarffortresswiki.org/index.php/Squad "Squad")
- It does not restrict the assignment of [SUCCESSION] positions.
- Assigning this position does not clear any previously held squad position.
- The [Leader](https://dwarffortresswiki.org/index.php/Leader "Leader") and [Tactician](https://dwarffortresswiki.org/index.php/Tactician "Tactician") skill are not marked as relevant skills and are not taken into account in elections.
- It cannot be formed as a squad.

# Further testing

The following questions may need additional testing. Feel free to add or answer

- Everything regarding COMMANDING and army-structure
    - [[1]](http://www.bay12forums.com/smf/index.php?topic=175437.msg8331668#msg8331668)
    - [[2]](http://www.bay12forums.com/smf/index.php?topic=165213.msg8335682#msg8335682)
    - [[3]](http://www.bay12forums.com/smf/index.php?topic=174584.msg8026854#msg8026854)
- Stuff about the monarch, its arrival and its entourage.

# Oddities (Bugs)

Almost everything on this page could be called an oddity. Because of their unexpected usability, some may also be referred to as “undocumented features.” Others, however, are simply odd and not particularly useful, yet I hesitate to call them “bugs.”

- If a certain threshold is reached that makes an elected position electable, and the triggering event that initiates this evaluation is an assumption, then the resulting assumption works partially as an election. It referred to in the messages as an election and the [REJECTED_CREATURE]-token is not applied, like it is with assumptions.

# Examples

### The Founder

The founder is a single dwarf, appointed at embark. They will be the only one ever to have this position and are not replaceable. When they lose their position some way, the position will not be assumed by another dwarf.

|[show][[Select all](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#)]<br><br>The Founder|
|---|

### Marriage bar

Dwarven matrons are held in great honour. Upon marriage, a female dwarf is no longer expected to perform menial labour. All dwarven males hold this position by default, granting their spouses exemption from menial work.

The position becomes available with the arrival of the first migrants; otherwise, on embark, it would be assumed by females. Its succession rule is non-functional, but this prevents the player from unassigning the position. A squad size of 1 and the succession rules together prevent a unit from assuming the position more than once.

With precedence set to NONE, the position name is hidden, while LAND_NAME remains visible on the nobles screen. All married females receive the suffix “, Mrs.” and are marked as Nobles.

The practical usefulness of this position is debatable, but it serves as a clear demonstration of several mechanics.

|[show][[Select all](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#)]<br><br>Mrs. Urist|
|---|

### The Archduke

The archduke is the leader of the civilization, but exists only from landholder 4-level. Until then, its position remains vacant. When a settlement is elevated to tier 4 (grand duke), the grand duke can appoint the ruler of the civilisation, the archduke. Because of 'Premature Succession', they themself inherit that position immediately, but only when in fortress mode. Its heir then becomes grand duke.

|[show][[Select all](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics#)]<br><br>The Archduke|
|---|

[Categories](https://dwarffortresswiki.org/index.php/Special:Categories "Special:Categories"): 

- [Fine Quality Articles](https://dwarffortresswiki.org/index.php/Category:Fine_Quality_Articles "Category:Fine Quality Articles")
- [Modding](https://dwarffortresswiki.org/index.php/Category:Modding "Category:Modding")
- [Entities](https://dwarffortresswiki.org/index.php/Category:Entities "Category:Entities")
- [Guides](https://dwarffortresswiki.org/index.php/Category:Guides "Category:Guides")

## Navigation menu

- Not logged in
- [Talk](https://dwarffortresswiki.org/index.php/Special:MyTalk "Discussion about edits from this IP address [alt-shift-n]")
- [Contributions](https://dwarffortresswiki.org/index.php/Special:MyContributions "A list of edits made from this IP address [alt-shift-y]")
- [Create account](https://dwarffortresswiki.org/index.php?title=Special:CreateAccount&returnto=Advanced+entity+position+mechanics "You are encouraged to create an account and log in; however, it is not mandatory")
- [Log in](https://dwarffortresswiki.org/index.php?title=Special:UserLogin&returnto=Advanced+entity+position+mechanics "You are encouraged to log in; however, it is not mandatory [alt-shift-o]")

- [Page](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics "View the content page [alt-shift-c]")
- [Discussion](https://dwarffortresswiki.org/index.php/Talk:Advanced_entity_position_mechanics "Discussion about the content page [alt-shift-t]")

- [Read](https://dwarffortresswiki.org/index.php/Advanced_entity_position_mechanics)
- [Edit](https://dwarffortresswiki.org/index.php?title=Advanced_entity_position_mechanics&action=edit "Edit this page [alt-shift-e]")
- [View history](https://dwarffortresswiki.org/index.php?title=Advanced_entity_position_mechanics&action=history "Past revisions of this page [alt-shift-h]")

### Search

[](https://dwarffortresswiki.org/index.php/Main_Page "Visit the main page")

- [Main page](https://dwarffortresswiki.org/index.php/Main_Page "Visit the main page [alt-shift-z]")
- [Centralized discussion](https://dwarffortresswiki.org/index.php/Dwarf_Fortress_Wiki:Centralized_Discussion)
- [Community portal](https://dwarffortresswiki.org/index.php/Dwarf_Fortress_Wiki:Community_Portal "About the project, what you can do, where to find things")
- [Recent changes](https://dwarffortresswiki.org/index.php/Special:RecentChanges "A list of recent changes in the wiki [alt-shift-r]")
- [Announcements](https://dwarffortresswiki.org/index.php/Dwarf_Fortress_Wiki:Announcements)
- [Random page](https://dwarffortresswiki.org/index.php/Special:Random "Load a random page [alt-shift-x]")
- [Random page by namespace](https://dwarffortresswiki.org/index.php/Special:RandomByNamespace)
- [Help](https://www.mediawiki.org/wiki/Special:MyLanguage/Help:Contents "The place to find out")

### Tools

- [What links here](https://dwarffortresswiki.org/index.php/Special:WhatLinksHere/Advanced_entity_position_mechanics "A list of all wiki pages that link here [alt-shift-j]")
- [Related changes](https://dwarffortresswiki.org/index.php/Special:RecentChangesLinked/Advanced_entity_position_mechanics "Recent changes in pages linked from this page [alt-shift-k]")
- [Special pages](https://dwarffortresswiki.org/index.php/Special:SpecialPages "A list of all special pages [alt-shift-q]")
- Printable version
- [Permanent link](https://dwarffortresswiki.org/index.php?title=Advanced_entity_position_mechanics&oldid=315875 "Permanent link to this revision of the page")
- [Page information](https://dwarffortresswiki.org/index.php?title=Advanced_entity_position_mechanics&action=info "More information about this page")

### In other languages

- [Русский](http://www.dfwk.ru/index.php/Advanced_entity_position_mechanics "Advanced entity position mechanics – русский")

- This page was last edited on 29 April 2026, at 17:35.
- Content is available under [GFDL & MIT](https://dwarffortresswiki.org/index.php/Dwarf_Fortress_Wiki:Copyrights "Dwarf Fortress Wiki:Copyrights") unless otherwise noted.

- [Privacy policy](https://dwarffortresswiki.org/index.php/Dwarf_Fortress_Wiki:Privacy_policy "Dwarf Fortress Wiki:Privacy policy")
- [About Dwarf Fortress Wiki](https://dwarffortresswiki.org/index.php/Dwarf_Fortress_Wiki:About "Dwarf Fortress Wiki:About")
- [Disclaimers](https://dwarffortresswiki.org/index.php/Dwarf_Fortress_Wiki:General_disclaimer "Dwarf Fortress Wiki:General disclaimer")

- [![[Watch It Later/attachments/9939f1d5ca7dda20af4033547d933162_MD5.png]]](http://www.gnu.org/copyleft/fdl.html)
- [![[Watch It Later/attachments/a74b40a86670a28647499a15d7146ba7_MD5.png]]](https://www.kitfoxgames.com/)