## Network File Sharing Help

It's possible to share files with (transfer files to/from) the BTSpeak over the network.
This is done via the SMB (Server Message Block) or NFS (Network File System) protocol.
SMB works on many platforms (e.g. Windows, Linux).
NFS might work on other platforms but is primarily used between Linux systems.

In the examples below, we'll assume that the host name of your BTSpeak is btspeak50.
When using any of them, remember to use your BTSpeak's actual name instead.
To find out your BTSpeak's host name, do the following:
  1. Use O-Chord to go to the Options menu.
  1. Select the System menu (shortcut is s).
  1. Select About This Device (shortcut is d).
  1. Look for Host Name.

The first thing you need to do is to ensure that the /Public directory on your BTSpeak has been created.
This is the location to/from which you'll be transferring files.
This only needs to be done once, but, if you aren't sure, it won't hurt to do it again.
  1. Use O-Chord to go to the Options menu.
  1. Select the System menu (shortcut is s).
  1. Select the System Administration menu (shortcut is s).
  1. Select the Advanced System Administration menu (shortcut is a).
  1. Select the System Maintenance menu (shortcut is m).
  1. Select Make Third Partition (shortcut is 3).

### Accessing your BTSpeak from Windows

To access your BTSpeak from Windows, you'll need to first ensure that your Windows computer is allowed to use the SMB 1.0 protocol (it's disabled by default).
To do this:
  1. Press Windows+R, and type control.
  1. Select "Programs and Features".
  1. Select "Turn Windows features on and off".
  1. Go down to "SMB 1.0".
  1. If it's disabled then enable it and reboot.

Now, to access folders on your BTSpeak from your Windows computer, go into the "File Explorer"
and either click on "Network" (in the pane on the left) or tab over to "Home", type "Network", and press Enter.
You'll then see a screen listing all of the computers on your network; double-click on your BTSpeak.
A screen will come up asking you to enter the credentials for connecting to it.
It wants a username and a password default username is "pi", default password is "blz-tech".
You'll now see a screen that lists two folders: "pi" (your home folder), and "Public".
If you right-click on a file while browsing either of these folders, you'll be able to share it, email it, download it, or copy it.
If you don't see your BTSpeak's "Public" folder then it might not have been created yet - see above for how to do that.

### To use SMB on Linux:

In the GUI's file browser, click on Other Locations.
At the bottom of that screen is a place to enter the server name.
Depending on which DHCP server you're using, you may need to enter:
   either "smb://btspeak50/pi"
   or "smb://btspeak50.local/pi"
It'll ask for the user's name and password - enter "pi" and its password.

You can manually mount your BTSpeak's public volume from the Linux command line.
You'll need to first create a directory to be its mountpoint.
While this directory can be anywhere, it's usually created under the /mnt directory.
Let's assume that the mountpoint is "/mnt/btspeak".
These commands will mount your BTSpeak's public volume:
   mkdir /mnt/btspeak
   mount -t cifs -o username=pi,password=whatever //btspeak50/Public /mnt/btspeak
If you don't specify the user's name then it'll get it from the $USER environment variable.
This is usually the user that you're currently logged in as.
If you don't specify the password then it'll get it from the $PASSWD environment variable.
If $PASSWD isn't set then it'll prompt for the password.

If you'd like your BTSpeak's public volume to be mounted automatically each time you reboot your system
then add this line to your system's "/etc/fstab" file:
  //btspeak50/Public /mnt/btspeak cifs username=pi,password=whatever 0 0

In both of these cases (manual or automatic mounting), it's a bad idea to put a password in a public place.
Rather than using the username= and password= mount options, therefore, you should use the credentials= mount option instead.
It takes the absolute path to a file as its operand.
That file should, of course, be adequately protected from public scrutiny.
It's format is:
  username=pi
  password=whatever

