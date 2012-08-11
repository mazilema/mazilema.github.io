---
layout: page
title: "How to rename your home directory in OS X"
categories: 
- OS X
date: 2012-08-10 19:17
comments: true
sharing: true
footer: true
---
I tried to install RVM on my machine to set up [octopress](http://octopress.org) and ended up with an error (again) because my home directory name has  a space in it. This happend when I restored my account from Timemachine and just renaming the home directory did not work. So now it was time to repair this oddness.  

<!-- more -->

## Let's start with the easy part:

### OS X Mountain Lion: Enable and disable the root user 

* Choose Apple menu > System Preferences, and then click Users & Groups.
* Click the lock icon to unlock it, and then type an administrator name and password.
* In the Network Account Server section, click Join or Edit.
* Click Open Directory Utility.
* Click the lock icon to unlock it, and then enter your administrator name and password.
* Choose Edit > Enable Root User, and then enter a root user password in the Password and Verify fields.

Be sure to specify a secure password.

[Source: http://support.apple.com/kb/PH11331](http://support.apple.com/kb/PH11331)

## Now it's time to get dirty:

I had to go through this step twice as my short name was already "mazilema" but my home directory was "mazilema 1". So I renamed it to "mazilemas" and set up the corresponding user because the system does not  allow you to use a existing one. In the second run I then set "mazilema" as short name and home directory name.

I suppose there is a easier way with just renaming the home directory and some re-configuration. I would appreciate any hint on this for the next time.

### OS X: How to change user account name or home directory name 

For Mac OS X v10.5 or later

1. Enable the root user.
2. Log in as root.
3. Navigate to the /Users folder.
4. Select the Home folder with the short name you want to change, and rename it just like you would rename any folder. Keep in mind that the shortname must be all lowercase, with no spaces, and only contain letters.
5. Use the Users & Groups pane (Accounts pane in Mac OS X v10.6.8 or earlier) in System Preferences to create a new user with the Account name or Short Name that you used in the previous step.  
Note: As root, my keyboard layout switched to english so be carfeul when you set your password.
6. Click OK when "A folder in the Users folder already has the name 'account name'. Would you like to use that folder as the Home folder for this user account?" appears. Note: This will correct the ownership of all files in the Home folder, and avoid permissions issues with the contents. 
7. Choose Log Out from the Apple menu.
8. Log in as the newly created user. You should be able to access all of your original files (on the desktop, in Documents, and in the other folders of this Home).
Note: If you chose a different password, you will be promted how to handle your keychain.
9. After verifying that your data is as expected, you can delete the original user account via the Users & Groups pane (Accounts pane in Mac OS X v10.6.8 or earlier).
Note: You will have to reconfigure some applications like Dropbox, Steam, 1Password as the path changed.. You may also run into trouble with Skype and high cpu usage. In this case you may try: Close Skype. Delete or rename "~/Library/Caches/com.skype.skype". Reopen Skype. [Source:](http://community.skype.com/t5/Mac/Skype-heat-fan-high-cpu-usage-issues-in-Lion-OSX/td-p/41264/page/2)
10. Disable the root user.

[Source: http://support.apple.com/kb/HT1428](http://support.apple.com/kb/HT1428)