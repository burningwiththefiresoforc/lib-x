### Fixes 1.8.1
-Fixed some more minor breakages that I caused including --search and --sort-by functionality for the command line options.  

### Fixes 1.8
-Languages are now loaded in the menu as their ISO codes. A slight compromise but the menu is much, much faster now.  
-Categories are now populated entirely by the master TSV, save for one call to the csv at startup that defines the categories that are actually present. The CSV cache itself is now deprecated. Parsing is much faster, you would need a pretty large library to slow this down significantly. Tested on a library of ~600 books, near instantaneous on a 15 year old laptop.  
-Cleaned up some remnants of old features. There are now only two cached files, the books_path for adding books, and the master TSV. Database is refreshed either manually or at startup.  
-Removed some user managed lists that seemed a bit redundant.  
-More refactoring and merged a couple functions, offloaded some more stuff onto startup rather than repeated calls.  

### Fixes 1.7.1
-Expanded the TSV solution to allow for quick lookups for categories. It is much faster and less resource intensive. The exception to this is the Languages category, which is currently broken due to calibredb list_categories outputting the full language name while calibredb list outputs the ISO-639-2/T language codes, which are difficult to parse from the names any single language has for any other language (French -> fra, German -> deu, etc.). There is also some trouble parsing complex language names ("Greek, Ancient (to 1453)" causes some trouble). I have to think on it for a bit, this one might just have to use the slower calibredb/jq solution previously implemented or, best of all, a solution that cuts out the need for the calibre_categories.csv entirely, which exists now only to construct the category menus.  
-The use of the TSV will also allow in the future for me to easily include its relevant category metadata along with the title which will make it searchable.  
-Book comments are now a little bit prettier.  

### Fixes 1.7
-Heavily optimized preview image and metadata loading for fzf. Instead of everything being on demand it creates a TSV cache of the metadata, much less I/O and overhead, just slightly more loadtime on startup or reload. Also loads the lists faster. This also deprecated the need for a persistent JSON cache. Should work a little bit better with bigger libraries (tested on a library of about 600 books with lots of weird metadata).  
-Trying to work out a method to do the same for the calibredb categories lists like Authors, Formats, etc. which load very slowly but it's a bit more dynamic and harder to cache without making like eight separate caches or one massive one.  
-Other miscellaneous refactors  
-Broke some command line functionality. Might get around to fixing it, who knows.  
-Note to self need to sanitize the book comments of stray HTML tags  
-Code is basically impossible to read now and I have no idea what it does 🎉  

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
