## Menu File Help

Menu files have the ".menu" extension and are in the "/BTSpeak/Menus/" directory.  
Blank lines are ignored.  
If the first non-space character on a line is # then that line is a comment and is ignored.  
The rest of the lines are item definitions, except for the first one which is the menu's title.

An item definition has the following general format ([brackets] means optional):
  [shortcut=]label [#comment]: action [argument ...]

The label is what's displayed on the screen.
If it contains a # then the rest of the text is a comment and is rendered within parentheses.

The shortcut for an item defaults to the first character of its label (case doesn't matter).
This can be overridden by adding the optional shortcut= prefix (where shortcut is a single character).
Explicitly specifying the shortcut is necessary when two or more labels start with the same character.
The cursor is placed on the shortcut of the currently selected menu item so that 3-6-Chord will say what it is.
If there's no shortcut then the cursor is placed on a space.

The following actions are supported:
* menu name
    * The "menu" action enters the named menu recursively.
    * Leaving it returns to the current menu.
* run command [argument ...]
    * The "run" action executes the specified host command and waits for it to finish.
    * You won't see its standard error while it's executing.
    * If it finishes with a nonzero exit status then you'll be asked if you'd like to view the errors.
    * The default response to this prompt is "no".
* execute command [argument ...]
    * The "execute" action executes the specified host command and waits for it to finish.
    * Standard error isn't intercepted.
    * This action must be used for host commands that are interactive, e.g. for shells and editors.
* exit
    * The "exit" action forces all of the active menus to be immediately exited.


