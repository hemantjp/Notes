Its more along the lines of dmneu that a file finder

Cris: 
An example simulating grep search
cat people.csv | zf
contents of a file piped into fzf and this will pop up a search list within fzf and then one can search the txt of string they are looking for

Plus the search is much more functional since fuzzy match


fzf by itself just gives the list of all the files
2 ways
fzf
find . -type f | fzf

exact match 
fzf '<filename>
fzf -e <filename>

open file for editing
fzf | xargs -or $EDITOR

and on selecting them pipes out to stdo

also we can pipe stdin into fzf 
simple as : | fzf 

an example of both (lukesmith)
du -a ~/scripts/* | awk '{print $2}' | fzf | xargs -r EDITOR
dua lists files in folder with sizes, awk only pipes file names, which fzf then displays for us to select the one we want and then the selected one is piped inot EDITOR

also there is some xtra cp -visual stuff in that video

