## [unreleased]
 - Wrath of the Lich King update
 - New management (thanks LBXZero)

## [2.6.4]
 - Some code clean-up

## [2.6.3]
 - Fixed a bug in how frames applied to SpellButtons from other addons are applied.
  Only frames that inherited "Button" at one point are raised to top.
 - Tweaked how Form/Stance custom coloring is applied.
  The Form/Stance coloring should apply last so that it overrides a default set by a
  skin addon for the SpellBook only when the highlighting is enabled.

## [2.6.2]
 - Attempt to fix the random "attempt to index upvalue" error

## [2.6.1]
 - Update TOC to 1.13.3
 - Fixed error caused when Spellbook closes while "Options" tab is displayed followed by 
  learning a new spell

## [2.6]
 - Added option to customize Spell Name and Spell Subtext colors as well as alter the color 
  of the Spell's Icons.
 - Shapeshift/Stance Highlighting colors can be changed and toggled on or off

## [2.5 (Beta)]
 - Fixed issued where Multibar Grids hide and stay hidden when the Spellbook closes.
  (Design oversight in Blizzard's Code)
 - (Beta) Added feature to highlight spells based on being in the required shapeshift form 
  or stance.

## [2.4]
 - The Spellbook will close and not be allowed to show during combat, preventing potential
  errors from combat lockdown.
 - Added basic Auto UpRank feature

## [2.3]
 - Added the ability to relocate the Rank Filter Button
 - Fixed compatibility issue with the addon "Clique"

## [2.2]
 - Fixed the issue where spells cannot be cast directly from the Spellbook
 - Fixed another design oversight where Addons can call spell tab information before the 
  addon completes loading

## [2.1]
 - Changed when the Spell List is generated to ensure it is made before the Spellbook updates.
 - Fixed a design oversight that prevented Addons that used the unused spell tabs from 
  properly working.

## [2.0]
 - Addon made
 - Functions in default WoW UI that are modified:
   - SpellBookFrame.lua
   - SpellBookFrame_Update (Hooked and appended)
   - SpellButton_UpdateButton (Replaced)
   - SpellBook_GetCurrentPage (Replaced)
   - SpellBook_GetSpellBookSlot (Replaced)
   - SpellBookFrame_UpdateSkillLineTabs (Replaced)
   - SpellBook_UpdatePlayerTab (Replaced)
   - SpellBookFrame_OpenToPageForSlot (Replaced)
   - v2.2 SpellButton_OnClick  (Blocked)
