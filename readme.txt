==========================================
ccccc	ooooo	l		ooooo	rrrr	!!
c		o	o	l		o	o	r	r	!!
c		o	o	l		o	o	rrrr	
ccccc	ooooo	lllll	ooooo	r	r	!!
==========================================

// Update //
Check version_log.txt for info on the new update!

// Documentation //
This document is for how to integrate this console with your gamecode. If you need help with anything,
just message me on discord (Epsiilon#2048)!

// Integration //
 - Display variable values using the display function
 - Display console messages using the output_set function
 - Set the input using the input_set function - you could use this to hotkey commands, which is
   something I intend to add soon
 - Even send messages to the player using the window_set function! spooky!
 - You can run your own scripts with the console with little-to-no effort required, so long as it uses
   supported data types (unsupported ones include arrays, structs, and data structures, and you'll just
   have to code your way around them in the script).
   
// Console help //
For help on in-game console commands, type "help" in the console. By default, it is toggled with the tab 
key. This help command is insufficient and will be updated later.

// Macros and built-in global variables //
Build-in global variables such as mouse_x have to be prefixed by "global.", and macros have to be added
manually, as there isn't a way to automatically search for them. Doing this is easy however, just add to
the switch statement in the macro_get script.

// Object identifier trouble //
As it is, the console currently relies on an object identifier in the name of the object to determine if a
data type is an object ID. You might prefix your object names with "o_" or "obj_". By default, it checks
for "o_". You can change it by changing the obj_identifier macro in the console create event. This system 
isn't very good because it doesn't support camel casing. For instance, if your objects were named 
as "oName", the identifier would have to be just "o", meaning you wouldn't be able to access any variables 
that start with an "o" properly. In later releases, I'll fix this. In the meantime however, I've added a 
universal object identifier, which is "o/". I'm not a fan of this solution, but it works for now.

// Spaghetti code //
There is a lot of stuff that should be cached and isnt, and there's probably also a lot of redundant logic.
The code in general is pretty unreadable, too. I plan to fix all of this in later versions. A lot of the
variable names are overly long, confusing, and inconsistent. I'll fix this in later versions.

// Potential features //
 - The ability to scroll through console commands which exceed the length
 - Embedding commands in text which can be clicked to activate
 - Hovering over scripts in the commandline shows help
 - Undo and redo
 - Autofill and real time syntax errors
 - Better synchronization between GML and the console syntax
 - Color picker window
 - Sprite support
 - Variable value sliders
 - Hotkey binding to commands
 - Buttons which activate a command when pressed
 - A command that allows you to specify another command to be run every frame
 - Console color palette presets
 - Text file logs
 - (proper) struct and array support
 - (possibly?) universal data structure support
 - (unlikely) support for scripts being run within scripts