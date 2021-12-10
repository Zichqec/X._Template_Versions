This template is originally based on Zarla's GT Template, though I have made numerous changes since then. If you need a template that is more of a walkthrough, try that one here: http://ashido.com/ukagaka/

You're using X. Template YAYA - v1.1.3
You can use the 'Check Template Version' button to check if there's a new version! Or you can check on my website here: https://zichqec.github.io/s-the-skeleton/xtemplate

If you find any bugs in this template, please tell me so I can correct them!

Feel free to contact me on Discord, or on any of my social medias. My website is here for more info (my socials are linked at the bottom) https://zichqec.github.io/s-the-skeleton/

This ghost includes a to-do list of the basic stuff every ghost needs. If you want to use it, type %(debug = 1) into script input to turn on debug mode. That will give you a menu option for the test variable and the todo list. You can turn it off again with %(debug = 0). When you're done with it you can delete the zzz_todo.dic file from the master folder, just make sure you remove it in yaya.txt too.

If you need a place to host network updates, I've set up a tutorial on how you can do that with Github! https://zichqec.github.io/s-the-skeleton/github


I've included 3 Saoris with X. Template. Saoris are basically plugins you can add to your ghost with unique functions. The ones I've included are:
Gomi - Allows the ghost to interact with the recycle bin, seeing how many items are in it and emptying it.
CPUID - Gathers system information.
Time_Check - Does time based math, so you can check the time between two dates, for example.
If you want to read what we've learned about these saoris and how to use them, you can see it here https://docs.google.com/document/d/1EJSeEMGdN2eHSfWGyS-acG0DzfqpqEvMU-kYuGjbBtk/edit


Here are the resources I most recommend when making ghosts, I use these almost daily and they will save you so much headache.

http://umeici.onjn.jp/files/tama_v1p1.zip This is Tama, a debugging tool for AYA and YAYA. All you need to do is reload your ghost while Tama is running, and it will show you all kinds of information. If your ghost has errors upon startup, Tama can help you find them.

http://ssp.shillest.net/ukadoc/manual/list_shiori_event.html This is a list of Shiori events and what information they give you.

http://ssp.shillest.net/ukadoc/manual/list_sakura_script.html This is a list of sakurascript tags and what they do.

http://emily.shillest.net/ayaya/index.php? This is the YAYA wiki, where you can find more information about programming with YAYA. I'd come here if you're looking to do anything complicated.

https://drive.google.com/file/d/16JYyweRFNPhq-BzLQhPu5EPwG557hFto/view?usp=sharing This is a download for Coordin, a little program that can help you make simple collisions. Just drag and drop your surface onto it, then click and drag an area, and it'll copy the coordinates to your clipboard for you to paste right into surfaces.txt!

You can't go wrong with those resources on your side! If by some chance you are not a part of the Ukagaka Dream Team Discord Server, you can join us here. https://ukagakadreamteam.tumblr.com/discord
Having feedback from other people is incredibly helpful, and we're always glad to meet more ghost devs!



----------Notable Features----------

-A lot of small QoL tweaks, like offering to open a new ghost you've just installed, displaying email headers, offering a changelog after updating, and much more.
-Automatic update checks are built in, and will notify the user if an update is available.
-By default, double clicking on the face will pop up an 'are you sure' box if you've never hit the ghost before, to ensure the user doesn't accidentally punch the ghost.
-Mostly consistent code formatting, minimal comments unless it's a new feature that I wrote. Optimized for ghosts that have multiple modes, so that they're easier to add in.
-A kero is not present unless you choose to add them in.
-It can check for template updates, so that when you start a new ghost you can always be sure you have the latest version.



---Changelog---

-v1.1.3-
-Reworked the first boot sequence to patch a critical bug where the user would get stuck in passivemode. It no longer uses passivemode at all, so hopefully this will never be an issue again.


-v1.1.2-
-Fixed a critical typo in the reloading code that made the ghost never think it was reloading. Thanks Wormspawn for pointing it out!
-Updated YAYA to Tc567-1. This gives access to the all, last, and melt modifiers.
-As a result of the YAYA update, changed all the menus that were using --; syntax to have the all modifier instead.


-v1.1.1-

-Updated YAYA to Tc566-2. This gives access to the pool modifiers, and 64 bit integers!
-As a result of the YAYA update, the Pool function has been removed, RandomTalk has been given the nonoverlap_pool modifier, and the pools previously set up have been changed to if checks.
-Added auto anchor system. Now you can set up simple anchors a bit easier(?).
-Reworked the timekeeping system since I was not satisfied with it. The version built into the SHIORI resets every time you reload the ghost, and that annoys me, so I recreated the code and set it up to not reset when you reload.
-Updated the ghost changing functions so that the ghost should always be able to tell the difference between reloading itself vs changing to a ghost of the same name.
-Updated FormatLinks function; links in string.dic should now be written as alternating strings of names and urls.
-Removed OnUpdateCheckFailure function because it was no longer in use.
-Fixed some mojibake in string.dic.
-Changed pronouns to functions controlled by a single variable. This makes the code more concise and makes it so that pronouns will never show up blank.
-Added some information about the new version of the iolog commands in system_config.txt.
-Fixed an issue where the firstboot sequence could be interrupted by the ghost attempting an auto update, or the user petting the ghost.
-Fixed the name of the function OnOtherGhostVanished, so it should work properly now.
-Moved OnChoiceSelect out of yaya_shiori3.dic and placed it in anchor.dic instead.
-Removed a couple of other functions from yaya_shiori3.dic that were not default and were not in use. The shiori files of X. Template now match the default ones that you can download from github ( https://github.com/ponapalt/yaya-dic ). The AiTalk function in aitalk.dic has been changed to OnAiTalk to reflect this.
-Slightly improved the display of email headers, and increased the maximum default amount to 500.



-v1.1.0-

-Tweaked BalloonCheck function and fixed it.
-Updated the pool function to be simpler and more efficient.
-Changed the label of the dressup button back to default.
-Improved RemovePauses function (now erases more variants of quicksection tags, \_q tags, and \_w[] tags).
-Removed the bit in string.dic that fixed the 'calendar' typo, since it's been fixed in SSP now.
-Added center align tag to the config menu, and center and right align tags to the todo list!
-Added newline function to help with align tags.
-Removed OnUpdate.OnMD5CompareFailure event since my use of it was redundant.
-Revamped the code for the update progress bar.
-Added loremipsum function.
-Removed beta tester toggle since I never ended up using it like I meant to.
-Shuffled stuff around in the config menu a bit.
-Changed the formatting of the code in the menus. Maybe I'll change it back later, we'll see!
-Improved the readability of the system info and config menus by using anchors to highlight information.
-Added Sanitize function.
-Made name changing escape sakurascript tags.
-Changed ghostexlist to use C_BYTE1 as a delimiter.
-Added protection to email headers so that sakurascript tags cannot be executed from displaying headers.
-Shell scaling function can now check for Y scaling as well. nowscale has been updated to an array, where element 0 is the X scaling and element 1 is the Y scaling.
-Changed runtime array to a function rather than a variable. It will also reset if you reload the ghost now, because of the system it's using. No more clutter in OnSecondChange related to this, though!
-Removed non-interrupt system in the commu file, and replaced it with a new timerraise system where if the ghost can't talk, it will attempt to receive the communication a second time after 5 seconds. If that also fails, it will give up on it.
-Added dialogue for minimizing the ghost.
-Added Flag functions for easy flags.
-Removed system for moving shells to the same position when changing to them, since I don't think I'll make much use of this system in the future and it was causing some issues.
-Added OnOtherGhostVanished, so that you can now have different dialogues based on whether the ghost was open when another ghost was uninstalled or not.
-Added OnStatsRequested in commu.dic, a function for sending your ghost's stats to other ghosts who ask for them. The details of this will vary from ghost to ghost, but the structure is there now.
-Added X. Template Balloon, a simple and rough balloon that can be used as a template for a balloon if you want.


-v1.0.9-

-Updated to YAYA tc559-1.
-Added emergency mode files; if the ghost fails to load it will now direct you to the error log, where the current error should display. If there are too many errors, it won't be able to display them all! You can use Tama to see them all in that case.
-Overhauled the Todo list. The code is much cleaner now!
-Changed randomtalk to use Pools by default, instead of normal if checks.
-Updated wallpaper function; it can now accept files with brackets in the name, and if you're on windows 7 or 10 it will offer you the 'Fill' and 'Fit' options.
-Added SNTP option to the functions menu.
-Added an option in the config menu to turn off top of the hour notifications.
-Changed name teaching to use reference.raw, so that auto type convert doesn't mess with the user's input. Also made it cut out spaces on the left and right.
-Changed email headers to use reference.raw, so that getting the headers no longer requires a loop! It should be much better now.
-Added OnUserInputCancel in xt_etc.dic, to prevent the user from accidentally closing the input box in OnFirstBoot and locking themselves out of the ghost. Updated that whole system in general to work better.
-Moved Capitalize function to xt_anchor.dic, to make it more clear how it's meant to be used.
-Removed some of the extra documentation files; a lot of the concepts covered in them are now on my website, or eventually will be.
-Moved SAORIs and SAORI readmes into a saori folder, to keep things clean.
-Removed an unneccessary function in xt_string.dic, which would create a list of installed ghosts. Such a list already exists as a part of the normal system files.
-Fixed the pronoun variables not being initialized in OnFirstBoot.
-Fixed a few typos and missing tags.


-v1.0.8-

-Fixed an issue where auto updates were broken.
-Fixed a couple of incorrect links in the right click menu.
-Removed the booting variable, and replaced it with a system that checks for certain tags during the firstboot dialogues. Please let me know if you have any issues using this! This also means I've introduced the OnUserInputCancel function, which I stuck in etc.dic for now.
-Updated the OnOffscreen function, made it a little better and easier to understand.
-Added some new functionality to nowday and nowmonth; you can now send them integers to get days even further in the future/past. The randomtalk has an example of how this is used.


-v1.0.7-

-Added the Pool function for creating pools of dialogue with proper probabilities.
-Added the FormatLinks function and changed the links in string.dic to use a cleaner format.
-Added the br function, for balloon-specific manual linebreaks.
-Added a note about the LOGGING function in the test variable.
-Edited some documentation with new information.


-v1.0.6-

-Fixed the nowday function, it now correctly handles Sunday.


-v1.0.5-

-Fixed a terrible bug I added in 1.0.2, which prevented you from changing the talk rate or the pronouns... Turns out those brackets were necessary!
-Added a Commu Ping Menu. If the variable debug is set to 1, you can press C to get a nice window with the names of all the currently open ghosts in it. Click a name to send them a generic ping, or click the custom option to type in a custom message to send. Good for easily testing commu dialogues!
-Added a new hotkey: pressing Y will start a commu conversation with a random ghost, same as clicking the 'Talk to another ghost' option in the menu.
-Changed to the dedicated OnOffscreen function for offscreen dialogue, instead of using OnSecondChange. The format is a little more complicated, but now you can check if any character is off the screen, not just the sakura.
-Related, changed the name of MikireTalk and EndMikireTalk to OffscreenTalk and EndOffscreenTalk. Same functions, clearer labels.
-OnGhostChanging now checks to see if reference0 and sakuraname are the same, so you don't need to actually type your ghost's name in there at all.
-New function: leapyear. Is 1 if it's currently a leapyear, and 0 if it's not.
-When email checking fails because the user has their POP settings wrong, it opens the configuration dialogue to the POP page specifically.
-betaTester and nowscale variables are now properly initialized on first boot
-Got rid of the currentfile global variable. New system uses a local variable, and uses the SPLITPATH function to grab just the file name and extension instead of the whole path.
-Viewing headlines/RSS feeds will now display a choice marker in front of every item.
-Tweaked the format of the name change function and birthday teaching functions to better match the rest of X. Template.
-Added cancel buttons to the name change function and birthday teaching functions. These cancel buttons will activate a bit of code in the config menu, which closes the appropriate input boxes. If you were in the middle of changing your birthday, this also resets it back to what it was before you tried to change it.
-Updated surfaces.txt with some new info about SERIKO comments, and tweaked my comments appropriately.
-Fixed a missing surface call when there was an MD5 error during updates, and corrected an incorrect surface call in the SNTP functions.


-v1.0.4-

-Removed some testing stuff I left in commu.dic by mistake
-Uncommented some stuff that I had commented in aitalk.dic by mistake
-Added some clarification about nonoverlap in aitalk.dic


-v1.0.3-

-Fixed an incorrect variable name when updates finish. 'updateavailable' should be 'AutoUpdates[1]'
-Changed "'o clock" in the hour notifications to "o'clock"
-Added a better loop prevention system in commu dialogue
-Added a non-interrupt system in commu dialogue
-Slightly restructured things in OnSecondChange
-Checking for an update from the ghost's menu now actually starts an update, not just a check (sorry, I keep changing my mind lol)
-Changed the recommendations for UpdateVars, now it has a proper check to see if the variable exists
-Made a tweak to nowday and nowmonth. If you call them and include 'last' or 'next' as the second argument, you'll get the previous day/month or next day/month, respectively.
-Added the Capitalize function
-When done creating a .nar file, the ghost will give you a link to click that will open the folder you made the .nar in.


-v1.0.2-

-Fixed email checking again, I forgot to change the name of 1 variable and I'm very sorry for the trouble.
-Fixed the aitalkinterval being set to 6 minutes instead of 5 during the first boot, and adjusted a check in the config menu as well.
-Removed some unnecessary brackets in the config menu and some spots in etc, added in some semicolons instead.
-Made the RSS/Headline failure dialogue tell the user what error it got even if it isn't a recognized error.
-Added a note about OnSNTPFailure.
-Added a check for ] characters when setting wallpapers, as a ] in the file name will cause the wallpaper command to break. X. Template will now tell you that you need to remove any ]s from the file name first.


-v1.0.1-

-Fixed email checking, it should no longer spew headers all over the place before you've asked.
-Fixed the header code, it's much simpler, cleaner, and works properly now.
-Fixed an issue where the auto updates button wasn't appearing in the config menu.
-Changed some options in the config menu to display a 'Back to menu' and 'I'm done' button, instead of clicking the balloon to go back.
-Changed how new variables are added in updates, and removed that section from the 'Some YAYA tips' file since it's no longer relevant (new explanation is in Bootend because it's very short)
-Changed the URL that links to the template in the right click menu; it now correctly points to X. Template's page instead of the website's homepage.
-Changed wallpaper code so that it can see what OS you're running without needing the Saori, meaning that the span option should always appear if available.
-Changed the function that checks the template's version number, the changelog will now be displayed instantly.


-v1.0.0-

-Initial release