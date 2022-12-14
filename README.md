# SpellBook Abridged Reborn
#### Version 3.0.0 for WotLK Classic

*Reborn Author: Crusherexe (crusherexe+sbar@protonmail.com)*

*Original Author: LBXZero (lightning_bug_x@yahoo.com)*

## Description:
With the return of Vanilla World of Warcraft comes the return of learning spells by rank. 
For warriors and rogues, this is not much of a problem as the newer rank of the ability/spell 
replaces the old one, because everything is the same except the effect power.  But for all 
classes that use mana, the spellbook gets filled with pages of the multitude of ranks for 
each spell.

After some time of playing a mage, I made an addon during Burning Crusade to condense the 
spellbook and display the ranks in a different way.

### SpellBook Rank Filter

This version is more minimal than my original version.  I made the filter and modified a few 
functions in SpellBookFrame.lua to adapt the base Spellbook to accept a custom spell list.  
For this addon, it filters the spellbook to show only the last rank of each unique spell.  To 
view the lower ranks, I added a check button "Rank Filter" that you can toggle to switch 
between the filtered list and the full list.

### Auto UpRank Feature 

The option button "Auto UpRank" enables/disables a feature that will automatically replace 
certain spells on your action bar.  When you learn a spell, this function checks if you have 
a lower ranking version of the spell in the spellbook.  If it finds a lower ranking spell, it 
will replace every instance of that rank of spell currently in your action bars with the spell 
you just learned.

 -  If you learn Fireball (Rank 5), every instance of Fireball (Rank 4) in your action bars 
	will be replaced by Fireball (Rank 5).  If Ranks 1, 2, or 3 of Fireball exist in the 
	action bars, those will be left alone.

The reason I went for this method so far for replacing spells is that if you have a spell that 
is lower rank than the highest rank you had previously, then you must have purposely set that 
specific rank of the spell.

Automatically replacing lower rank spells is a complicated scenario.  Some spells are not using 
the highest rank because the player forgot to set them.  Some spells are purposely set to a 
lower rank for a reason.

Macros are not affected.  Any macro using just the name of the spell without the rank should 
automatically use the highest available rank of the spell.

### SpellBook Shapeshift/Stance Highlighting

This feature was added because I remember some old requests from back in Burning Crusade to help 
Feral Druids find their shapeshift form specific abilities.  This is my current implementation 
based on what I know the WoW UI provides.  This addon can detect if a spell requires a 
specific shapeshift form or stance.  Instead of filtering out the spells, I determined changing 
the icon to represent if you are in the correct form or stance is more ideal.

If enabled in the "Options" tab provided, colors for the spell names, spell subtext, and spell 
icons can be changed.  Currently, you can change the Spell Name color and Spell Subtext Color and 
can alter the Icon's color.

By default, I have this feature disabled, as not to alienate people who don't care for it.

Normal Colors will be the standard colors for all spells.  I figured that some people may want a 
different Spell Name color than the default yellow.

In Form Colors are a special color set if the spell requires a shapeshift form or stance and 
the player is in that form.  For example, a Warrior in "Battle Stance" would have "Charge" 
highlighted the selected color.

Out of Form Colors are a special color set if the spell requires a shapeshift form or stance and 
the player is not in that form.  For example, a Warrior in "Defensive Stance" would have "Charge" 
highlighted this color instead of the normal or in-form colors.

## Installation
To install this addon, just copy the folder "SpellBookAbridged" from this zip file into the 
"Interface\Addons" folder for WoW Classic.

## Configuration
There are no special options to configure.  You just have the "Rank Filter" and "Auto UpRank" 
check boxes in the Spellbook to toggle.  These options will save when you close the game.

The Rank Filter Button can be dragged to a different location by press and holding 
"Control + Right Mouse Button".

To reset the Rank Filter Button to its home location, use slash command "/sba".


## Other Notes
The Pet Spellbook for Hunters is not affected, as it doesn't need anything.

My goal is to append onto the existing Spellbook in WoW's UI in order to minimize conflicts 
with other addons that may alter the Spellbook.  With the next potential feature I am reviewing 
to add into the Spellbook, my goal to keep the Spellbook simple may change.

