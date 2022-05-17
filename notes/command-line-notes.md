[[home.md]]

- navigation MOVING

      e  ^E  j  ^N  CR  *  Forward  one line   (or N lines).
      y  ^Y  k  ^K  ^P  *  Backward one line   (or N lines).
      f  ^F  ^V  SPACE  *  Forward  one window (or N lines).
      b  ^B  ESC-v      *  Backward one window (or N lines).
      z                 *  Forward  one window (and set window to N).
      w                 *  Backward one window (and set window to N).
      ESC-SPACE         *  Forward  one window, but don't stop at end-of-file.
      d  ^D             *  Forward  one half-window (and set half-window to N).
      u  ^U             *  Backward one half-window (and set half-window to N).
      ESC-)  RightArrow *  Right one half screen width (or N positions).
      ESC-(  LeftArrow  *  Left  one half screen width (or N positions).
      ESC-}  ^RightArrow   Right to last column displayed.
      ESC-{  ^LeftArrow    Left  to first column.
      F                    Forward forever; like "tail -f".
      ESC-F                Like F but stop when search pattern is found.
      r  ^R  ^L            Repaint screen.
      R                    Repaint screen, discarding buffered input.

- `whoami` prints current users name

- `man <comman>` opens manual page for that command. press `h` to open summary of less commands.

- `echo <file.type> > "line 1"` creates a file and adds a line. Good for quickly creating a basic file, or adding a line to an existing one.

  - `echo <filme.type> >> "line 2"` to add additional line

- `rmdir <directory>` to delete empty directories
- `rm <file>` to delete individual files
  - `rm <file1> <file2> <file3>` to remove multiple files
- `rm -r <directory>` to delete directories and all contents.
- `rm -v` 'remove verbose' prints what was deleted

        ╭─tim@LAPTOP-7RMVA9J2 ~/test
        ╰─$ rm -v cat dog purr woof
        removed 'cat'
        removed 'dog'
        removed 'purr'
        removed 'woof'

- `rm -ri directory/` interactive mode. It will ask `descend into directory 'aquarium/'?` answer `y/n` takes you into the directory and asks for confirmation to delete each file

        ╭─tim@LAPTOP-7RMVA9J2 ~/test
        ╰─$ rm -ri aquarium/
        rm: descend into directory 'aquarium/'? y
        rm: remove regular empty file 'aquarium/turtle'? y
        rm: remove regular empty file 'aquarium/fish'? y
        rm: remove regular empty file 'aquarium/seal'? y
        rm: remove directory 'aquarium/'? y
