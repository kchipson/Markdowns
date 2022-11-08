navigation

| Клавиша  |  Действие |
| ------------ | ------------ |
|p|Вставка текста после курсора|
|P|Вставка текста перед курсором|
|j, {n}j | move up line, or move up {n} lines|
|k, {n}k | move down line, or move down {n} lines|
|g{letter} |	quick go to (system level dir's)|
|gn, Ctrl-n | new tab|
|tab, shift-tab | switch tab|
|q | quit tab or |
|Q | quit ranger|
|uq | restore closed tab|
|[, {n}[ | move up dir in same parent, or move up n parent dir's|
|], {n}] | move down dir in same parent, or move down n parent dir's|
|H | move back 1 dir in history|
|L | move forward 1 dir in history|
|m{any letter} | bookmark the dir |
|`{any letter}, '{any letter} |	go to dir bookmarked {any letter}|
|`` | go to previous dir|
|dc	| update cumulative dir size|


sorting
| Клавиша  |  Действие |
| ------------ | ------------ |
|ot	| sort by type first|
|os	| sort by size first|
|oa/oc/om | sort by time|
|on	| sort natural|
|o{T/S/A/C/M} | sort in reverse order|
|or	| reverse the sort order|



file actions
/, f	enter file name to navigate (f can't do this with my keybinds as I make use of it)
n	search newest file in dir, or next after search with /, f
N	previous file after search
c..	set the next search order
o..	set the sort order
i	focus a highlighted file with less (but only able to see part of file)
i to toggle focus, E to edit in nano
y y	copy
y a	copy add to buffer (can copy-paste files from multiple directories this way)
y r	copy remove from buffer
y G	copy all files from selected to bottom of list
y gg	copy all files from selected to top of list
d d	cut (da, dr also to cut from multiple directories, dG, dgg also)
p p	paste
p P	paste (add to queue)
p o	paste with over-write
p O	paste with over-write (add to queue)
u d	clears copy/cut buffer, also uy (I change this to uu as it seems faster)
c w	rename/bulk rename
I	edit name, cursor at front (I change it to i, and make Alt-i view in pager)
A	edit name, cursor at end
a	edit name, cursor inside extension
E	edit file with bash editor (I change this to fe - there is F4 as well - see how to set nano as editor below)
insert	touch (create new file) (I add ft)
delete	deletes file (no confirm for single files by default -can change in conf.rc)
r	open file with program on rifle list
r 1	unpacks selected archive (need to install atool) -actually hits the 1st option with rifle (you can just type 1 Enter)
11,12,13,14 Enter	(on image file) set image as desktop background with feh (11=scale, 12=tile, 13-center, 14=fill)
+ / -	chmod commands
{octal no} =	change permissions, e.g. 744 =, set permissions to -rwxr--r--

marking
Space	mark
v	invert selection
V, uV	marks/unmarks files as cursor moves, until escape pressed, or yanked etc (I change this to b)
u v	unmark all files
t	tag toggle
u t	remove all tags
T	remove any tags of selected files
"{x}	custom tag
M..	linemode select (I change this to Alt-m)

operation
Ctrl-R	reload
Ctrl-h, z h	toggle hidden files (I add to this F2)
Ctrl-c	cancel an operation
Ctrl-s	freeze ranger! Ctrl-c to continue
:flat 1	puts all files of sub-dir's (1 level deep) in the main column
z	toggle settings
:, ;	open console to enter commands
s, !, @, #	open shell console
1?	display all key bindings alphabetically
2?	Ranger commands usage
3?	Ranger settings
?, F1	man page, key bindings or settings
W	message log
w	job queue


Macros used in console and shell
%f	the highlighted file
%d	the path of the current directory
%s	the selected files in the current directory. (defaults to highlighted file if none selected)
%t	all tagged files in the current directory
%c	the full paths of the currently copied/cut files
%p	the full paths of the selected files


Flags used with open_with and shell commands
(type r for open_with, or s, !, @ for shell. open_with flags must be plain with no dash -)

-f	runs process in background - useful for an encoding/mogrify job as ranger will still be usable while the process completes
-c	runs on current file, not selected
-r	runs with super user privileges
-t	will show the process in a new terminal window (opens xterm)


Flags used with only the shell command
-p	sends the process to the pager - which is closed with q, or canceled before with Ctrl-C
-s	silent mode - the output is discarded
-w	bash waits at the end of the process so that you can read the output and then press enter


typing '@-rf geany' will open a file with sudo (writes `shell -rf geany %s` to console)
