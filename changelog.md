### Fixes 1.6
-Fixed Add Book and Add Books From Folder (which I broke)  
-Minor bug fixes  
-Random optimizations  

### Fixes 1.5
-Any dreams of POSIX compliance are long dead  
-Much fewer lines of code  
-Quite a bit snappier now  
-Removed automatic update functionality entirely.

### Fixes 1.4
-Added option "Open Book Folder"  
-Optimizations

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
