# in-the-mail

Integration between Gmail (at least) and Inthe.AM/TaskWarrior

## Brainstorming

This is a place to get my initial ideas for this project written down before they have enough form to go into an issue tracker. I expect the brainstorming section of this document to disappear during the early phases of development, as more of it is reified and expanded in the issue tracker.

### Purpose

The idea of this project is to be able to integrate received e-mail with [TaskWarrior](http://www.taskwarrior.org). When I receive an e-mail message, it would be nice to be able to click a button (or forward it to a known address) to create a TaskWarrior task—and then have that task contain some sort of link to the e-mail message (Gmail uses unique message IDs, so that should not be hard). Inthe.AM actually does contain [some e-mail support](https://inthe.am/configure), but it's basically limited to sending literal TaskWarrior commands in e-mail messages.

### Support

Initially, I'm going to be doing this to support my own needs, which is to support the Gmail web interface (and possibly POP/IMAP clients, e.g. on mobile) and [Inthe.AM](http://inthe.am) as a TaskWarrior server. Ideally, I'd like it to work with a generic Taskserver installation, and hopefully other e-mail providers (as [Mailvelope](https://www.mailvelope.com/) does).

### Implementation ideas

I tried to implement this as a Gmail [contextual gadget](https://developers.google.com/gmail/contextual_gadgets), but it turned out that the interface for writing gadgets sort of sucks. I think my next attempt will be to implement it as a browser extension/userscript. I'm not sure what needs to be done on the TaskWarrior side, except for adding an annotation or UDA that contains the ID of the e-mail message.
