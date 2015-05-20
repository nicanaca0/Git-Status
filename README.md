--- Get Status ---
Ever wanted to get the status of repos in multiple sub directories? Yeah, me 
too. So I knocked this up.

-- Installation --
Copy the file to /usr/bin

%> cp show_status /usr/bin (or /usr/sbin)

Give it execute permissions

%> chmod +x /usr/bin/show_status

-- Usage --
Usage: show_status [options]

Show Status is awesome. If you tell it a directory to look in, it'll scan
through all the sub dirs looking for a .git directory. When it finds one it'll
look to see if there are any changes and let you know. It can also push and
pull to/from a remote location (like github.com) (but only if there are no
changes.) Contact mike@mikepearce.net for any support.

Options:
  -h, --help            show this help message and exit
  -d DIRNAME, --dir=DIRNAME
                        The directory to parse sub dirs from
  -v, --verbose         Show the full detail of git status
  -r REMOTE, --remote=REMOTE
                        Push to the master (remotename:branchname)
  -p PULL, --pull=PULL  Pull from the master (remotename:branchname)

[ forked notes: ]

I wanted to pretty print the statuses of git repos in a set of folders.
I found a nice script[0] which i put in /usr/local/bin along with this file
and then I set the directories I want to check the first-level sub folders
[0] https://github.com/MikePearce/Git-Status
Note: I comment out the os.system('clear') so I get all the folders on one screen


```bash	
cd /usr/local/bin
sudo ln -s ./path/to/GitStatus/show_status
sudo ln -s ./path/to/GitStatus/multi_show_status
```


-- Warranties/Guarantees --
None, you're on your own. If you'd like some help, mail me on mike@mikepearce.net
