# VIM Cheatsheet

_Motion, keyboard commands and shortcuts for VI Improved_

* [Legend](#legend)
* [Motion / Normal mode](#motion---normal-mode)
* [Insert mode](#insert-mode)
* [Changes](#changes)
* [Yank/Put or Copy/Paste](#yankput-or-copypaste)
* [Visual/Visual Block Mode](#visual--visual-block-mode)
* [Commands](#commands)
* [Files](#files)
* [Windows](#windows)
* [Tabs](#tabs)
* [coc.nvim](#cocnvim)
* [Denite](#denite)
* [Help](#help)
* [Search/Replace](#search--replace)
* [Find Files](#find-files)

![Graphic](http://i.imgur.com/HkCjM63.png)

## Legend

|  Command      | Keyboard Character           |
|  :---         | :---:                        |
|  command      | <kbd>⌘</kbd>                 |
|  control      | <kbd>⌃</kbd>                 |
|  alt          | <kbd>⎇</kbd>                 |
|  delete       | <kbd>⌫</kbd>                 |
|  option       | <kbd>⌥</kbd>                 |
|  shift        | <kbd>⇧</kbd>                 |
|  caps lock    | <kbd>⇪</kbd>                 |
|  tab          | <kbd>⇥</kbd>                 |
|  arrow up     | <kbd>↑</kbd>                 |
|  arrow down   | <kbd>↓</kbd>                 |
|  arrow left   | <kbd>←</kbd>                 |
|  arrow right  | <kbd>→</kbd>                 |
|  escape       | <kbd>⎋</kbd> or <kbd>␛</kbd> |
|  return/enter | <kbd>⏎</kbd> or <kbd>⌤</kbd> |
|  home         | <kbd>↖</kbd>                 |
|  end          | <kbd>↘</kbd>                 |
|  page up      | <kbd>⇞</kbd>                 |
|  page down    | <kbd>⇟</kbd>                 |


## Motion - Normal Mode

* <kbd>j</kbd>          - Down
* <kbd>k</kbd>          - Up
* <kbd>h</kbd>          - Left
* <kbd>l</kbd>          - Right
* <kbd>0</kbd>, <kbd>⇧6</kbd>    - Line beginning
* <kbd>$</kbd>          - Line ending
* <kbd>e</kbd>, <kbd>w</kbd>     - Forward (Small word)
* <kbd>⇧e</kbd>, <kbd>⇧w</kbd>     - Forward (big word forward (whitespace only))
* <kbd>b</kbd>          - Backwards (small word)
* <kbd>⇧b</kbd>          - Backwards (big word)
* <kbd>f&lt;char&gt;</kbd>    - Jump to first occurrence of &lt;char&gt;
* <kbd>;</kbd>          - Repeat previous jump
* <kbd>⇧f&lt;char&gt;</kbd>    - Jump to previous first occurrence of &lt;char&gt;
* <kbd>t&lt;char&gt;</kbd>    - Jump to position before first occurrence of &lt;char&gt;
* <kbd>⇧t&lt;char&gt;</kbd>    - Jump to position before first previous occurrence of &lt;char&gt; in the direction youre searching
* <kbd>&lt;n&gt; &lt;motion&gt;</kbd> - Prefix `motion` command with a number `n` to have it jump that `n` away. e.g. <kbd>4li</kbd> jumps to the 4th 'i' forward.
* <kbd>⌃f</kbd>         - Forward (page)
* <kbd>⌃b</kbd>         - Backward (page)
* <kbd>⌃u</kbd>         - Upward (half page)
* <kbd>⌃d</kbd>         - Downward (half page)
* <kbd>⇧h</kbd>         - Head (of current page)
* <kbd>⇧m</kbd>         - Middle (of current page)
* <kbd>⇧l</kbd>         - Lowest (of current page)
* <kbd>gg</kbd>         - Go to top of file
* <kbd>⇧gg</kbd>        - Go to bottom of file
* <kbd>&lt;n&gt;⇧g</kbd>      - Go to line `n`
* <kbd>][</kbd>         - Jump to next matching brace
* <kbd>[]</kbd>         - Jump to previous matching brace
* <kbd>%</kbd>          - Jump between matching braces
* <kbd>za</kbd>         - Toggle code fold
* <kbd>zo</kbd>         - Open code fold
* <kbd>zc</kbd>         - Close code fold
* <kbd>zr</kbd>         - Open one layer of code folds
* <kbd>z⇧r</kbd>        - Open all code folks


## Insert Mode

These commands are entered while in Normal or visual mode.

* <kbd>i</kbd>                - Insert at cursor
* <kbd>⇧i</kbd>               - Insert at line beginning
* <kbd>a</kbd>                - Append after cursor
* <kbd>ea</kbd>               - Append after word at cursor
* <kbd>⇧a</kbd>               - Append at end of line
* <kbd>o</kbd>                - Insert line below cursor
* <kbd>⇧o</kbd>               - Insert line above cursor
* <kbd>x</kbd>                - Delete character under cursor
* <kbd>⇧x</kbd>               - Delete character before cursor
* <kbd>dd</kbd>               - Delete line at cursor position
* <kbd>d &lt;motion&gt;</kbd> - Delete amount by motion command e.g. <kbd>dw</kbd> delete small word
* <kbd>c &lt;motion&gt;</kbd> - Change by motion e.g. <kbd>cw</kbd> overwrite small word
* <kbd>r</kbd>                - Replace character at cursor
* <kbd>⇧r</kbd>               - Replace overwriting text
* <kbd>^v u &lt;codepoint&gt;</kbd> - Insert unicode character at `codepoint`
* <kbd>␛</kbd>                - Exit insert mode

## Changes

* <kbd>⇧j</kbd>            - Join line with line below
* <kbd>c(f|t)&lt;char&gt;</kbd>  - Change characters (inclusive with f or exclusive with t) to `char`


## Yank/Put or Copy/Paste

* <kbd>yw</kbd>         - Yank word into buffer
* <kbd>yy</kbd>         - Yank line into buffer
* <kbd>&lt;n&gt;yy</kbd>- Yank `n` lines into buffer
* <kbd>y &lt;motion&gt;</kbd> - Yank into buffer by `motion`
* <kbd>x</kbd>          - Yank character at cursor
* <kbd>p</kbd>          - Put buffer after cursor
* <kbd>⇧p</kbd>         - Put buffer before cursor


## Visual / Visual Block Mode

Visual mode is used for marking text.

* <kbd>v</kbd>          - Visual mode
* <kbd>V</kbd>          - Visual line-based mode
* <kbd>⌃v</kbd>         - Visual block mode
* <kbd>gv</kbd>         - Re-select previous Visual block buffer
* <kbd>o</kbd>          - Jump to other end of block
* <kbd>⇧o</kbd>         - Jump to other corner of block
* <kbd>vaw</kbd>        - Visual select a word (includes whitespace)
* <kbd>viw</kbd>        - Vissual select inner word (no whitespace)
* <kbd>vap</kbd>        - Visual select a paragraph
* <kbd>vip</kbd>        - Visual select inner paragraph
* <kbd>va[</kbd>        - Visual select [] block and contents
* <kbd>vi[</kbd>        - Visual select [] contents only
* <kbd>va{</kbd>        - Visual select {} block and contents
* <kbd>vi{</kbd>        - Visual select {} contents only
* <kbd>va(</kbd>        - Visual select () block and contents
* <kbd>vi(</kbd>        - Visual select () contents only
* <kbd>va<</kbd>        - Visual select <> block and contents
* <kbd>vi<</kbd>        - Visual select <> contents only
* <kbd>va"</kbd>        - Visual select all double quote and contents
* <kbd>vi"</kbd>        - Visual select inner quoted contents
* <kbd>vit</kbd>        - Visual select inner XML/HTML tag contents
* <kbd>vat</kbd>        - Visual select all XML/HTML tag contents
* <kbd>v&lt;motion&gt;</kbd> - Visually mark text by `motion` command
* <kbd>␛</kbd>          - Exit visual mode

The following commands can be used while text is marked.

* <kbd>c</kbd>          - Delete and begin inserting (To replace currently marked text)
* <kbd>d</kbd>          - Delete
* <kbd>y</kbd>          - Yank
* <kbd>&gt;</kbd>       - Indent right
* <kbd>&lt;</kbd>       - Indent left


## Commands

* <kbd>.</kbd>           - Repeat previous command
* <kbd>u</kbd>           - Undo previous command
* <kbd>⇧u</kbd>          - Undo all changes to current line
* <kbd>⌃r</kbd>          - Redo
* <kbd>:q</kbd>           - Quit
* <kbd>:q!</kbd>          - Quit (without saving changes)


## Files

* <kbd>:e &lt;path&gt;</kbd>           - OpEn file into buffer
* <kbd>:w</kbd>                  - Write buffer to file
* <kbd>:ls</kbd>                 - List open buffers
* <kbd>:(b|buf|buffer) &lt;n&gt;</kbd> - Switch to buff `n`
* <kbd>:(bd|bdelete) &lt;n&gt;</kbd>   - Delete buffer `n` (close file)
* <kbd>:bp</kbd>                 - Switch to previous buffer
* <kbd>:bn</kbd>                 - Switch to next buffer


## Windows

* <kbd>⌃wo</kbd> - make current window the Only window
* <kbd>:(sp|spl|split) &lt;path&gt;</kbd> - SPlit window horizontally, optionally loading file at `path`
* <kbd>:vsp &lt;path&gt;</kbd>            - Vertically SPlit window, optionally loading file at `path`
* <kbd>⌃ws</kbd> - Window split (horizontally)
* <kbd>⌃wv</kbd> - Window split (vertically)
* <kbd>⌃wx</kbd> - Windows eXchange, swap their position
* <kbd>⌃wk</kbd> - Move window up
* <kbd>⌃wj</kbd> - Move window down
* <kbd>⌃wh</kbd> - Move window left
* <kbd>⌃wl</kbd> - Move window right
* <kbd>⌃wp</kbd> - Move window previous
* <kbd>⌃wc</kbd> - Window close 
* <kbd>⌃w=</kbd> - Balance windows
* <kbd>⌃w+</kbd> - Grow horizontal window split by 1
* <kbd>⌃w-</kbd> - Shrink horizontal window split by 1
* <kbd>⌃w></kbd> - Grow vertical window split by 1
* <kbd>⌃w<</kbd> - Shrink vertical window split by 1
* <kbd>:(resize|res) (+|-)&lt;n&gt;</kbd> - Horizontal resize to `n` or increase/decrease by `n`
* <kbd>:vertical resize (+|-)&lt;n&gt;</kbd> - Vertical resize to `n` or increase/decrease by `n`


## Tabs

* <kbd>gt</kbd>          - GoTo next tab
* <kbd>g⇧t</kbd>         - Goto previous tab
* <kbd>&lt;n&gt;gt</kbd> - Goto tab `n`
* <kbd>:tabedit &lt;file&gt;</kbd> - Edit specified file in a new tab
* <kbd>:tabfind &lt;file&gt;</kbd> - Open a new tab with filename given
* <kbd>:tabclose</kbd>  - Close tab
* <kbd>:tabclose &lt;n&gt;</kbd>  - Close tab `n`
* <kbd>:tabonly</kbd>   - Close all other tabs

## coc.nvim

* <kbd>,dj</kbd> Open implementation at cursor (coc-implementation)
* <kbd>,dd</kbd> Open symbol definition at cursor (coc-definition)
* <kbd>,dr</kbd> Open panel of symbol references at cursor (coc-references)

## Denite

* <kbd>;</kbd>  - fuzzy-search buffers for a string
* <kbd>,t</kbd> - fuzzy-search current directory for string
* <kbd>,j</kbd> - fuzzy-search current directory for string at cursor

## Help

* <kbd>:h</kbd> - Open Help
* <kbd>⌃]</kbd> - Activate link at cursor
* <kbd>⌃T</kbd> - Back


## Search / Replace

* <kbd>/&lt;pattern&gt;</kbd>  - Search forward for `pattern`
* <kbd>?&lt;pattern&gt;</kbd>  - Search backward for `pattern`
* <kbd>n</kbd>                 - Jump to next match in searching direction
* <kbd>⇧n</kbd>                - Jump to next match in opposite direction
* <kbd>:&lt;range&gt;s/&lt;foo&gt;/&lt;bar&gt;/[g,i,I,c]</kbd> - Replace `old`
  with `new`.
  `range` is either empty, `%` for whole file, or a line number.
  `g` flag replaces all occurrances on the line.
  `i` ignores case. `I` doesn't ignore case. `c` asks for confirmation.
* <kbd>* &lt;n|⇧n&gt;</kbd>    - Search forward for word at cursor, `n` jumps to Next result, `N` jumps to previous
* <kbd># &lt;n|⇧n&gt;</kbd>    - Search backward for word at cursor, `n` jumps to Next result, `N` jumps to previous


## Find Files

For finding patterns in files. Use <kbd>:vimgrep</kbd> if unsure if the `grep`
command-line utility is available, but <kbd>:grep</kbd> is generally
faster. All searches fill a buffer that is accessible by the
<kbd>:cw</kbd> command.

* <kbd>:vimgrep /&lt;pattern&gt;/[g][j] &lt;path/**/*&gt;</kbd> - Search for regex `pattern` located in `path`.
  The `g` option specifies that all matches for a search will be returned instead of just one per line,
  and the `j` option specifies that Vim will not jump to the first match automatically.
* <kbd>:grep &lt;pattern&gt; &lt;path&gt;</kbd> - Search for regex `pattern` located in `path`.

## Awesome Key Mappings

The [leader](http://learnvimscriptthehardway.stevelosh.com/chapters/06.html#leader) is `,`, so whenever you see `<leader>` it means `,`.


### Plugin related mappings

Open [bufexplorer](https://github.com/vim-scripts/bufexplorer.zip) to see and manage the current buffers (`<leader>o`):
    
    map <leader>o :BufExplorer<cr>

Open [MRU.vim](https://github.com/vim-scripts/mru.vim) to see the recently open files (`<leader>f`):

    map <leader>f :MRU<CR>

Open [ctrlp.vim](https://github.com/kien/ctrlp.vim) plugin to quickly find a file or a buffer (`<leader>j` or `<ctrl>f`):
    
    let g:ctrlp_map = '<c-f>'

[NERD Tree](https://github.com/scrooloose/nerdtree) mappings:

    map <leader>nn :NERDTreeToggle<cr>
    map <leader>nb :NERDTreeFromBookmark 
    map <leader>nf :NERDTreeFind<cr>

[goyo.vim](https://github.com/junegunn/goyo.vim) and [vim-zenroom2](https://github.com/amix/vim-zenroom2) lets you only focus on one thing at a time. It removes all the distractions and centers the content. It has a special look when editing Markdown, reStructuredText and textfiles. It only has one mapping. (`<leader>z`)

    map <leader>z :Goyo<cr>


### Normal mode mappings

Fast saving of a buffer (`<leader>w`):

	nmap <leader>w :w!<cr>
	
Map `<Space>` to `/` (search) and `<Ctrl>+<Space>` to `?` (backwards search):
	
	map <space> /
	map <c-space> ?
	map <silent> <leader><cr> :noh<cr>

Disable highlights when you press `<leader><cr>`:
	
	map <silent> <leader><cr> :noh<cr>

Smart way to move between windows (`<ctrl>j` etc.):
	
	map <C-j> <C-W>j
	map <C-k> <C-W>k
	map <C-h> <C-W>h
	map <C-l> <C-W>l

Closing of the current buffer(s) (`<leader>bd` and (`<leader>ba`)):
	
	" Close current buffer
	map <leader>bd :Bclose<cr>
	
	" Close all buffers
	map <leader>ba :1,1000 bd!<cr>
	
Useful mappings for managing tabs:
	
	map <leader>tn :tabnew<cr>
	map <leader>to :tabonly<cr>
	map <leader>tc :tabclose<cr>
	map <leader>tm :tabmove 
	
	" Opens a new tab with the current buffer's path
	" Super useful when editing files in the same directory
	map <leader>te :tabedit <c-r>=expand("%:p:h")<cr>/
	
Switch [CWD](http://vim.wikia.com/wiki/Set_working_directory_to_the_current_file) to the directory of the open buffer:
	
	map <leader>cd :cd %:p:h<cr>:pwd<cr>
	
Open `ack.vim` for fast search:
	
	map <leader>g :Ack 

Quickly open a buffer for scripbble:
	
	map <leader>q :e ~/buffer<cr>

Toggle paste mode on and off:
	
	map <leader>pp :setlocal paste!<cr>


### Visual mode mappings

Visual mode pressing `*` or `#` searches for the current selection:

	vnoremap <silent> * :call VisualSelection('f')<CR>
	vnoremap <silent> # :call VisualSelection('b')<CR>

When you press gv you `Ack.vim` after the selected text:

	vnoremap <silent> gv :call VisualSelection('gv', '')<CR>

When you press `<leader>r` you can search and replace the selected text:

	vnoremap <silent> <leader>r :call VisualSelection('replace')<CR>

Surround the visual selection in parenthesis/brackets/etc.:

    vnoremap $1 <esc>`>a)<esc>`<i(<esc>
    vnoremap $2 <esc>`>a]<esc>`<i[<esc>
    vnoremap $3 <esc>`>a}<esc>`<i{<esc>
    vnoremap $$ <esc>`>a"<esc>`<i"<esc>
    vnoremap $q <esc>`>a'<esc>`<i'<esc>
    vnoremap $e <esc>`>a"<esc>`<i"<esc>


### Insert mode mappings

Quickly insert parenthesis/brackets/etc.:

    inoremap $1 ()<esc>i
    inoremap $2 []<esc>i
    inoremap $3 {}<esc>i
    inoremap $4 {<esc>o}<esc>O
    inoremap $q ''<esc>i
    inoremap $e ""<esc>i
    inoremap $t <><esc>i

Insert the current date and time (useful for timestamps):

    iab xdate <c-r>=strftime("%d/%m/%y %H:%M:%S")<cr>


### Command line mappings

$q is super useful when browsing on the command line. It deletes everything until the last slash:

    cno $q <C-\>eDeleteTillSlash()<cr>

Bash like keys for the command line:

    cnoremap <C-A>		<Home>
    cnoremap <C-E>		<End>
    cnoremap <C-K>		<C-U>

    cnoremap <C-P> <Up>
    cnoremap <C-N> <Down>

Write the file as sudo (works only on Unix). Super useful when you open a file and you don't have permissions to save your changes. [Vim tip](http://vim.wikia.com/wiki/Su-write):

    :W 


### Spell checking
Pressing `<leader>ss` will toggle spell checking:

    map <leader>ss :setlocal spell!<cr>

Shortcuts using `<leader>` instead of special characters:

    map <leader>sn ]s
    map <leader>sp [s
    map <leader>sa zg
    map <leader>s? z=


### Cope
Query `:help cope` if you are unsure what cope is. It's super useful!

When you search with `Ack.vim`, display your results in cope by doing:
`<leader>cc`

To go to the next search result do:
`<leader>n`

To go to the previous search results do:
`<leader>p`

Cope mappings:

    map <leader>cc :botright cope<cr>
    map <leader>co ggVGy:tabnew<cr>:set syntax=qf<cr>pgg
    map <leader>n :cn<cr>
    map <leader>p :cp<cr>
