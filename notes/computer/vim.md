<!-- njnmdoc:  title="Vim"  -->


#Vim Cheat Sheet

##Modes

* Normal mode
* Insert mode
* Visual mode

##Navigation

```
  hjkl  		:: left down up right

  wbe   		:: next/prev word

  }     		:: next chunk
  {     		:: prev chunk


  g##   		:: Go to line ##
  gg    		:: Go to line 1
  GG    		:: Go to last line

  /     		:: search
  n     		:: next match
  N     		:: prev match
```

##Commands

```
  =     		:: Indent object

  dd            :: delete line (cut)
  yy            :: yank line   (copy)
  p             :: paste

  :e    		:: edit
  :q    		:: quit
  :w    		:: write out

  :diffsplit    :: view a diff
  :diffpatch    :: view a patch (as a diff)
```

##Spelling

```
  :set spell    :: Turn on
  :set nospell  :: Turn off

  zg            :: Add word to list (good)
  zw            :: Add word to list (wrong)
  z=            :: Suggest a word       *CTRL-X*
```

##Buffers

Buffers are

```
  :ls       	:: List open buffers
  :b#       	:: Open buffer #
  :bd       	:: Delete buffer
  :bn       	:: Next buffer
  :bp       	:: Previous buffer
```
                :: Switch to last       *CTRL-6*

###How to read ls

```

| Code | Meaning                  |
|------|--------------------------|
| %    | current window           |
| #    | alternate window for C-^ |
| a    | active buffer            |
| h    | hidden buffer            |
| -    | modifiable off           |
| =    | readonly                 |
| +    | modified                 |
| x    | read errors              |
```


##Windows

Windows split the screen into regions

```
  :sp       	:: Split window         *CTRL-w s*
  :vs       	:: Vertical split       *CTRL-w v*
  :clo      	:: Close current win    *CTRL-w c*
  :q            :: Quit current window  *CTRL-w q*
  :on       	:: Make current only    *CTRL-w o*

  :res          :: Resize +-N height    *CTRL-w +/-*
  :vertical res :: Resize +-N width     *CTRL-w </>*
                :: Equal size all win   *CTRL-w =*
                :: Rotate windows       *CTRL-w r*
```

##Tabs

Tabs contain windows.

```
  :tabs     	:: List tabs
  :tabe     	:: Edit in new tab
  :tabc     	:: Close current tab

  :tabn     	:: Next tab             *CTRL-PgDn*
  :tabp     	:: Prev tab             *CTRL-PgUp*

```

##Folding

```
  zo            :: Open one fold
  zc            :: Close one fold

  zO            :: Open all nested folds
  zC            :: Close all nested folds
```

##Screen

```
  :ScreenShell  :: Starts a shell below
  :ScreenQuit   :: Closes it
  :ScreenSend   :: Sends a selection to the ScreenShell
%% todo: bind to keys
```

##File Manager
```
  :e.   :: Look at current dir
  :Ve.  :: Look at current in side panel
```

##Version Control
```
  \ca 			:: Add current file
  \cb 			:: Annotate
  \cc 			:: Commit
  \cd 			:: Diff
  \cs 			:: Status
```

## VimWiki

```
 =              :: adds a header level to this line
 -              :: remove a header level

  zr            :: unfold next level (vimwiki)
  zM            :: fold all (vimwiki)
```

## Misc Knowledge

How to get vim to open multiple files into tabs at once?

```
:args *.c
:tab all
```

http://superuser.com/questions/171763/how-to-get-vim-to-open-multiple-files-into-tabs-at-once


##Links
  * http://arstechnica.com/information-technology/2011/11/two-decades-of-productivity-vims-20th-anniversary/
