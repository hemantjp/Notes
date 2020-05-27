if included header file had one declaration not definition and mutiple .c filesi import it then itll act as a global variable.
however this si not the recomemnded way.. hence extern usage

when defined in header this leader to double definition if the .c files build of each other. eg. call functions 
https://stackoverflow.com/questions/8108634/global-variables-in-header-file

very detailed
https://stackoverflow.com/questions/1433204/how-do-i-use-extern-to-share-variables-between-source-files?noredirect=1&lq=1
