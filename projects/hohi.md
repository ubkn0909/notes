This is a tui app with a horizontal hierarchy for managing todos. Its similar to gingko.

I think I will use golang and bubbletea for this project

**Design:**
- infinite column insertion 
	- how should we resolve the parentless cards that are created if we insert a hierarchy above?
- priority through row arrangment (the topmost card has the highest priority)
- status of a task/card
	- shows the date when a task was started and also the date when a task ended and also shows in human-readable format how long it took to complete that task
	- have a section that lists all currently started/doing tasks 
		- and there should be a way to access its actual location
	- 