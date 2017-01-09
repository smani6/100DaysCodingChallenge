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

[1]:	https://github.com/GrfxGuru/CodeNotesForiOS