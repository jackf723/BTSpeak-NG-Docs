## March 5, 2024 BT Speak® System Upgrade | Posted By: BT Development Team

It's time for another upgrade!  

### BT Speak® and BT Speak® Pro

* A new System Upgrade Notification monitor has been added It will manifest itself to you in two ways.
    * First, you'll hear a background announcement that "a new system upgrade is available" each time it detects that more changes have been posted. Since it runs on an intentionally somewhat randomized schedule from roughly once to twice per day, this announcement may occur when you aren't there to hear it.
    * You'll also hear an announcement that "a system upgrade is available", in between the "BTSpeak ready" and the "file is open" messages, each time you boot your BTSpeak if there are any changes that you haven't yet applied.
* When using the File Browser, each file's position in the listing of the current directory is now announced. For example, if you're currently on the third file of a listing that contains a hundred files then you'll hear the phrase "3 of 100" after it's name.
* A set of file listing filters has been added to the File Browser. The default filter is, of course, no filter. You can change the filter that's currently being applied by typing the letter F when using the File Browser. The filters that are currently provided are:
    * A: list audio files
    * B: list braille files
    * D: list directories
    * F: list all files
    * I: list image files
    * N: no filter (the default)
    * T: list text files
    * V: list video files
* Files can now be translated from one format to another. This can be done by typing the letter T from within either the File Browser or the File Management menu. If you do so from the latter then you'll be prompted for the file's name.
    * A file with any of these extensions can be translated:
        * .brf: Formatted Braille
        * .brl: Braille
        * .csv: Comma Separated Values
        * .docx: Word Document
        * .epub: Electronic Publication
        * .html: Hypertext Markup
        * .odt: Open Document
        * .txt: Plain Text
    * A file can be translated to any of the following formats:
        * B: Braille (.brl)
        * E: Electronic Publication (.epub)
        * H: Hypertext Markup (.html)
        * O: Open Document (.odt)
        * P: Portable Document (.pdf)
        * R: Rich Text (.rtf)
        * T: Plain Text (.txt)
        * W: Word Document (.docx)
* When the date is pasted, the name of the month, rather than its number, is now used. This has already been the case for a date when it's spoken.
* When a date is spoken or pasted, the order of its components (year, month, day) is now the one preferred by the current locale. For example, a user in the United States will hear the month before the day whereas a user located in the United Kingdom will hear the day before the month.
* BRF files, such as documents which have been downloaded from book providers, are now spoken properly by the editor. Rendering them used to sound more or less like gibberish. For the curious, this was because BRF files use the range of ASCII braille characters that add Dot7 to the base characters, and seeing Dot7 made no sense to the six-dot braille back-translator that we're using.
* Quoting of the file's name within the deletion confirmation prompt has been removed because DECtalk was speaking those quotes, thus making the actual file name rather difficult to understand.
* As DECtalk users will know all too well, the name of this very product - BTSpeak - wasn't being pronounced properly. As a general fix for this kind of problem, we've implemented a scheme that most modern text-to-speech engines are using, i.e. to consider an uppercase letter, even when it's in the middle of a word, to be the start of a new word. This is also referred to as “camel case.”
A set of word pronunciation dictionaries has also been added so that we can deal with words that text-to-speech engines get wrong. While the eventual goal is to make this user-configurable, for the time being we've hard-coded the use of the basic dictionary.
* DECtalk speech, when not set to the default rate, now sounds much more natural. This is because we're now using its new Samples per Frame feature rather then just setting the raw rate.
* The View Password Hint action has been added to the Device Customization menu. You are now asked for a hint regarding what your new password is when you change your password. When shipped, the hint is initially set to tell you what the default password is.
* When an important underlying host command failed, you were asked if you wanted to have a look at a log of that failure. The File Viewer is now used to present that log to you so that you can much more easily navigate your way through it. You'll now also be offered the opportunity to send a copy of that log to BT Speak Support.

### BT Speak® Pro

* The desktop's screen saver has been disabled so that you won't be unexpectedly prompted for your login password if Desktop mode has been idle for a few minutes.
* Starting Desktop mode no longer restarts the booting indicator (those regular vibrations that you feel while the BTSpeak is booting).
* Starting Desktop mode no longer makes it impossible to disable the keyboard while the BTSpeak is asleep.

## February 19, 2024 BT Speak® System Upgrade | Posted By: BT Development Team

We are pleased to announce another upgrade with the following new features and improvements:

### BT Speak® and BT Speak® Pro

* The editor now honors your key echo setting (controlled by E within the Speech Settings menu). It used to be that whenever you typed a character it'd always be spoken. Now, if you've turned key echo off, you'll no longer hear what you're typing. Note that word echo, i.e. the speaking of completed words, when in the editor is still not implemented. We'll be having a look at this as part of a future update.
* We have improved ER-Chord (i.e. 1-2-4-5-6-Chord) within the editor, which speaks the text from the cursor's current position through the end of the file. The five-second delay between lines has been removed. Pressing any key will interrupt the speech. While the underlying mechanism requires that cursor be moved as each line is enqueued for speaking, it's always returned to its original position afterwards. This happens quickly enough that you may not even notice the cursor motion.
* A booting indicator has been added. You'll feel a repeating short vibration, roughly once per second, while BT Speak® is booting. This is the same indicator that's already being used while a long action is being performed in other BT Speak utilities, such as System Upgrade.
* A Wi-Fi monitor has been added. You'll hear "Wi-Fi disconnected" when your connection drops, and you'll hear "Wi-Fi connected to [access point name]" when it's regained.
* The File Viewer has been enhanced. You'll now hear a rejection beep each time you type a character. 1-3-Chord and 4-6-Chord used to go to the beginning and end of the file - they now go to the beginning and end of the current line. 1-2-3-Chord and 4-5-6-Chord now go to the beginning and end of the file, respectively. These chord changes make the File Viewer consistent with how the editor uses them.
* Action confirmations, i.e. prompts that require you to answer either "yes" or "no", now clearly tell you what the default is, i.e. what'll happen if you just press Enter.
* The Rename action within the File Browser and File Manager no longer prefills the new name prompt with the old name, so that it could be edited.
* A new submenu of the System Menu, called About This Device has been added with the shortcut D. Rather than having to select each setting individually in order to check it, all of the settings are shown, within a single display, via the File Viewer. This means, among other things, that you can now navigate a setting's value by character in order to more accurately know exactly what it is.
* A Customize This Device submenu of the System Administration menu has been implemented with shortcut C. Among other options, this menu contains Change Owner's Name, allowing you assign your own name to BT Speak®. This will, for example, enable our Tech Support staff to more easily know who has sent us a log file. We recommend that you enter your first name followed by your last name and use normal capitalization (e.g. Deane Blazie).
* The Wi-Fi submenu of the Options menu (O-Chord) is now much simpler. In addition to just letting you add a new network, now also lets you switch to another network.
* BTRadio now synchronizes with your Pandora account, giving you access to its library of >800 music stations. If you already have a Pandora account, BTRadio will load your existing playlist. If you don't have a Pandora account, you can [sign-up for a free account.](https://www.pandora.com/account/register) If you are starting with a brand new Pandora account, your BTRadio playlist will initially be empty. Therefore, begin BTRadio using its Add Stations to PlayList option to build a playlist with your favorite music genres.

### BT Speak® Pro

Your BT Speak® Pro now includes Pidgin on its desktop! This application handles several instant messaging protocols. 

## January 28, 2024 BT Speak® System Upgrade | Posted By: BT Development Team

Today we released another software upgrade for BT Speak® and BT Speak® Pro! The upgrade is available for download from the System Administration Menu. To get there: from the options menu, navigate to System, select System Administration Menu, and choose Upgrade the System. This upgrade offers new features and performance improvements:

### BT Speak® and BT Speak® Pro

* System Services has been added to the Advanced System Administration menu.
    * It allows you to either enable or disable three services (so far). They are:
        * SSH (Secure Shell),
        * SMB (File Sharing)
        * NFS (Network File System).
    * They've been selected because each gives others remote access to your BT Speak® via the network. You have the option to manually disable whichever of them you'd rather not have running on your BT Speak®.
* We have introduced shortcuts within the Advanced System Administration menu. They are as follows:
    * The shortcut to invoke an interactive shell is now I. This aligns it with the same action within the Boot menu. It used to be S, which now enters the new System Services menu.
    * The shortcut to view open issues is now O. It used to be I, which now invokes an interactive shell.
* Enhanced technical support: After viewing a log file, you'll now be asked if you'd like to send a copy of it to BT Speak® Support. The default answer is "no", but, if you answer "yes", we'll receive it via email. This is a great way to get your technical support concerns addressed by our team. Also, you'll no longer need to find some way to retrieve your own copy of it.
* If your BT Speak® encounters a problem during system upgrade, you'll now be told exactly which step had the problem, if you'd like to send a copy of that step's log to BT Speak® Support, and an option to retry the upgrade.
* A symbolic link named "Public", which points to the "/Public/" directory, has been added to the home directory.
* Viewing a log file now uses the File Viewer. This means that you can now navigate around log file contents by word or character.
* Minor bug fixes and performance enhancements.

## January 13, 2024 BT Speak® System Upgrade | Posted By: BT Development Team

Earlier today, we released software upgrades for BT Speak® and BT Speak® Pro, which are available for download from the System Administration Menu.

### BT Speak® and BT Speak® Pro

* The Boot menu has been added. Get into it by holding the Power button while BT Speak® boots. It's main purpose is that you can boot into it when the normal user interface isn't working. From it, you can do things like perform a system upgrade, invoke an interactive shell, run hardware tests, switch to a low-level system maintenance shell, etc.
* The Where Am I command - WH-Chord (dots 1-5-6) - when invoked while in the editor now also tells you which file is open.
* When in the editor, 1-3-Chord and 4-6-Chord, which go to the beginning and end of the current line respectively, now speaks what the new current character is.
* Three new hot chords have been added that work everywhere.
    * D-8-Chord says the current date
    * T-8-Chord says the current time
    * ST-8-Chord (dots 3-4) says the current battery status. 
* Dates are now spoken using the weekday and month names in the format: weekday name, numeric day of the month, month name, and numeric year. So, for example, today's date is spoken as "Friday, 19 January, 2024". We intentionally separated the two numeric components (the day of the month, and the year) from one another in order to make each much more easy to hear.
* Selecting Date, Time, or Battery from the Options menu now speaks the corresponding value immediately. These actions no longer temporarily leave the editor in order to be performed.
* The Paste menu now allows you to paste the most recent calculator result, the most recent Gregorian date calculation, and the most recent Stopwatch reading.
* The Paste menu now pastes in braille when you're editing a .brl or a .brf (braille scripted) file.
* Introduced small bug fixes to the Battery Status and Power Status features

###BT Speak® Pro

Desktop mode - only available on Pro units - was designed and developed. If you're curious about how to use it, you can check out the Desktop Navigation and the Desktop Review help files.
