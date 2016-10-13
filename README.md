# LaTeX Style Files

This is a collection of useful LaTeX style sheets that I use for my courses.

## Installation

By following one of the following method, you will be able to use the package files by using the standard `LaTeX` commands such as `\usepackage` or `\documentclass`.

### Local Installation

You can use these files by simply putting the `*.sty` or `.cls` files in the same folder as your main `LaTeX` file.

### Global Installation

You can also install the `*.sty` or `*.cls` files in your `LaTeX` home folder. You can find the path of this folder by running the following command:

```bash
kpsewhich -var-value=TEXMFHOME
```

Then, you will have to create the folder `tex/latex` inside the folder returned by the previous command. You can then copy or symlink the package files to this directory.

**Note:** If this command did not work, check this [link](http://tex.stackexchange.com/questions/1137/where-do-i-place-my-own-sty-or-cls-files-to-make-them-available-to-all-my-te/1167#1167) for more help.

## License

MIT License. See [LICENSE](LICENSE).
