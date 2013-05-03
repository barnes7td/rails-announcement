#Sublime Tips \#3

This week we are going to discuss Setup and Customization. Most text editors you will use will have the ability to customize features and Sublime Text 2 is no different.


##User vs Default

An important concept when customizing Sublime Text is that most customizations have a User version and a Default version. The Default version is where all the application defaults are set. Each time you upgrade Sublime this file will get overwritten. Therefore, the User version of configuration file is the file that you change to set your specific settings. Even with an upgrade to the program this file will not be overwritten. From here on out all changes will be the User settings.


##User Settings

The "Packages/User/Preferences.sublime-settings" config file is where you will change the editors to your settings. You can open this file in Sublime through the menu or just locate the file. The file is just a json file that preferences can be typed into.

---

**Mac**

Menu  
=> Sublime Text 2   
=> Preferences   
=> Settings - Users

The package directory is located at:

```
~/Library/Application Support/Sublime Text 2
```

Copy and past this into the file:

```json
{
  "match_brackets_angle": true,
  "scroll_past_end": true,
  "tab_size": 2,
  "translate_tabs_to_spaces": true,
  "ensure_newline_at_eof_on_save": true,
  "save_on_focus_lost": true
}
```    

--- 

**Windows 7**

Menu  
=> Sublime Text 2   
=> Preferences   
=> Settings - Users

TThe package directory is located at:

```
C:\Users\<username>\AppData\Roaming\Sublime Text 2
```

Copy and past this into the file:

```json
{
  "default_line_ending": "unix",
  "match_brackets_angle": true,
  "scroll_past_end": true,
  "tab_size": 2,
  "translate_tabs_to_spaces": true,
  "ensure_newline_at_eof_on_save": true,
  "save_on_focus_lost": true
}
``` 

---

**Linux**

Menu  
=> Sublime Text 2   
=> Preferences   
=> Settings - Users

The package directory is located at:

```
~/.Sublime Text 2
```

Copy and past this into the file:

```json
{
  "match_brackets_angle": true,
  "scroll_past_end": true,
  "tab_size": 2,
  "translate_tabs_to_spaces": true,
  "ensure_newline_at_eof_on_save": true,
  "save_on_focus_lost": true
}
``` 
