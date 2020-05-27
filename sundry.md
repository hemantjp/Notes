## silent
u can use the extra command silent if you want to suppress normal breakpoint output when the breakpoint is hi

## Pending [Breakpoints](Breakpoints)
If the debugger cannot resolve a breakpoint location you specify to an address in the current debuggee, it will ask whether to create a 'pending' breakpoint.

A pending breakpoint will be re-evaluated every time a shared library is loaded.  If the location can be resolved to an address at one of those times, the pending breakpoint will become a real breakpoint at that address.

## string compare
could also use the built-in $_streq(str1, str2) function:

## convenience fuction
https://sourceware.org/gdb/onlinedocs/gdb/Convenience-Funs.html
