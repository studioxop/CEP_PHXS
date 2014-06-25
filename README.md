CEP_PHXS
========

Sample script HTML configurator like panel 

put the com.example.testbld3 folder in one or more of the following folders:

    All users, Win: C:\Program Files\Common Files\Adobe\CEP\extensions
    All users, Mac: /Library/Application Support/Adobe/CEP/extensions
    Per user, Win: C:\<username>\AppData\Roaming\Adobe\CEP\extensions
    Per user, Mac: ~/Library/Application Support/Adobe/CEP/extensions

For an unsigned panel to work on your system, you have to set a debug flag (do it once and will be ok)

    WIN: regedit > HKEY_CURRENT_USER/Software/Adobe/CSXS.5
    MAC: /Users/<username>/Library/Preferences/com.adobe.CSXS.5.plist 

Add a new entry PlayerDebugMode of type "string" with the value of "1". This enables debug extensions to be displayed in the host applications.

Special notes for Mac 10.9 - Starting with Mac 10.9, Apple introduced a caching mechanism for plist files. Your modifications to plist files does not take effect until the cache gets updated (on a periodic basis, you cannot know exactly when the update will happen). To make sure your modifications take effect, there are two methods.

Kill cfprefsd process. It will restart automatically. Then the update takes effect.

Restart your Mac, or log out the current user and re-log in. 
