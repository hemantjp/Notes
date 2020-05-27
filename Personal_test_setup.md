## include test functions
For GCC, this is accomplished in two stages:

First compile the data but tell the compiler to separate the code into separate sections within the translation unit. This will be done for functions, classes, and external variables by using the following two compiler flags:

-fdata-sections -ffunction-sections


Link the translation units together using the linker optimization flag (this causes the linker to discard unreferenced sections):
-Wl,--gc-sections

remove this from compile process
else
the linking part happens in the final -o section
maybe we can keep this for rest and skip only for our test files
