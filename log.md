# 100 Days Of Code - Log

**Link to work project:** [https://github.com/GrfxGuru/CodeNotesForiOS][1]

### Day 0: January 2nd, 2017

**Today's Progress**: Initial fork of the 100 Days repository.

**Thoughts:** Not having taken part in this project before, I thought the set-up rules were pretty straight forward. Would be nice to have a clean Git history to start with, but not a big deal.

### Day 1: January 3rd, 2017

**Today's Progress**: Xcode Project Created
- Created the Xcode Master / Detail project.
- Removed code from template project that is not needed, including a display label from the detail view and NSDateObject from the master list.
- Added a new value object class to hold a note.
- Refactored project structure to organize code better.

**Thoughts:** Initial application creation can be annoying sometimes when you start from a template, removing code and keeping the build working can take longer than it should.

### Day 2: January 4th, 2017

**Today's Progress**: Note List Prototype Cell
I created the prototype cell for the master list, actually I created it twice since Xcode 8 screwed it up and deleted the cell contents twice due to bugs! I also set a hard return of note count so I could check the layout of multiple cells. I used stack views for the items within the cell to hopefully make it easier to change the layout as the program matures.

**Thoughts:** Xcode 8 bugs mean’t I had to do somethings more than once today and also repair the errors it left behind. Stack views have been a great addition to iOS to enable some automatic handling of layout.

### Day 3: January 5th, 2017

**Today's Progress**: Start of screen layouts for the detail views including, view / Edit / Add and Deleting of a note.

**Thoughts:** Not as much progress as I would of liked today due to external factors. The screens are far from complete, at this time they are more content holders than layout complete. There is no re-sizing or real design yet for any of the screens, but that will come once the basic shell of the app is in place.

### Day 4: January 6th, 2017

**Today's Progress**: The Change log
- Added empty screen to edit application settings.
- Added button to access future settings.
- Added a button to add a new note from the notes list.
- Created a function that will eventually load the data from the file system when the application starts.
- Added a temporary data structure to the loading function for testing purposes.

**Thoughts:** I think the screens are getting close to needing a proper design and clean up. I also need to start creating the proper segues for passing data around and ensuring the correction navigation items remain, currently adding a note replaces the navigation in some instances on the details view.

I have decided to post every seven days a more detailed overview of the weeks progression. I will be posting this both on Medium and my web site where I discuss Swift development. Links will be in this log when they are created.

### Day 5: January 7th, 2017

**Today's Progress**: The Change log
- Details list cells now populate with data from a note
- Decided one link to the Github project at the log was more sensible than the same link every day, changed previous day logs accordingly.
- Created a date formatter for general usage in the application.


**Thoughts:** 
I need to debug the conversation and display of the date object for each note list cell. For personal reasons I did not get as much done today as I would of liked.

### Day 6: January 8th, 2017

**Today's Progress**: The Change log
- Date formatter function now works with a month/day/year format. Previously it was configured for an hour/minute/second format that I had used on another project.
- Note object creation refactored to a function that takes arguments.
- Added constraints for the master list cell.
- Started work on the constraints for the viewing of a note.

**Thoughts:** 
Anyone that has dealt with constraints in Xcode knows the pain of trying to get them right, so annoying to work with.

### Day 7: January 9th, 2017

**Today's Progress**: The Change log
- Fixed the layout of the view note detail screen for all device rotations.
- Changed view note screen text fields to labels for display only.
- Updated segue for displaying a note.
- When selecting from the note list, it will now display the details.

**Thoughts:** 
Some times, in fact for me most times, the best way to deal with constraint problems is to remove them all and start again. Whilst Xcode storyboards go a long way to try and help you solve layout issues, there are times all it does is create problems.

I had more trouble than I expected with the sending of the data across the segue when selecting a note from the list and displaying it. I have blogged and used the technique many times, but there are always the little gotcha’s. In this case I had to wrap the detail screen in a navigation controller to get it working properly, this was an oversight on my part and a lesson I will not soon forget.

### Day 8: January 10th, 2017

**Today's Progress**: The Change log
- Spent time today looking at a few storage options including SQLLite, Plists, CoreData, and a few more projects on Github. This will aid in deciding on the data store I intend to use.
- Added constraints for the editing and adding note views.
- Updated the table view cell height.

**Thoughts:** 
- No clear decision yet on the data store. I do feel CoreData will be overkill and take a lot of implementation.

### Day 9: January 11th, 2017

**Today's Progress**: The Change log
- Added the ‘add’ button to the new note screen and updated constraints.
- When creating a new note it is now added to the data source.

**Thoughts:** 
Still working to refresh the master list after adding a new note, still need to return to the first detail screen after adding a new note.

### Day 10: January 12th, 2017

**Today's Progress**: The Change log
- No file changes to the project today.

**Thoughts:** 
Today was pure trial and error regarding navigation techniques between views to find a method that gives me what I need and is resource friendly, hopefully the results will make it in to the app over the next few days.

### Day 11: January 13th, 2017

**Today's Progress**: The Change log
- Refactored the adding of a new note to use the edit view.
- Clicking the + on the list view now creates a new note on the list and selects it, this is then sent to the edit view.

**Thoughts:** 
Sometimes, when something appears to be causing you a lot of problems, this is a sign that you are approaching the solution the wrong way and need to think again. This was the case with adding a new note, after some thought and trial and error, I realized that I should create a blank note and then select and edit it rather than try to pass data and navigation around.

### Day 12: January 14th, 2017

**Today's Progress**: The Change log
- Due to system issues I did not get to code today, but everything is ready to continue tomorrow.

**Thoughts:** 

### Day 13: January 15th, 2017

**Today's Progress**: The Change log
- Refactored segue code yet again for the adding of a note.

**Thoughts:** 
I confess to being tired of trying to solve my segue \<\> viewController issues. I think I am going to have to make a test project to do nothing but study UINavigationController and segue code.

### Day 14: January 16th, 2017

**Today's Progress**: The Change log
- Resolved my segue navigation issues with editing / adding a note.

**Thoughts:** 
Finally resolved my navigation issues with editing a new note, after clearing out the mess created, things now work as expected. I am still working on updating the data source and refreshing the detail list.

### Day 15: January 17th, 2017

**Today's Progress**: The Change log
- When cancelling a new note, the new note is removed from the master list.
- When saving a new note, the note is now stored in the array and the master list is updated.
- When going to the add / edit note screen, the note name is now selected by default ready to just start typing.

**Thoughts:** 
Starting work on the data handling proper, I have left test data in for now until persistent storage is implemented. An interesting way to throw data around and access it across the application is to use a singleton. I implemented it in the application delegate and create a reference in each of the views that need to work with the data.

### Day 16: January 18th, 2017

**Today's Progress**: The Change log
- You can now delete a note when viewing it.
- Alert presentation of choice when deleting a note, you can either cancel or delete.

**Thoughts:** 
Interesting way to work when deleting something and showing an alert dialog. I first show the dialog and if you choose to delete, I remove the record, update the master list display, and then perform a segue that I attached to the view rather than a control on the screen.

### Day 17: January 19th, 2017

**Today's Progress**: The Change log
- Enabled the edit button when viewing a note to switch to edit mode.
- Moved the application settings button to the master list.
- Added the option to either show or not show the note deletion confirmation alert, code still needs to be written to activate it.
- Moved the settings view into a navigation controller for consistency.

**Thoughts:** 
I have spent most of my career working on user interfaces, and as I start to think about the designs and layout for this application, I am reminded again of all the little things you have to take in to consideration like deselecting something under a certain condition. For example, deselect any note that might be selected on the master list when going to the settings screen. Often these can be some of the most timing consuming things to deal with.

### Day 18: January 20th, 2017

**Today's Progress**: The Change log
- The user can no longer edit text whilst on the view note screen.
- Working with Sketch to design some better looking layouts now the functionality is coming together.

**Thoughts:** 
Sketch continues to be my tool for putting ideas together fast when it comes to layouts. I plan to design in the app and export to Xcode.

### Day 19: January 21st, 2017

**Today's Progress**: The Change log
- The application settings are now operational and stored.
- The confirmation dialog for deleting a note can now be turned on or off in the user settings.

**Thoughts:** 
A good day, the application settings are now working and ready for any other options I might put in there. I am considering a dark/light interface setting as that seems popular these days.

### Day 20: January 22nd, 2017

**Today's Progress**: The Change log
- Added application information to the settings screen.
- Changed the language field on the add / edit screen to use a UIPickerView instead. This is a work in progress but there are several reasons for this choice.
	- Consistent spelling.
	- Quicker entry method.
	- Will provide a data source for other users including filtering and searching.

**Thoughts:** 
I think the switch to using a picker for the language field will be far better in the long run as I bring other features online. There will also be a way to manage the language list including editing, adding, and deletion. This also serves as a great excuse to work with delegation in Swift.

### Day 21: January 23rd, 2017

**Today's Progress**: The Change log
- Played with CoreData some today as I think this will be my data source for the application.
- Worked more on some Sketch designs.
**Thoughts:** 
CoreData has a reputation for being difficult, but I think if you approach it correctly, it can yield good results. I might change my mind later in the project, but for now this is the winner.

### Day 22: January 24th, 2017

**Today's Progress**: The Change log
- Fixed some display issues for the master list when the device is in portrait mode.
- When the application returns from the background it now corrects the interface display for the master list.
- Designed and added an icon for the application. Used the excellent IconSlate tool. [App Store Link][2]

**Thoughts:** 
Always check both portrait and landscape modes for user interface problems. I had not noticed until today that the master list was not displaying automatically if the application started with the iPad in portrait mode.

### Day 23: January 25th, 2017

**Today's Progress**: The Change log
- Added an icon to the settings page.
- Continued reading into CoreData.

**Thoughts:** 
Not a lot of actual project code today, but a lot of reading on CoreData in preparation.

### Day 24: January 26th, 2017

**Today's Progress**: The Change log
- Continued reading into CoreData.

**Thoughts:** 
More CoreData exploration and model planning.

### Day 25: January 27th, 2017

**Today's Progress**: The Change log
- Removed CoreData branch, planning to start again with this rather than patch into existing data source.

**Thoughts:** 
While researching CoreData, I have come across many different ways to use it. At this time I am not sure which I agree with the most, therefore I am trying a few different ways of using it before settling on one method.

[1]:	https://github.com/GrfxGuru/CodeNotesForiOS
[2]:	https://itunes.apple.com/us/app/icon-slate/id439697913?mt=12