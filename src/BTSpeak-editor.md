## BTSpeak Editor Help

Both the File Management menu *(O-Chord M)* and the File Browser *(O-Chord F)* provide these file editing functions:
  * O: open an existing file (prompts for name)
  * C: create a new file (prompts for name)
  * S: save the current file without leaving it
  * L: leave the current file after saving any changes
  * Q: quit the current file without saving any changes

Another way to open an existing file is to press Enter when on it in the File Browser.

The editor's screen has three regions:
  * A title bar on the top line; T-Chord navigates to it.
  * A status bar on the bottom line; 3-4-Chord (s t) navigates to it.
  * An edit area in the middle; E-Chord navigates to it.

From left to right, the title bar contains:
  * Either the word "editing" (you can make changes) or the word "viewing" (you can't make changes) to the file.
  * The name of (not the full path to) the file.
  * The word "restricted" if the editor is in its restricted mode.
  * The phrase "mark set" if the mark has been set.
  * The phrase "unsaved changes" if you've made at least one change to the file.

The edit area is kept blank so that the BTSpeak's own speech mechanism won't be accidentally triggered.
This is done so that the editor can always be in full control of what gets spoken.

The status bar is spoken whenever its content changes.
It's used to display information, warnings, errors, and alerts.
If there's more than one message to be displayed at the same time then the most important one is chosen.

The editor has three menus (each of which has its own help file):
  * D-Chord: the Delete menu
  * N-Chord: the Navigation menu
  * P-Chord: the Paste menu

An editor command is bound to either a Control character or to a Meta character.
[{control-characters}]
[{meta-characters}]

These chords provide easier and more intuitive ways to perform useful editing functions.
  * 3-4-5-6-Chord (number sign): toggle the showing of line numbers (editor command is Meta N)
  * 8-Chord: type a "newline" character (editor command is Control M)
  * 7-Chord: delete the character to the left of the cursor (editor command is Control H)
  * 2-5-6-Chord (low d): delete the character that the cursor is on (editor command is Control D)
  * 1-4-Chord: say the current line (editor command is Control Y)
  * 2-5-Chord: say the current word (editor command is Control V)
  * 3-6-Chord: say the current character (editor command is Control J)
  * 1-Chord: go to the previous line (editor command is Arrow-Up)
  * 4-Chord: go to the next line (editor command is Arrow-Down)
  * 2-Chord: go to the previous word (editor command is Control B)
  * 5-Chord: go to the next word (editor command is Control F)
  * 3-Chord: go to the previous character (editor command is Arrow-Left)
  * 6-Chord: go to the next character (editor command is Arrow-Right)
  * 1-3-Chord: go to the first character of the current line (editor command is Control A)
  * 4-6-Chord: go to the last character of the current line (editor command is Control E)
  * 1-2-3-Chord: go to the first line of the file (editor command is Meta Backslash)
  * 4-5-6-Chord: go to the last line of the file (editor command is Meta Slash)
  * 2-3-Chord: go to the beginning of the previous (or current) block of text (editor command is Meta 7)
  * 5-6-Chord: go to the beginning of the next block of text (editor command is Meta 8)
  * G-Chord: Place/remove an anchor (editor command is Meta X)
  * 1-2-7-Chord: go to the previous anchor (editor command is Control P)
  * 4-5-8-Chord: go to the next anchor (editor command is Control N)
  * 1-3-7-Chord: go to the beginning of the current (or previous) paragraph (editor command is Meta Left Parenthesis)
  * 4-6-8-Chord: go to the end of the current (or next) paragraph (editor command is Meta Right Parenthesis)
  * 2-3-7-Chord: switch to the previous open file (editor command is Meta Less Than)
  * 5-6-8-Chord: switch to the next open file (editor command is Meta Greater Than)
  * F-Chord (prompts for text): find forward (editor command is Control W)
  * F-7-8-Chord (prompts for text): find backward (editor command is Control Q)
  * F-7-Chord: find previous (editor command is Meta Q)
  * F-8-Chord: find next (editor command is Meta W)
  * M-Chord: set/remove the mark (editor command is Meta A)
  * 1-2-6-Chord: copy to the clipboard (editor command is Meta 6)
  * 3-4-6-Chord: paste from the clipboard (editor command is Control U)

Cutting and copying to, and pasting from, the clipboard can also be performed via the Delete menu (D-chord).
These operations use the "from to" (rather than the "from through") paradigm, i.e. they're exclusive rather than inclusive.
This means that the first character is included but that the last character isn't.
If the cursor is before the mark then the marked character isn't included.
If the cursor is after the mark then the character under the cursor isn't included.

Clipboard commands have also been defined for those who are accustomed to using the traditional Control- X, C, and V conventions.
These are formed by adding 8-Chord to the letter. So:
  * M-8-Chord: set the mark
  * X-8-Chord: cut to the clipboard
  * C-8-Chord: copy to the clipboard
  * V-8-Chord: paste from the clipboard

The full list of the editor's commands is:
  * Enter: insert a newline at the cursor's position
  * Tab: insert a tab at the cursor's position
  * Arrow Left: go back one character
  * Arrow Right: go forward one character
  * Arrow Up: go up one line
  * Arrow Down: go down one line
  * Page Up: go up one screenful
  * Page Down: go down one screenful
  * Home: go to the beginning of the current line
  * End: go to the end of the current line
  * Insert: paste another file into the current (or a new) file
  * Delete: delete the character that the cursor is on
  * Backspace: delete the character to the left of the cursor
  * Control A: go to the beginning of the current line
  * Control B: go back one word
  * Control C: show the cursor's position
  * Control D: delete the character under the cursor
  * Control E: go to the end of the current line
  * Control F: go forward one word
  * Control G: display help (Control X to exit)
  * Control H: delete the character to the left of the cursor
  * Control I: insert a tab at the cursor's position
  * Control J: say the current character
  * Control K: cut the current line (or marked region)
  * Control L: refresh (redraw) the screen
  * Control M: insert a newline at the cursor's position
  * Control N: go to the next anchor (wraps from last to first)
  * Control O: save the current file (or marked region)
  * Control O twice: quit the current file without saving changes
  * Control P: go to the previous anchor (wraps from first to last)
  * Control Q: search backward for a string (or regular expression)
  * Control R: paste another file into the current (or a new) file
  * Control S: save the current file without leaving it
  * Control T: insert the output of an editor function or an external command into the current (or a new) file
  * Control U: paste the clipboard at the cursor's position
  * Control V: say the current word
  * Control W: search forward for a string (or regular expression)
  * Control X: close the current file (or exit the editor)
  * Control Y: say the current line
  * Control Z: zap (discard) the current line (or marked region)
  * Control Right Bracket: try to complete the current word

  * Meta A: set the mark at the cursor's position
  * Meta B: invoke the linter
  * Meta C: enable/disable always show cursor position
  * Meta D: count the number of words, lines, and characters
  * Meta E: redo the last undone operation
  * Meta F: invoke the formatter
  * Meta G: go to the specified line and column (prompts for line,column numbers)
  * Meta H: enable/disable smart home key
  * Meta I: enable/disable auto indent
  * Meta J: justify the entire file
  * Meta K: enable/disable cut from cursor
  * Meta L: enable/disable hard wrapping of over-long lines
  * Meta M: enable/disable mouse support
  * Meta N: enable/disable show line numbers
  * Meta O: enable/disable convert typed tabs to spaces
  * Meta P: enable/disable show whitespace
  * Meta Q: search backward for the next occurrence
  * Meta R: replace a string (or regular expression)
  * Meta S: enable/disable soft wrapping of over-long lines
  * Meta T: cut from the cursor's position to the end of the file
  * Meta U: undo the last operation
  * Meta V: insert the next keystroke verbatim
  * Meta W: search forward for next occurrence
  * Meta X: place/remove an anchor at the current line
  * Meta Y: enable/disable color syntax highlighting
  * Meta Z: invoke the spell checker
  * Meta 1: delete backward to the start of the current word
  * Meta 2: delete forward to the start of the next word
  * Meta 3: comment/uncomment the current line (or marked lines)
  * Meta 6: copy the current line (or marked region)
  * Meta 7: go to the beginning of the current (or previous) block of text
  * Meta 8: go to the beginning of the next block of text
  * Meta Left Parenthesis: go to the beginning of the current (or previous) paragraph
  * Meta Right Parenthesis: go to the end of the current (or next) paragraph
  * Meta Equal: scroll the line with the cursor to the middle of the screen
  * Meta Plus: scroll down one line
  * Meta Minus: scroll up one line
  * Meta Less Than: switch to the previous open file
  * Meta Greater Than: switch to the next open file
  * Meta Left Brace: unindent the current line (or marked lines)
  * Meta Right Brace: indent the current line (or marked lines)
  * Meta Right Bracket: go forward/backward to the matching bracket
  * Meta Backslash: go to the first line of the file
  * Meta Slash: go to the last line of the file
  * Meta Colon: start/stop recording a macro
  * Meta Semicolon: run the last recorded macro
