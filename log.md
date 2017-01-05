# 100 Days Of Code - Log

### Day 0: January 2nd, 2017

**Today's Progress**: Initial fork of the 100 Days repository.

**Thoughts:** Not having taken part in this project before, I thought the set-up rules were pretty straight forward. Would be nice to have a clean Git history to start with, but not a big deal.

**Link to work:** \<Coming\>

### Day 1: January 3rd, 2017

**Today's Progress**: Xcode Project Created
- Created the Xcode Master / Detail project.
- Removed code from template project that is not needed, including a display label from the detail view and NSDateObject from the master list.
- Added a new value object class to hold a note.
- Refactored project structure to organize code better.

**Thoughts:** Initial application creation can be annoying sometimes when you start from a template, removing code and keeping the build working can take longer than it should.

**Link to work:** [https://github.com/GrfxGuru/CodeNotesForiOS][1]

### Day 2: January 4th, 2017

**Today's Progress**: Note List Prototype Cell
I created the prototype cell for the master list, actually I created it twice since Xcode 8 screwed it up and deleted the cell contents twice due to bugs! I also set a hard return of note count so I could check the layout of multiple cells. I used stack views for the items within the cell to hopefully make it easier to change the layout as the program matures.

**Thoughts:** Xcode 8 bugs mean’t I had to do somethings more than once today and also repair the errors it left behind. Stack views have been a great addition to iOS to enable some automatic handling of layout.

**Link to work:** [https://github.com/GrfxGuru/CodeNotesForiOS][2]

[1]:	https://github.com/GrfxGuru/CodeNotesForiOS
[2]:	https://github.com/GrfxGuru/CodeNotesForiOS