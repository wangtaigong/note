### ch01

- vim命令

  `vim `

- 退出vim

  `:quit :q` 

- 保存文件

  `:write :w`

  保存并命名 `:w file.txt`

  保存并退出 `:wq`

  强制退出`:q!`

- 帮助

  `:h  :h write-quit`

- 打开文件

  `vim hello.txt`

  打开多个文件

  `vim hello.txt hello2.txt`

- 参数

  传标记和选项给vim

  `vim --version`

  +语法 或者 -c

  `vim +%s/a/b/g hello.txt`

  `vim -c %s/a/b/g hello.txt`

- 打开多窗口

  打开水平多窗口

  `vim -02`

  打开垂直多窗口

  `vim -O2`

  `vim -O5 hello.txt hello2.txt`

- 暂停编辑

  `Ctrl + z   :stop :suspend`

  恢复

  `fg`

- 智能打开vim



### ch02 

buffers, windows, tabs

- buffers

  What is a *buffer*?

  A buffer is an in-memory space where you can write and edit some text. When you open a file in Vim, the data is bound to a buffer. When you open 3 files in Vim, you have 3 buffers.

  `:bnext :buffer + filename :buffer + n :bdelete :buffers`

  退出vim

  By the way, if you have multiple buffers opened, you can close all of them with quit-all:

  `:qall :qall! :wqall`

- windows

  `:split filename :vsplit filename`

  ```
  Ctrl-W H    Moves the cursor to the left window
  Ctrl-W J    Moves the cursor to the window below
  Ctrl-W K    Moves the cursor to the window upper
  Ctrl-W L    Moves the cursor to the right window
  ```

  Here are some useful normal-mode window commands:

  ```
  Ctrl-W V    Opens a new vertical split
  Ctrl-W S    Opens a new horizontal split
  Ctrl-W C    Closes a window
  Ctrl-W O    Makes the current window the only one on screen and closes other windows
  ```

  And here is a list of useful window command-line commands:

  ```
  :vsplit filename    Split window vertically
  :split filename     Split window horizontally
  :new filename       Create new window
  ```

- tabs

  ```
  :tabnew file.txt    Open file.txt in a new tab
  :tabclose           Close the current tab
  :tabnext            Go to next tab
  :tabprevious        Go to previous tab
  :tablast            Go to last tab
  :tabfirst           Go to first tab
  ```

  To start Vim with multiple tabs, you can do this from the terminal:

  ```
  vim -p file1.js file2.js file3.js
  ```

- 移动

  左右上下移动， z轴移动（：buffer）