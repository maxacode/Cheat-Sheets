# Screen 

Screen or GNU Screen is a terminal multiplexer. In other words, it means that you can start a screen session and then open any number of windows (virtual terminals). This does not contain all of screen’s commands and options, read GNU’s manual to see everything

### CLI Options
- -S	Starts a named session
- -r [name]	Reattach to a screen (optionally by name)
- -ls or --list	Returns a list of session ids
- -d -r detach and attach right a new an existing one. 

### Screens
- ctrl+a c	Create a new screen tab inside a screen
- ctrl+a [0-9]	Switch to a screen tab by number 0 through 9
- ctrl+a n	Go to the next screen tab
- ctrl+a p	Go to the previous screen tab
- ctrl+a k	Kill current screen tab
- ctrl+a ctrl+d	Detach the current screen and go back to the terminal (screen windows will stay running)

### Visual pleasure
- ctrl+a S	Split a screen horizontally
- ctrl+a |	Split a screen vertically
- ctrl+a ctrl+I or ctrl+a tab	Change screen split
- ctrl+a Q	Remove all screen splits
- ctrl+a C	Clear the current screen tab

### Accessibility
- ctrl+a A	Rename current screen tab
- ctrl+a k	Kill current screen tab
- ctrl+a ctrl+a	Switch to last used screen tab
- ctrl+a a	Send ctrl+a to current screen tab
-ctrl+a ctrl+w	See a list of all screen tabs in the current screen
