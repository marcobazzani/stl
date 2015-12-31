# stl
A tool that use diff rsync vim and colordiff to allow a fine graded control over 2 directory on 2 different system to be kept in sync

Requirements:

grep, ssh, colordiff, rsync, vim (invoked with vimdiff)

Install:

1. download and copy into ~/bin

 		2. sh -c ~/bin/stl

That's it

commands:

	stl (list all the files that has changes)

	stl-vim (for each of the differences a vimdiff will be performed) 

	stl-diff (colorized diff output)

	stl-check (is a basic rsync which show what will change)

	stl-sync (effectively sync)

        stl-check-full (same as stl-check but without skipping configured patterns)
        
        stl-sync-full (same as stl-sync but without skipping configured patterns)
        
examples:

show only different files

	stl . 192.168.4.2:/home/centos/installation-scripts/

execute vimdiff for each of the file which differs (you can also use dp (diff put) and do (diff obtain) to sync only part of a file

	stl-vim . 192.168.4.2:/home/centos/installation-scripts/

execute diff for each of the file that differs
	
	stl-diff . 192.168.4.2:/home/centos/installation-scripts/

list everything which will be rsynced

	stl-check . 192.168.4.2:/home/centos/installation-scripts/

do the real rsync

	stl-sync . 192.168.4.2:/home/centos/installation-scripts/


NOTE: trailing slash is relvant
