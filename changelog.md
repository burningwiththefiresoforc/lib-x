### Fixes 1.3
-A whole bunch more refactoring (thanks AI)

### Fixes 1.2
-Removed list enumeration which seemed to be causing some issues with jq  
-Fixed jq parsing errors due to some escaping issues and weird calibredb outputs  
-Added some functionality to leave the user categories menus cleanly  
-Some refactoring and more cleanup  

### Fixes 1.1
-Added escape key functionality to the rofi menus  
-Simplified menu structure  
-Fixed confirmation menus for rofi  
-Some cleanup  

### Fixes 1.0  

-Changed notifications from terminal notifications to notify-send for integration into dunst or other notification daemons. Removed NOTIFICATION_DURATION.  
-Fixed the rofi menu cutting off the exit option making it difficult to exit the menu loop  
-Added functionality for the rofi menu to pull up yazi or fzf with a terminal in a new option PREFERRED_TERMINAL when adding books. Default terminal is kitty. Not tested with other terminals.  
-Reordered some of the menu items  
-Made the icons more consistent  
-Spelling corrections  
-Disabled automatic update checking. 
