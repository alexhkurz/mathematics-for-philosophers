# mathematics-for-philosophers

(under construction)

## mathematics for philosophers

This is the repo in which I, a mathematician, keep my notes on ongoing discussions with an undergraduate philosophy student, Johanna Speiser.

The notes are written together while discussing the topic. Unfortunately, the notes do not show the discussions as they happened and do not contain much information about the teaching and learning. Rather the notes are the frozen outcome of the learning process. Their main purpose is to remind the authors of the work we have done and help motivating us to add more in the future.

## how to create this jupyter book

### basics

After cloning this repo, and installing jupyter-book run from the command line

`jupyter-book build .` or `jb build .`

The book can now be opened in a browser by opening the file `_build/html/index.html`. On a mac, simply run `open _build/html/index.html`. To summarize

```
jb build . ; open _build/html/index.html
```

### publishing

(There is sth missing here.) After installing `ghp-import` with
`pip install ghp-import` publish the book by running 

````
ghp-import -n -p -f _build/html
```

This makes the [book available online](https://alexhkurz.github.io/mathematics-for-philosophers). It also keeps the source files in the `main`-branch separate from the files in `_build` in the `gh-pages` branch.

### important commands

If, for example, the table of contents in the left-hand pane behaves in a strange way, clean out `_build` by running `jupyter-book clean .`

### references

[Create your first book](https://jupyterbook.org/en/stable/start/your-first-book.html).

[Math and equations](https://jupyterbook.org/en/stable/content/math.html#math-and-equations).

[.gitignore](https://raw.githubusercontent.com/executablebooks/jupyter-book/master/.gitignore).

[Publish your book online](https://jupyterbook.org/en/stable/start/publish.html).

