# Methodius Markdown to PDF script
Methodius is a wrapper for pandoc and url2cite with a sane default template. PDFs generated with this wrapper will be formatted to the default template provided (Methodius) with citations formatted to the default CSL (Chicago-note).

The default template is a badly edited version of [eisvogel](https://github.com/Wandmalfarbe/pandoc-latex-template). The original eisvogol template can be used with the `-t` flag. The project also includes my case brief template (case) and my notes template (cupertino).

| Cupertino |
:----------:|
![](https://github.com/shmalebx9/methodius/blob/assets/examples/cupertino.png)|

Methodius                   | Case                   |
:--------------------------:|:----------------------:|
![](https://github.com/shmalebx9/methodius/blob/assets/examples/methodius.png) | ![](https://github.com/shmalebx9/methodius/blob/assets/examples/case.png) |

## Installation & usage
Make sure the methodius script is executable then try running with the `-b` flag. The bootstrap process will install the templates and attempt to acquire the necessary tools. The bootstrapper should be considered incomplete, so manual installation of the required tools is preferred after the templates have been bootstrapped. The url2cite filter is not currently compatible with pandoc 2.10+. If you face citation issues try verifying your pandoc version is 2.9x or below.

To use the wrapper run it from your git repo directory or add it to your `$PATH`

Simply supply the script with a markdown file and optionally CSL/template files.

Example:

	methodius test.md
	
or:
	
	methodius test.md -t mytemplate -c path/to/my/CSL.csl

For mermaid charts you must include `format=pdf loc=mermaid-images` in your codeblock and pass the `-m` option. For example:

	~~~{.mermaid format=pdf loc=mermaid-images}
	graph TB
	A[No Basic Fact]
	B[Basic Fact]
	C[Permissive]
	D[Mandatory]
	E[Conclusive]
	F[Rebuttable]
	G[Balance of Probabilities]
	H[Evidence to the contrary]
	I[Presumptions]
	I --> A
	I --> B
	B --> C
	B --> D
	C --> E
	C --> F
	F --> G
	F --> H
	~~~

Will render as: 

![](https://github.com/shmalebx9/methodius/blob/assets/examples/mermaid-example.png)

## Required tools
* [url2cite](https://github.com/phiresky/pandoc-url2cite) for citations
* [pandoc](https://pandoc.org/)
* [tectonic](https://tectonic-typesetting.github.io/en-US/) as a pdf engine
+ [mermaid-filter](https://github.com/raghur/mermaid-filter)
* A functioning Texlive installation (Check your distro's docs)
+ Optionally: librsvg-utils for mermaid

The bootstrap function in the script will attempt to install these tools. The bootstrapper is configured  for void and will not work properly on other distros.

# Credits

Eisvogel latex template from [Pascal Wagler and John MacFarlane](https://github.com/Wandmalfarbe/pandoc-latex-template)

[Sofadesign](https://github.com/sofadesign) latex template

[url2cite](https://github.com/phiresky/pandoc-url2cite) by phiresky

Chicago-note CSL from [Zotero](https://www.zotero.org/)

[mermaid-filter](https://github.com/raghur/mermaid-filter) by raghur