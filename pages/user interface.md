- references
  collapsed:: true
	- [Getting started with the Journals page](https://docs.logseq.com/#/page/getting%20started%20with%20the%20journals%20page)
	  collapsed:: true
		- a journal page automatically gets created each day
		- the journal page has linked references
	- [How to work with the right-hand sidebar](https://docs.logseq.com/#/page/how%20to%20work%20with%20the%20right-hand%20sidebar)
	  collapsed:: true
		- any internal link can be opened in the right sidebar
		- you can use it to
			- reference information on other pages while working in the center panel
			- drag blocks between pages - will discuss later
	- [What is indentation and why does it matter?](https://docs.logseq.com/#/page/what%20is%20indentation%20and%20why%20does%20it%20matter%3F)
	  collapsed:: true
		- how to think about parent-child relationships
		- importance of hierarchy in linked reference section
	- [Whiteboards overview](https://docs.logseq.com/#/page/whiteboard)
	  collapsed:: true
		- interesting use of [[namespace]] feature here
- Logseq has 3 main UI sections
  collapsed:: true
	- a left sidebar that lets you
		- navigate to different functionality
		- view favorite pages
		- view recent pages
	- a center panel that either shows a list of journal pages or one specific page at a time
	- a right sidebar where you can potentially view multiple pages stacked on top of each other
		- you open a page in the right sidebar by shift-clicking its title
		- you can open individual blocks by shift-clicking the bullet
	- I sometimes collapse the sidebars depending on what other applications I'm working with
		- a common situation is for me to collapse the right sidebar and take notes on an application to the right of Logseq
		- I've set up [[keyboard shortcuts]] for collapsing panels that are the same for other applications like [[VS Code]] and [[Obsidian]]
- Logseq is made up of bullet points called blocks
  collapsed:: true
	- the bullet icon indicates whether there are hidden nodes beneath them
	- you use the `shift` and `shift tab` [[keyboard shortcuts]] to control which blocks are parents of others
	- this hierarchical relationship is important for easily linking notes because any block with a link will show all the parent blocks above it
	  collapsed:: true
		- this design helps you see the context of why an entity was linked on another page
		- this is actually a powerful feature that makes the outline more useful - you just need to be thoughtful into how you structure the outline to get the info you're looking for
	- you can right-click a bullet icon to see menu items associated with the
	- in markdown these bullets are represented by a dash
	- this structure can make long-form writing difficult in Logseq
	- [[Obsidian]] is generally better suited for long-form writing, but Logseq can be useful for organizing and structuring an entry
- you can control whether to show braces around internal links
  collapsed:: true
	- I prefer not to see them
	- the downside is that it can be hard to tell where one link ends and another begins if they are next to each other
	- but I prefer not having the clutter that the extra four bracks `[[` and `]]` add
	- most of the time I don't have multiple links next to each other
- the journals "page" is the default page in the main panel
  collapsed:: true
	- this page is actually a list of recent journal pages in descending order
	- a new journal page gets created automatically each day
	  collapsed:: true
		- this can be annoying if you don't write anything on the journal page for that day
		- it should be an option for the page to automatically get created vs. only get created if the user writes something #[[Logseq improvements]]
	- the default journal page view lacks a calendar to help you navigate to prior journal entries
	  collapsed:: true
		- there is a calendar plugin that lets you see which days you have entries
		- otherwise you need to do a fair amount of scrolling to look through your entries
		- this is where the top-level collapse functionality comes in handy
		- if you have a few top-level nodes that summarize the projects your working on, you can easily browse through the days to check your activity
		- I don't normally go back many days in Logseq
		- one of the advantages of having this journal format is that irrelevant notes tend to naturally fall away
		- there is a risk that important notes will follow suit but if you are careful about the entities and tags you use, this is less of a risk
- the UI is limited in how much information it can display at one time
  collapsed:: true
	- most of this time I have not found this constraint to be a problem
	- in a way, the limitation helps you limit what you need to look at
	- but it can be difficult to navigate between multiple pages
	- I use the back and forth [[keyboard shortcuts]] to help me navigate my history
	- it would be really useful to have a history view of the pages I've visited #[[Logseq improvements]]
- if you take a lot of notes on a page, you need to think about the best way to structure the outline
  collapsed:: true
	- the goal is to hide complexity beneath a few top-level notes
	- you also don't want there to be too much nesting because it can make navigating the outline difficult
	- there are [[keyboard shortcuts]] to expand and collapse all the nodes on a page at one
	- sometimes this shortcut is not useful because I just want to collapse the top nodes and leave the others expanded so that I don't have to go through an manually expand each level
	- the shortcut also doesn't work when you are viewing multiple journal pages
	- I wrote a [[PowerShell]] script that only toggles the top-level nodes
		- it works across all pages on the graph at once
		- I did add a few exceptions for the contents page
- there is a graph view that shows you the links between pages
  collapsed:: true
	- I don't use this very much at all
	- it can be useful to help you visualize which pages are the most connected and whether there are any without any links but I typically don't do much with that information
- there are whiteboards where you can control which connections to show
  collapsed:: true
	- I see this feature being more useful than the graph view
	- It would be helpful if you could automatically generate the whiteboard based on relationships similar to how the graph view looks, but then prune the connections #[[Logseq improvements]]
	- a good use case I see for whiteboards is helping other people navigate your graph
	- you can highlight where the important points are and they can easily jump to those pages
	- I will experiment with that feature while I'm creating this site