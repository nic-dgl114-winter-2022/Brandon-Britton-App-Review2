# Brandon Britton's App Review 2

## Intro

  The two apps that I will be reviewing are two gaming apps: **Dragalia Lost** and **Sdorica**. In this review, I will cover both game's uses of the following elements and compare them in how they are used. UI elements and Activities will be covered first, the use of RecyclerView and Activities in both apps, the Activity lifecycle of these apps, and then I will answer what changes I would make to the app if were to be a developer on it.
  
  _Please note, and I apologize in advance, that all my .gifs were limited to 5MB in size. As a result, quality between them may differ_

## UI Elements, Activities and Navigation

### Activity Navigation within a Constraint

**Dragalia Lost**
<p float="left">
  <img src="https://cdn.discordapp.com/attachments/910117718924099594/947867457148817418/Screen_Recording_20220227-202727_Dragalia_1.gif" width="400" />
  <img src="https://cdn.discordapp.com/attachments/910117718924099594/947939609915056188/Screenshot_20220228-110427_Dragalia.jpg" width="400" /></p>

  In Dragalia Lost, there are many different UI layouts depending where you navigate within the game, but I will divide them broadly into two seperate categories: the UI within gameplay, and the UI within menus. In the two pictures above, we see that by tapping on the buttons marked (2), the center-constrained activity changes to the appropriate menu while retaining the upper (1) and lower (2) navigation bars. The second image depictes what the "Home" activity appears as, while the .gif image can be seen rotating through three different activities by tapping the corrosponding buttons on the bottom of the UI: Quests, Upgrade, and Teams.
  
<p float="left">
  <img src="https://cdn.discordapp.com/attachments/910117718924099594/947944351496036362/Screenshot_20220228-115215_Dragalia.jpg" width="400" />
</p>
   
  Just to be thorough, this is a screenshot of what the UI appears as in-battle. It's thankfully less cluttered compared to what the primary main menu has become; it features four skills at the bottom of the screen, a portrait for the two leading units on the bottom left, a list of buttons at the top-left showing the status of other teammates, a map and "auto" buttons at the top right (the latter of which is not always present). In regards to Activities, I believe the entire sequence of gameplay is regarded as a single activity; a loading transistion does occur when changing maps, but I do not think this is a new activity since saving the all the states of the characters would be ineffecient. Instead, I speculate that the new scene is loaded the characters moved to a fixed location at the new area.


**Sdorica**
<p float="left"><img src="https://cdn.discordapp.com/attachments/910117718924099594/947867409707040778/Screen_Recording_20220227-204924_Sdorica_1.gif" width="500" /></p>

  In Sdorica, there are also a variety of UIs you may come across depending where you navigate throughout the game. Again, my primary focus will be where an Activity is present rather than where they are not. In Sdorica's horizontal layout, the primary UI can be seen by a header of information at the top, and on the right-hand side, five buttons that change an activity within a constraint on the screen. I believe this is where an Activity is present, as new information is loaded for each transistion to a different menu. Note how when a button is pressed, the UI persists, but the activity within the constrait changes through a transistion.
  
  Although I can't be sure, I will note that clicking on the "Journey" or "Roster" buttons leads to pages that require significant amounts of loading time when compared to the others (which is why I began the .gif on the "Journey" Activity)-- this is no doubt a result of the amount of information that they need to dipslay as a result, but it tells me that when navigating through these menus, the information for each of them is discarded each time they are navigated away from, which would suggest to me these are activities rather than a change in display. 
  
<p float="left"><img src="https://cdn.discordapp.com/attachments/910117718924099594/947950149282439188/20220228_121507.gif" width="500" /></p>

  Here, we see a navigation of the "Events" menu within the "Journey" Activity. I'm actually suspicious of this navigation being an activity or not, since it's so well optimized compared to the rest of the app. Much like the previous navigation examples, we have two primary "left" and "right" buttons that are at the top-right of the scene. Thinking more about it, I instead think this could be a RecyclerView within a RecyclerView, but more on that later.

  I found this utilization of activities quite interesting, and it's more widespread that I originally imagined in the use of games. Normally, I might have imagined that a change to an activity would have had a transistion where it appears the new activity "pops up", or has a transistion from the side of the screen, but I realized that a  new Activity may also have custom animations as you change from one to another. I also found the use of persisting UI elements overtop of Activities a clever and well designed use of a clean UI overall.
  
  ## Use of RecyclerView
  
  **Dragalia Lost**
  
  <p float="left"><img src="https://cdn.discordapp.com/attachments/910117718924099594/948082221967892480/20220228_210002.gif" width="250" />
<img src="https://cdn.discordapp.com/attachments/910117718924099594/947867445727748156/Screen_Recording_20220227-202954_Dragalia_1.gif" width="250" />
<img src="https://cdn.discordapp.com/attachments/910117718924099594/947936372285653073/20220228_112007.gif" width="250" /></p>
  
  Dragalia Lost actually has significant use of RecyclerView throughout its app. After having been introduced to the RecyclerView concept, I was surprised to discover it being used so frequently among the app. In all three of the above images, we can use of the RecyclerView in various constraints: as a horizontal view for story chapters, a vertical view for the event page, and a grid view for character icons, weapons, and other equipment. There are many other examples of RecyclerView throughout the entirety of Dragalia Lost, but here would be the three primary examples of its use horizontally, vertically, and as a grid.
  
  **Sdorica**
  <p float="left"><img src="https://cdn.discordapp.com/attachments/910117718924099594/947867402018914334/Screen_Recording_20220227-205153_Sdorica_1.gif" width="400" />
  <img src="https://cdn.discordapp.com/attachments/910117718924099594/948081265695924244/20220228_205607.gif" width="400" /></p>
  
  In these two Sdorica images (and the one in the prior category), we can see use of RecyclerView in both the main UI and within the character roster page. The first .gif is a demonstration of RecyclerView in a grid format, where the top row of characters' views are reused for every new row below (or above) them. In the second picture, I believe there are actually two RecyclerViews in use; one for the text tabs at the bottom, and one for the image above that matches the corrosponding text of the RecyclerView below it. You might say this can be accomplished as one view-- but there is a bug where you are able to desync the image of the above view so it does not match the correct view selection at the bottom. Since this bug exists, I am tempted to believe that this is two serperate RecyclerViews that may go out of sync with one another given some scenarios.
  
  It's difficult for me to say whether or not these apps makes better use of common layout patterns-- as I have become accustomed to navigating them effectively throughout the years. I can admit that Dragalia's UI is becoming increasingly crowded as more content is added, and can become difficult to navigate as a result. Meanwhile, Sdorica's UI has loading and optimization issues that can make navigation throughout the game sluggish. If it were simply about optimized navigation, then Dragalia definitely is the winner of these two apps.
  
  ## App Lifecycle
  
   **Dragalia Lost**
   
   <p float="left"><img src="https://cdn.discordapp.com/attachments/910117718924099594/947931612832759868/Screen_Recording_20220228-094410_Dragalia_1.gif" width="400" /></p>

  Dragalia's app lifecycle I believe is rather typical from what you'd expect from an android game. Although still too long to make a .gif out of, starting the app usually begins with a black screen with a white pixel in the middle, and later presents a title screen with splash art and theme music. A typical "Tap to Play" prompt is shown before loading the main UI menu.
  
  When stopping the app, Dragalia aims to do primarily one of two things, depending on whether or not you're in a battle or within menus. If you are within a menu, the game will preserve your location in the menu and any changes that may have been made or are currently in progress, such as team orginization. The other, more notable thing that Dragalia does is if you stop the app while currently in a stage or battle-- upon resuming the app, you will see that the game has automatically paused the game for you, and you will see the pause menu upon resuming the app, with all battle information paused at that current point in time.
  
  One other important detail to mention while stopping the app in co-operative play, is that while the pause menu is brought up, it neither pauses the battle gameplay for the player who has stopped the app, and additionally, it results in the immedieate disconnection of that player in co-operative play.
  
  **Sdorica**
  
  Sdorica on the other hand, has very little to write home about regarding the App Lifecycle in comparison. Like Dragalia, it has a typical startup and loading screen until a "Tap to Play" prompt is brought up to lead the user to the main UI. Also like Dragalia, it has typical behaviour when stopping, resuming, and destroying the app. The app lifecycle of Sdorica is comparative to Dragalia's, although it does not have the niches of co-operative play.
  
  Sdorica however, does resuming very poorly. When stopping the app, I suspect it tries to store too much data when trying to resume-- especially when you swap to a different app and return to it after even a short period of time. Sdorica more often than not has a higher failure rate of onRestart -ing the app over success, and while it clearly is not the intent, putting Sdorica onStop often leads to destroying the current instance of the app. I suspect this may be because of the amount of unnessecary information it tries to save into its state, but I cannot be sure.
  
  ## Closing Thoughts
  
  Both Dragalia and Sdorica have common use of Activities, RecyclerView, and neither had use of implicit intent to open pages in other apps, such as browsers (Instead, they both had in-game pages that mimicked the use of a webpage). In regards to design, it's difficult for me to say if one's interface is better than the other, as both have advantages and disadvantages in how their content is laid out. I will say however, that due to Dragalia's better optimization and loading times, it wins out on the better implemented UI. Due to the variety and complex uses of Activities and RecyclerVies in both apps, I would argue they are both difficult to implement, with lots of time spent on each of them.
  
  If I were to be a developer on one of these apps, then a change I would like to make to Sdorica's code is to simply better optimize it. It **needs** to have better loading times, have better version control on a wider variety of devices, and better bug and error reporting. "Object reference not found" is a app-destorying bug that has appeared on several occasions across a variety of devices. 
  
  Meanwhile in Dragalia, bug testing and device support is of exceptional quality. It's difficult to say how one might improve on the UI, but the difficulty of managing so much additional content on an increasingly cluttered menu is certainly a point of concern; I'm not quite sure I'd address this immedietely. Recently, there has been a crash that causes the app to close on the first attempt of a co-operative match per day, with acknowledgment that the issue is being worked on.
  
  It's difficult to say which of these two apps I'd rather be a developer on if I were given the choice. There would have been points in time where I would have certainly picked one over the other, both only because I have a fond affinity for these games-- I'd like to be a part of their development no matter the difficulties I come across in either of them. I would be proud to be a part of their development, and no reason more.

**_fin_**
