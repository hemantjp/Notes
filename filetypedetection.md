By default, Vim assumes all .h files to be C++ files. 
However, I work with pure C and want filetype to be c. 
Since project also comes with doxygen documentation, I want to set subtype to doxygen to enable very nice doxygen highlighting.

Add lines like these to your local .vimrc file:

augroup project
  autocmd!
  autocmd BufRead,BufNewFile *.h,*.c set filetype=c.doxygen
augroup END
