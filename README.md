# shellcheck
64-bit build of shellcheck, the Haskell-based shell script checker, on windows 10.

Source project: https://github.com/koalaman/shellcheck


```bash
$ shellcheck -V
ShellCheck - shell script analysis tool
version: 0.4.7
license: GNU General Public License, version 3
website: http://www.shellcheck.net

$ file ./shellcheck.exe
./shellcheck.exe: PE32+ executable (console) x86-64 (stripped to external PDB), for MS Windows

```

Rough outline of build steps in Windows 10

1. Get MSYS2
2. Run `Mingw-w64 64bit`
3. Get `python3` and `pip` via pacman
4. Get `cabal` via pip
5. `cabal update`
 _(I had to restart MSYS2 at some point when python got confused)_
6. `cabal install ShellCheck`

The binary was created in `/c/Users/$USER/AppData/Roaming/cabal/bin/shellcheck.exe`
