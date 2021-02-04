# RDictCc

RDictCc is a simple translation tool written in Ruby that creates a local
database out of the dictionary files from [dict.cc](http://www.dict.cc).

## Usage

Simply place the file `rdictcc.rb` somewhere in your `PATH`.  Executing
`rdictcc.rb --help` will show you all that's needed.

```
Usage: rdictcc.rb [database_import_options]
       rdictcc.rb [misc_options]
       rdictcc.rb [query_option] QUERY
       rdictcc.rb

If no option nor QUERY is given, you'll enter rdictcc's interactive mode.

Database building options:
    -i, --import DICTCC_FILE         Import the dict file from dict.cc

Misc options:
    -v, --version                    Show rdictcc.rb's version
    -S, --size                       Show the number of entries in the databases
    -d, --directory PATH             Use PATH instead of ~/.rdictcc/
    -h, --help                       Show this message

Format options:
    -c, --compact                    Use compact output format

Query option:
    -s, --simple                     Translate the word given as QUERY (default)
    -r, --regexp                     Translate all words matching the regexp QUERY
    -f, --fulltext                   Translate all sentences matching the regexp QUERY
```

To make use of the Emacs interface, add this to your `~/.emacs`.

```
;; Adapt path as you need
(add-to-list 'load-path "~/path/to/rdictcc")
(setq rdictcc-program "~/path/to/rdictcc/rdictcc.rb")

(require 'rdictcc)
;; Adapt to your likings
(global-set-key (kbd "C-c t") 'rdictcc-translate-word-at-point)
(global-set-key (kbd "C-c T") 'rdictcc-translate-word)

```

Have fun!

## Bugs

Bugs can be reported at [here](https://todo.sr.ht/~tsdh/rdictcc).

## License

Distributed under the [General Public License, Version 3 or
later](https://www.gnu.org/licenses/gpl-3.0.en.html).
