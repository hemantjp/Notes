:let @/= lets you mdify last searched pattern

To clear the last used search pattern:
:let @/ = ""
This will not set the pattern to an empty string, because that would match everywhere. The pattern is really cleared, like when starting Vim.

global search and replace
find text
select text using *. text wont actually show up as selected
then :%s//<will replace>/gc
inital empty // will automatically fill value  taken from *

To turn off highlighting until the next search:

:noh
Or turn off highlighting completely:

set nohlsearch
Or, to toggle it:

set hlsearch!

nnoremap <F3> :set hlsearch!<CR>

