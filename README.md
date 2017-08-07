# hvlines - draw horizontal and vertical lines


## Overview

A small [PGFPlots](https://ctan.org/pkg/pgfplots) library to draw horizontal and vertical lines.

## Installation and loading

Place tikzlibrarypgfplots.hvlines.code.tex in a directory read by your TeX compiler. 
Load it through 
```latex
\usetikzlibrary{calc} % required
\usepgfplotslibrary{hvlines}
```

## Licence

[Gnu General Public version, 3](https://ctan.org/license/gpl3), as for [PGFPlots](https://ctan.org/pkg/pgfplots).

## Motivation and usage

Two keys, `vertical line` and `horizontal line` are defined that could be called
in the options of axis. They took key-values with key `at` for the position and
`style` for the style of the line.

The lines are plotted before the `addplot` through the `execute at begin axis`.

*Example*
```latex
 \begin{axis}[vertical line={at=2.5,style={blue}},horizontal line={at=1.5,style={dashed,->}}]
     \addplot table {
 	    1	1
 	    2	2
 	3	3.5};
 \end{axis}
```


For an alternative possibility, see this [Stack Exchange question](https://tex.stackexchange.com/questions/240642/add-vertical-line-of-equation-x-2-and-shade-a-region-in-graph-by-pgfplots)

## Note

This is an experimental, alpha release, designed first for personnal use.

## TODO

* Add commands for defining nodes. 
* Dealing with missing value `at`.

