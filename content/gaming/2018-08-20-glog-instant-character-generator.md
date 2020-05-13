---
layout:  
title: GLOG Instant Character Generator
date: '2018-08-20T08:03:00.003-07:00'
author: Jeff Russell
categories:
- Gaming
tags:
modified_time: '2018-08-23T13:39:08.508-07:00'
blogger_id: tag:blogger.com,1999:blog-7657840612384361644.post-7016812135422434218
blogger_orig_url: https://blessingsofthedicegods.blogspot.com/2018/08/glog-instant-character-generator.html
---

<table> <tbody> <tr class="odd"> <td><a href="https://78.media.tumblr.com/be0467003c7bce84b56b098e17b4b80c/tumblr_pcja7ddO1s1rskzz1o1_1280.jpg"><img src="https://78.media.tumblr.com/be0467003c7bce84b56b098e17b4b80c/tumblr_pcja7ddO1s1rskzz1o1_1280.jpg" width="223" height="320" /></a></td> </tr> <tr class="even"> <td>From <a href="http://mischeviouslittleelf.tumblr.com/">mischeviouslittleelf.tumblr.com</a></td> </tr> </tbody> </table> 
  

I made a character generator for Arnold's excellent [GLOG](http://goblinpunch.blogspot.com/2016/05/the-glog.html). I'm pretty jazzed about it. To use, simply set the toggles at the top to any inputs you want specified (or leave them random) and it'll spit out a fully fledged character. Goes from levels 1 to 20. If you want to set Level, Class, or anything else (instead of random), you'll need to make a copy on your own Drive or download it. Check it out.  
  

  
(Or open in its own tab [here](https://docs.google.com/spreadsheets/d/1jsdfz7WGcVoFsd4KEGcYsyN8PFpExFddB1Qhtc7gPmw/edit?usp=sharing))  
  

  - Races are Arnold's and come from
    [here](http://goblinpunch.blogspot.com/2016/12/designing-races.html)
    and
    [here](http://goblinpunch.blogspot.com/2013/10/i-killed-all-humans.html).
  - Classes are also Arnold's and come from
    [here](http://goblinpunch.blogspot.com/2016/05/the-glog.html) and
    [here](http://goblinpunch.blogspot.com/2016/09/the-glog-wizards.html). 
  - Random items are also also Arnold's and comes from
    [here](http://goblinpunch.blogspot.com/2017/06/adventuring-gear-alchemy-items.html).
  - Names, some of the looks, and some of the quirks are from *[Maze
    Rats](https://www.drivethrurpg.com/product/197158/Maze-Rats)* by Ben
    Milton
  - Basic methodology from Brendan S
    [here](http://www.necropraxis.com/2018/07/22/random-table-format-wars/)

### How to Modify for Your Own Nefarious Purposes  **First, Learn the Basics**  1\. Read Brendan's explanation of the underlying method [here](http://www.necropraxis.com/2018/07/22/random-table-format-wars/)  **   **  **Next, Create Your Own Copy to Work In**  1\. Either download the [sheet](https://docs.google.com/spreadsheets/d/1jsdfz7WGcVoFsd4KEGcYsyN8PFpExFddB1Qhtc7gPmw/edit?usp=sharing)as an Exel file or else Make a Copy on your own Drive so that you can edit it 
  

**If You Modify An Existing Table**  Make sure you double check that the named range it's a part of covers your changed entries and no empty space. All named ranges correspond to the title at the top of the range (except with real spaces instead of underscores) 
  

**If You Want to Add an Entirely New Table**  Make some space for it on the "Character" tab, then follow Brendan's instructions above 
  

**If You Want to Add a New Race**  1\. Create a new column  2\. Use the top row to label it "[NAME] Race Template"  3\. Put all racial information in cell immediately below that  4\. Click on cell, then click the "Data" menu and select "Named Ranges"  5\. Select "Add a Range", title it "[NAME]_Race_Template" - for example "Ratman_Race_Template"  6\. Add the name of the race to the "Races" table. Make sure any spaces are underscores "_" - example: "Iron_Ghost_Men"  7\. Check to make sure the "Races" named range includes your new name, modify it to include if needed  8\. If the race modifies any stats (attributes, move, stealth, et cetera), you'll have to modify the appropriate stat output to look for that race name in "Race_Output" with a conditional 
  

**If You Want to Add a New Class**  1\. Create a new column  2\. Use the top cell to label it "[Name] Class Templates"  3\. In first through fourth cell, put Templates A, B, C, D for that class. I recommend you just put the names of the abilities, not a full explanation  4\. In the fifth cell, put the class's Prime Ability  5\. In the sixth cell, put the class's Starting Equipment  6\. In the seventh cell, if the class allows for spellcasting, put "TRUE"  7\. Highlight the cells you just filled and click on "Add a Range" (Data\>Named Ranges) and name it "[NAME]_Class_Templates" - note the plural (for example "Fighter_Class_Templates")  8\. Add the class name to the Classes table, being sure to use underscores for any spaces, then check to make sure the "Classes" named range covers it  9\. Under these seven cells, create a label for "[Class Name] Skills"  10\. On the three rows below, write in the three background skill options for this class to begin with  11\. Name the three skill range "[Class Name]_Skills" 
  

**If You Add a Spellcaster and Want to Add Their Spells**  1\. Create a new column  2\. Label it "[Class Name] Spells"  3\. Add spells in cells 1-14  4\. Select list of spells and "Add a Range" (Data\>Named Ranges), naming it "[Class Name]_Spell_List" 
  

### Notes and Assumptions 
  - Your "primary" class is assumed to the one you have the most
    templates in, and in the case of a tie, the one you had first
  - "Spells" are assumed to accumulate at one per level, and I have not
    been able to figure out how to prevent duplicates
  - This "effective levels" nonsense was my stop-gap way of making sure
    that multi-class spellcasters don't have oodles and oodles of spells
    - it multiplies your level times the number of templates out of 4
    you have in that class, and then assumes you have that many levels
    worth of spells from the template
  - Duplicate spells are quite possible - feel free to either re-roll or
    assume duplicates are wasted
  - No matter the level, every character starts with first level gear -
    you might want to adjust if you're creating higher level characters
  - Characters are assumed to have the minimum experience for the level
    selected
  - Characters get 3 skills at level 1 and then up to their level in
    random skills at a random rank capped by level - if any skill comes
    up a "0", then no further skills are known
  - In Class Templates, rows 1-4 are what you get for each level of a
    class you take, Row 5 is the Prime Ability for that class, and Row 6
    is the class's starting equipment, Row 7 specifies whether it's a
    spellcasting class
  - This does not yet calculate encumbrance or assign gear to slots,
    sorry
  - The other pain in the ass thing to modify will be the stats that are
    upgraded by different class templates (Movement, Initiative,
    Stealth, HP, Save) - removing classes won't hurt the calculations,
    but if you add new classes that modify stats, you'll have to do that
    manually. I could have done a stat line modification per template,
    but there werent enough to make it seem worthwhile, and doing the
    "every two templates" thing would have been challenging
  - I went ahead and made Dog a race template and removed it from the
    first level template for "Really Good Dog" and made "Really Good
    Dog" the only playable class for that race. This does currently have
    the effect of making Really Good Dog slightly more common than it
    would be if it was random among the classes (more classes than
    races), which I'm fine with. If you don't want to play a dog, just
    reroll. Also, if you specify a class but go for a random Race, you
    may end up with "Really Good Dog" instead of your specified class
  - Most classes don't have a prime ability because that's something
    Arnold came up with after putting out the Martial classes. I thought
    about inventing my own, but decided to go "by the book" for now
  - The different wizards can only get spells 1-6 at level 1, 1-8 at
    level 2, 1-10 at level 3, and 1-12 at level 4 and beyond. I
    arbitrarily decided that level 19 and 20 characters have a shot at
    the Legendary spells (13 and 14)
