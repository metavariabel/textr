# textr
Simple text formatter (find/replace, sql formatter, list macros, batch edit) made in Windows Forms.

Supposed to make daily work easier by allowing quick access to functions like:

turn list into ,-separated list
add ' to list ('123', '234', '345')
SQL formatting (may not work very well but it's there!)
find and replace
remove duplicates
new line after/before x occurences of y
remove empty rows

Each function is a transform that is added to a list, so if you change something in the left-hand-side text box, all transforms will automatically retrigger and update the copyable right-hand-side text box.

Batch edit mode matches a search phrase against each line and performs changes. For example this list:
select hello, person from friends
select hello, person from enemies
select hello, person from frienemies

Selection mode:
turn select * from *
into union select *, bye from * where

will produce this result:
union select hello, person, bye from friends
union select hello, person, bye from enemies
union select hello, person, bye from frienemies

Format mode:

turn select hello, person from *
into select '*:' '*:', hello, person from *

will produce this result:
select 'friends:' 'friends:', hello, person from friends 
select 'enemies:' 'enemies:', hello, person from enemies 
select 'frienemies:' 'frienemies:', hello, person from frienemies 

Jira button gives a few shortcuts to jira commands. Use to easily make a list of attachments, images (with or without thumbnails) or links. mark text in bold/italics using a rich text editor.

Horse icon credits: https://thenounproject.com/search/?q=swing%20horse&i=2121526
