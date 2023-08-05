- references
  collapsed:: true
	- [How to create a Logseq graph using existing Markdown files](https://docs.logseq.com/#/page/how%20to%20create%20a%20logseq%20graph%20using%20existing%20markdown%20files)
	  collapsed:: true
		- default folders where Logseq creates files
		- Logseq can find files anywhere, but it will create files in specific folders
	- [Logseq file and folder naming rules](https://docs.logseq.com/#/page/logseq%20file%20and%20folder%20naming%20rules)
	  collapsed:: true
		- don't use emojis - there is an icon page property for that
		- avoid spaces at end of filename
	- [Filename format](https://docs.logseq.com/#/page/filename%20format)
	  collapsed:: true
		- see functionality section, conversation details not necessarily important for new users
		- each page is a file
		- Logseq does conversions to avoid navigation problems caused by invalid characters in file names
		- I try to keep my file names simple
	- [Logseq Sync](https://docs.logseq.com/#/page/logseq%20sync)
	  collapsed:: true
		- paid feature in Beta
		- graph open on only one device at a time
		- sync up to 10 graphs
		- uses end-to-end encryption
		- files are stored on AWS
- how Logseq works with files
	- Logseq looks at all of the files in a folder and parses the markdown or orgmode files - it ignores the others unless they have links to them in Logseq
	- it creates a database in memory with all of the file information
	  collapsed:: true
		- the database is called [[Datascript]] and it is based on the [[Datalog]] database written in [[Clojure]]
		- this backend uses technologies similar to [[Roam]] and [[Tana]] but because those tools are not open-source we can't be sure
	- as you make changes to a block, it writes those changes to the files on your computer
	- so auto-save is constantly happening in the background
- how to sync files between devices
	- Logseq has a paid sync function
		- it encrypts the data and stores it in AWS
		- you can sync 10 graphs at most and each graph can only be open on one device at a time
	- you can use Git
		- Git works with files, so you can make your Logseq graph a Git repository and track changes there
		- I use that approach with this public graph
		- whenever I want to add something to the website, I just create a new commit and push it to GitHub
		- I use a Logseq GitHub action to update the published site
		- there is also an auto-commit feature built in to Logseq but I prefer to control when I make commits and what the message says so that I can understand what I was working on
		- Git can help you avoid data loss because it can restore previous states
		- you just need to remember to make commits at important times
	- you can use a file-syncing provider
		- I have had success using Microsoft OneDrive on both Windows and Mac
			- problems
			  collapsed:: true
				- Logseq will create extra files in these two folders
				  collapsed:: true
					- folders
						- `logseq\.recycle`
						- `logseq\bak`
					- Logseq ignores these files but doing a search outside of logseq will cause them to show up and can cause confusion if you are looking for something specific
					- occasionally I run a [[PowerShell]] script to delete those backup files
				- if there is a sync conflict, OneDrive will duplicate config files and append the machine name to the old file
				  collapsed:: true
					- Logseq automatically uses the new file, so this isn't a problem but it does generate unnecessary files
				- you can lose data sometimes if there is a sync issue
				  collapsed:: true
					- in that case the `bak` folder may have what you're looking for
				- there can be a mismatch between what Logseq sees on disk and in memory
				  collapsed:: true
					- usually I accept what is in memory
					- but sometimes I'll accept what is on disk if I've imported data into a file and am expecting Logseq to read the file and refresh the screen
			- tips
			  collapsed:: true
				- Logseq parses all of the files in a folder, so I set OneDrive to automatically download all the files in my Logseq folder to make sure Logseq can read everything that it needs to
		- iCloud does not work well
			- iCloud frequently creates sync conflicts and loses data
			- the approach that Apple takes to syncing happens to conflict with how Logseq works
			- iCloud could be useful to iOS on mobile because you need to keep application data in a specific folder, but in practice it doesn't work because of the sync conflicts
		- I have not tried other services like Dropbox