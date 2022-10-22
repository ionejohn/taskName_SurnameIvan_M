On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Readme.txt
        index.html
        styles.css

nothing added to commit but untracked files present (use "git add" to track)

2e
info
pack
usage: git cat-file <type> <object>
   or: git cat-file (-e | -p) <object>
   or: git cat-file (-t | -s) [--allow-unknown-type] <object>
   or: git cat-file (--batch | --batch-check | --batch-command) [--batch-all-objects]
                    [--buffer] [--follow-symlinks] [--unordered]
                    [--textconv | --filters]
   or: git cat-file (--textconv | --filters)
                    [<rev>:<path|tree-ish> | --path=<path|tree-ish> <rev>]

Check object existence or emit object contents
    -e                    check if <object> exists
    -p                    pretty-print <object> content

Emit [broken] object attributes
    -t                    show object type (one of 'blob', 'tree', 'commit', 'tag', ...)
    -s                    show object size
    --allow-unknown-type  allow -s and -t to work with broken/corrupt objects
    --use-mailmap         use mail map file
    --mailmap ...         alias of --use-mailmap

Batch objects requested on stdin (or --batch-all-objects)
    --batch[=<format>]    show full <object> or <rev> contents
    --batch-check[=<format>]
                          like --batch, but don't emit <contents>
    -z                    stdin is NUL-terminated
    --batch-command[=<format>]
                          read commands from stdin
    --batch-all-objects   with --batch[-check]: ignores stdin, batches all known objects

Change or optimize batch output
    --buffer              buffer --batch output
    --follow-symlinks     follow in-tree symlinks
    --unordered           do not order objects before emitting them

Emit object (blob or tree) with conversion or filter (stand-alone, or with batch)
    --textconv            run textconv on object's content
    --filters             run filters on object's content
    --path blob|tree      use a <path> for (--textconv | --filters); Not with 'batch'