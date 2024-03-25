## Editor Details Help

The BTSpeak's editor is based on nano - a popular, light-weight text editor.
Nano was chosen because it's stable, easy to learn, and has been tested and regularly updated for over 20 years.

The main reasons that we've modified nano are:
  * So that we have direct control over what's spoken as files are being reviewed and/or modified.
  * To keep the edit area on the screen blank so that the BTSpeak's own speech mechanism isn't accidentally triggered.
  * To disable line wrapping because, while a wrapped line fits on the screen nicely and looks well enough to a sighted user, one who uses speech much prefers that each line is always spoken in its entirety.
  * To include custom commands that are useful when working with braille documents.
  * To have a much simpler, speech-friendly, title bar.

The editor has a number of features that can be enabled/disabled (toggled) via some of its commands.
They are:
  * Always Show Cursor Position
    * This feature is toggled by Meta C.
    * We've disabled it by default.
  * Smart Home Key
    * This feature is toggled by Meta H.
    * We've enabled it by default.
  * Auto Indent
    * This feature is toggled by Meta I.
    * We've enabled it by default.
  * Cut from Cursor
    * This feature is toggled by Meta K.
    * We've disabled it by default.
  * Hard Wrapping (of over-long lines)
    * This feature is toggled by Meta L.
    * We've disabled it by default.
  * Mouse Support
    * This feature is toggled by Meta M.
    * We've disabled it by default.
  * Show Line Numbers
    * This feature is toggled by Meta N.
    * We've disabled it by default.
  * Convert Typed Tabs to Spaces
    * This feature is toggled by Meta O.
    * We've disabled it by default.
  * Show Whitespace
    * This feature is toggled by Meta P.
    * It's disabled by default.
  * Soft Wrapping (of over-long lines)
    * This feature is toggled by Meta S.
    * We've disabled it by default.
  * Color Syntax Highlighting
    * This feature is toggled by Meta Y.
    * It's enabled by default.

Most of the editor's key bindings are the same as nano's default ones.
The ones that we've changed are:
  * Control B: go back one word
             * (was go back one character)
  * Control F: go forward one word
             * (was go forward one character)
  * Control J: say the current character
             * (was justify the current paragraph)
  * Control N: go to the next anchor
             * (was go down one line)
  * Control P: go to the previous anchor
             * (was go up one line)
  * Control V: say the current word
             * (was go down one screenful)
  * Control Y: say the current line
             * (was go up one screenful)
  * Control Z: zap (discard) the current line (or marked region)
             * (was suspend the editor)
  * Meta X: place/remove an anchor at the current line
          * (was enable/disable show help summary below the status bar)
  * Meta Z: invoke the spell checker
          * (was enable/disable suspension)

