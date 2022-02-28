# Brandon Britton's App Review 2

## Intro

  The two apps that I will be reviewing are two gaming apps: **Dragalia Lost** and **Sdorica**. In this review, I will cover both game's uses of the following elements and compare them in how they are used. UI elements and Activities will be covered first, the use of RecyclerView and Activities in both apps, the Activity lifecycle of these apps, and then I will answer what changes I would make to the app if were to be a developer on it.
  
  _Please note, and I apologize in advance, that all my .gifs were limited to 5MB in size. As a result, quality between them may differ_

## UI Elements, Activities and Navigation

### Activity Navigation within a Constraint

**Dragalia Lost**
<p float="left">
  <img src="https://cdn.discordapp.com/attachments/910117718924099594/947867457148817418/Screen_Recording_20220227-202727_Dragalia_1.gif" width="400" />
  <img src="https://cdn.discordapp.com/attachments/910117718924099594/947939609915056188/Screenshot_20220228-110427_Dragalia.jpg" width="400" /> 
</p>

  In Dragalia Lost, there are many different UI layouts depending where you navigate within the game, but I will divide them broadly into two seperate categories: the UI within gameplay, and the UI within menus. In the two pictures above, we see that by tapping on the buttons marked (2), the center-constrained activity changes to the appropriate menu while retaining the upper (1) and lower (2) navigation bars. The second image depictes what the "Home" activity appears as, while the .gif image can be seen rotating through three different activities by tapping the corrosponding buttons on the bottom of the UI: Quests, Upgrade, and Teams.
  
<p float="left">
  <img src="https://cdn.discordapp.com/attachments/910117718924099594/947944351496036362/Screenshot_20220228-115215_Dragalia.jpg" width="400" />
</p>
    
    Just to be thorough, this is a screenshot of what the UI appears to be in-battle. It's thankfully less cluttered compared to what the primary main menu has become-- it features four skills at the bottom of the screen, a portrait for the two leading units on the bottom left, a list of buttons at the top-left showing the status of other teammates, a map and "auto" buttons at the top right (the latter of which is not always present). In regards to Activities, I believe the entire sequence of gameplay is regarded as a single activity-- a loading transistion does occur when changing maps, but I do not think this is a new activity since saving the all the states of the characters would be ineffecient. Instead, I speculate that the new scene is loaded the characters moved to a fixed location at the new area.

  I found this utilization of activities quite interesting, and it's more widespread that I originally imagined in use of games. Normally, I might have imagined that a change to an activity would have had a transistion where it appears the new activity "pops up", or has a transistion from the side of the screen 
  
  
  

REQUIREMENTS
Your analysis should compare and contrast your chosen apps in terms of their user interface (UI), especially relating to specific "views" (or what I've referred to as Activities in class), and to navigation, as well as the app lifecycle and especially the experience of starting, stopping and resuming use of the app. Your analysis should also continue to consider the same, or similar questions asked in the last app review assignment.
 
The following questions are prompts that are intended to get you thinking about the points above. You need not answer all of them (or even any of them, if you have other equivalent ideas). Think of them as starting points to help you develop your own questions as part of your analysis:
Consider specific and related UI elements in each of your chosen apps (e.g. menus in each of your apps, or data entry views, etc.): Does one app have a "better" interface than the other? Which do you think might be easier, or more challenging to implement?
The RecyclerView is a commonly used layout pattern in Android development; do either of your chosen apps make use of RecyclerView? Are there other layout patterns present in either or both apps that you have seen elsewhere? Do you think that one app makes better use of common layout patterns?
What is the user experience in starting each of your apps? What about stopping, or exiting? Is resuming easy and efficient? How do these experiences compare across both apps?
If you were a developer on one of your chosen apps, what is one change you'd like to make, or one feature you'd like to implement? Which of the two apps would you rather be a developer on? Why?
