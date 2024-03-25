## File Management Help

There are two ways to perform file management -
via the File Browser or via the Manage Files menu.
Both methods are in the Options menu *(O-Chord)*.
*Z-Chord* exits both.

Both methods offer these choices:
  * C: create a new file (prompts for name)
  * D: delete a file or directory (prompts for confirmation)
  * G: go to a specific directory (prompts for name, forces browser)
  * H: show hidden files (toggle)
  * L: leave the current file after saving any changes
  * N: create a new directory (prompts for name)
  * O: open an existing file (prompts for name)
  * P: protect a file or directory (make it read-only)
  * Q: quit the current file without saving changes
  * R: rename a file or directory (prompts for new name)
  * S: save the current file without leaving it
  * U: unprotect a file or directory (make it read-write)
  * W: which directory

The File Browser offers this additional choice:
  * M: switch to the File Management menu

The Manage Files menu offers this additional choice:
  * F: switch to the File Browser

### menu-navigation

If you are in the browser and need a reminder on the available file management shortcuts,
type *M* to switch to the menu, explore the options, and type *F* to switch back to the browser.

If an action prompts for confirmation, you can type one of these responses:
  * yes: Y
  * no: N
  * repeat the question: R

If you enter anything else then you'll be reminded of these choices.
*Z-Chord* cancels the prompt - it's equivalent to answering no.

When renaming, the new name response is pre-filled with the old name so that it can be easily edited.
To clear this initial value, type *X-Chord, A* (to move to the beginning),
followed by *X-Chord, K* (to delete from the cursor to the end).

The file browser shows a list of the contents (files, subdirectories, etc) of the current directory.
These keys can be used to navigate the list:
  * select first item: 1-2-3-Chord
  * select last item: 4-5-6-Chord
  * select previous item (wraps from first to last): 1-Chord or Backspace
  * select next item (wraps from last to first): 4-Chord or Space
  * go to parent directory: 3-Chord
  * go to selected directory: 6-Chord
  * open selected file or go to selected directory: Enter

If you are within the home directory's hierarchy then *Dot 3-Chord* (go to parent directory),
as a safety constraint, won't allow you to browse above the home directory itself.
You can, however, use *g* (go to directory) to bypass this constraint.

