/g global
/gc as confirmation
/gi case insensitive
/gI case sensitive 

:s/foo/bar/g	Change each 'foo' to 'bar' in the current line.
:%s/foo/bar/g	Change each 'foo' to 'bar' in all the lines.
:5,12s/foo/bar/g	Change each 'foo' to 'bar' for all lines from line 5 to line 12 (inclusive).
:'a,'bs/foo/bar/g	Change each 'foo' to 'bar' for all lines from mark a to mark b inclusive (see Note below).
:'<,'>s/foo/bar/g	When compiled with +visual, change each 'foo' to 'bar' for all lines within a visual selection. Vim automatically appends the visual selection range ('<,'>) for any ex command when you select an area and enter :. Also, see Note below.
:.,$s/foo/bar/g	Change each 'foo' to 'bar' for all lines from the current line (.) to the last line ($) inclusive.
:.,+2s/foo/bar/g	Change each 'foo' to 'bar' for the current line (.) and the two next lines (+2).
:g/^baz/s/foo/bar/g	Change each 'foo' to 'bar' in each line starting with 'baz'.
