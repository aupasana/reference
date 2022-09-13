# Ebooks

The following zsh function converts an ebook from one format to another.
eg. epub2 in.epub pdf,txt

Prerequisites: Install calibre via brew

```zsh
function epub2() {
    # #2 is a comma separated list of output types. 
    # eg. pdf,txt
    second_arg=$2
    output_types=(${(@s:,:)second_arg})

    echo Converting to $output_types

    for i in $output_types; do
        base=$1:r
        echo Converting $1 to $base.$i
        ebook-convert $1 $base.$i
    done
}
```

Format a file, wrapping lines at 80 characters, breaking on spaces

```zsh
function txt-fold {
    fold -w 80 -s $1
}
```
