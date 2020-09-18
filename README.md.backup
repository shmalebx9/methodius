# Methodius Markdown to PDF script
Methodius is a wrapper for pandoc and url2cite with a sane default template. PDFs generated with this wrapper will be formatted to the default template provided (Methodius) with citations formatted to the default CSL (Chicago-note).

The default template is a badly edited version of [eisvogel](https://github.com/Wandmalfarbe/pandoc-latex-template). The original eisvogol template can be used with the `-t` flag.

## Installation & usage
Make sure the methodius script is executeable then try running with the `-b` flag. The bootstrap process will install the templates and attempt to aquire the necessary tools. The bootstrapper should be considered incomplete, so manual installation of the required tools is preffered after the templates have been bootstrapped.

To use the wrapper run it from your git repo directory or add it to your `$PATH`

Simply supply the script with a markdown file and optionally CSL/template files.

Example:

	methodius test.md
	
or:
	
	methodius test.md -t mytemplate -c path/to/my/CSL.csl
## Required tools
* [url2cite](https://github.com/phiresky/pandoc-url2cite) for citations
* [pandoc](https://pandoc.org/)
* [tectonic](https://tectonic-typesetting.github.io/en-US/) as a pdf engine
* A functioning Texlive installation (Check your distro's docs)

The bootstrap function in the script will attempt to install these tools. The bootstrapper is configured  for void and will not work properly on other distros.

# Credits
Eisvogel latex template from [Pascal Wagler and John MacFarlane](https://github.com/Wandmalfarbe/pandoc-latex-template)

[url2cite](https://github.com/phiresky/pandoc-url2cite) by phiresky

Chicago-note CSL from [Zotero](https://www.zotero.org/)