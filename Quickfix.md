The easiest way to navigate the quickfix list (or the location list, for that matter) is the unimpaired plugin.

Once the quickfix window is populated, [q and ]q go forward and back (respectively) in the quickfix list. [Q and ]Q go to the beginning and end (which is especially handy if you only have one item in the list; this makes vim complain about [q and ]q). So the workflow is:

Run whatever command populates the quickfix list
Type [Q to go to the first item
Scroll through subsequent items (if any) with [q and ]q

:copen " Open the quickfix window
:ccl   " Close it
:cw    " Open it if there are "errors", close it otherwise (some people prefer this)
:cn    " Go to the next error in the window
:cp    " Go to the previous error in the window
:cnf   " Go to the first error in the next file
