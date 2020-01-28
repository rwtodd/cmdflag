# cmdflag

## DOS/cmd.exe-style flags

This is a drop-in replacement for the standard Go "flag" package, except
it parses flags in the style of cmd.exe/DOS commands.  In particular:

 * Flags start with '/'
 * Flags with an argument can be given as: `/flag arg` or `/flag:arg`
 * The 'help' arg is `/?`
 * You don't have to put a space between flags (and on cmd.exe, you don't even
need a space between the command name and the first flag).  The following are all
equivalent:
   * `myprog.exe/p/wd:40/xx`
   * `myprog.exe /p /wd:40 /xx`
   * `myprog.exe /p /wd 40 /xx`

## Licensing

This is a small modification of the Go 1.13 stdlib package, so I left the original
copyright in the file, and used the same license file from the Go distribution.

