# thesis-template

You’re a graduate student preparing to write your thesis or dissertation. You'd like to start writing up your amazing research results, but first there's the small matter of your university's style requirements.

This project provides LaTeX classes that do most of that formatting work for you. It is intended to be easy to use and easy to maintain, so you don't have to be a TeX genius to make those small changes your supervisor asks for.

This project is primarily aimed at graduate students at Simon Fraser University. If you go to the University of Victoria, you might want to check out a [different template][uvic] based on my master's thesis there.


## System Requirements

You will need a relatively recent LaTeX distribution. In particular, the SFU template depends on the following (standard) packages:

- `appendix` to add the word "Appendix" to the Table of Contents
- `etoolbox` for class options
- `geometry` to set margins
- `lmodern` and `fontenc` for extended fonts
- `nowidow` to prevent nearly-empty pages
- `pdfpages` to include Declaration of Partial Copyright Licence form
- `setspace` for line spacing
- `tocloft` to make the ToC nicer

If you do not have these installed, you can easily get them using the package manager that came with your distribution (`tlmgr` in TeX Live or its GUI frontend `TeX Live Utility` on OS X; `mpm` on Windows MikTeX installations).


## Installation

1. [Download all of the project's files][download] and move the files appropriate to your university to the (same) folder of your choice.

2. Rename `template.tex` to something more suitable, like `thesis.tex`. Delete the placeholder information and replace it with your own.

3. Compile it with your favourite [LaTeX editor][editors] or from the command line using [`latexmk`][latexmk]:

```
latexmk -pdf thesis.tex
```


## Contributing

If you find you have to make any changes to these templates, either because it doesn't compile on your system or because your university's requirements have changed, please email me at `rchurchl@sfu.ca` so other people can benefit.

If you have a GitHub account, you can [open an issue][newissue] to report a bug or suggest an enhancement.


## Changelog

**6 Feb 2015:** Many bugfixes and improvements, but also a few compatibility-breaking changes:

- All font class options except for `serif` are removed. Users may now safely change fonts to their hearts' content in their own preamble.
- `\committee` now only takes one argument. Users who need to change the committee type from "Examining Committee" to "Supervisory Committee" may now use the `undefended` class option.
- `\defended` and `\approved` are removed. Users should now set the date of defence or approval with `\date` and use the `undefended` class option if applicable.
- Users are now required to download their own copy of the Declaration of Partial Copyright License form, in case it changes in the future.

[uvic]: https://github.com/rchurchley/uvic-thesis
[download]: https://github.com/rchurchley/thesis-template/archive/master.zip
[editors]: http://en.wikipedia.org/wiki/Comparison_of_TeX_editors
[newissue]: https://github.com/rchurchley/thesis-template/issues/new
[latexmk]: http://ctan.math.ca/tex-archive/support/latexmk/latexmk.pdf
