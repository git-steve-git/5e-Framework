# 5e-Framework

A comprehensive 5th Edition Dungeons & Dragons Framework for MapTool with character sheet and character creation tools, a compendium of items, features, spells and creatures and campaign management tools.

Made by rtakehara.  It's an amazing framework and I highly recommend checking out his main branch for the latest updates as well as tutorials, etc.  Don't forget to check out his Patreon if you want to reward his fantastic work!

## Forkables

The main reason for this fork is to clean up the Equipment tables for use with my imported items.  The way I choose to format item descriptions is not exactly the same as the way he does it, and I've found a few glitches with they way they are subsequently displayed in the main branch.  Sometimes items are assigned to incorrect areas (Wand of Orcus showing up in the Armor table) or just all over (Apparatus of Kwalish is EVERYWHERE!)

The issue appears to stem from the fact that the macros use regex that scans the whole item description looking for keywords, and sometimes I suppose those regexes find a match when they shouldn't.  When importing items myself, I add an additional field in the JSON object which explicitly IDs the item type, and I've altered the macros that built the Equipment table to look for those tags instead.
