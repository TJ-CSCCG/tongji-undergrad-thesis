# Tongji University Undergraduate Thesis Template

## Overview

`tongjithesis` is a LaTeX class for creating undergraduate theses that comply with the official requirements of Tongji University, China. This template is designed to help students focus on content creation rather than formatting details.

## Features

- Compliant with Tongji University's official undergraduate thesis requirements
- Support for both one-sided and two-sided printing
- Comprehensive formatting for title page, abstract, table of contents, chapters, etc.
- Customized citation styles that comply with Chinese GB/T 7714-2015 standard
- Support for code listings with syntax highlighting
- Integration of mathematical formulas, figures, tables, and algorithms

## Requirements

- A complete TeX distribution (TeXLive, MikTeX, or MacTeX)
- XeLaTeX or LuaLaTeX engine (the template doesn't support pdfLaTeX)
- Python with Pygments installed (for code syntax highlighting via `minted`)

## Installation

1. **Manual Installation**: 
   - Copy `tongjithesis.cls` and `tongjithesis.cfg` to your project directory, or
   - Install to your local texmf tree (recommended)
   
2. **Install to TEXMF tree**:
   - For TeX Live on Unix-like systems: `~/texmf/tex/latex/tongjithesis/`
   - For MiKTeX on Windows: `%USERPROFILE%\texmf\tex\latex\tongjithesis`
   - For MacTeX: `~/Library/texmf/tex/latex/tongjithesis/`

## Basic Usage

```latex
\documentclass[oneside]{tongjithesis}  % Use 'twoside' for double-sided printing

% Set thesis information
\school{计算机科学与技术学院}
\major{计算机科学与技术}
\student{1234567}{张三}
\thesistitle{基于机器学习的图像分类研究}{——以交通标志识别为例}
\thesistitleeng{Research on Image Classification Based on Machine Learning}{——Take Traffic Sign Recognition as an Example}
\thesisadvisor{李四 教授}
\thesisdate{2025}{4}{20}

\begin{document}

% Generate cover
\MakeCover

% Abstract pages
\pagestyle{firststyle}
\input{sections/abstract}

% Table of contents
\clearpage
\tableofcontents
\cleardoublepage

% Main content with page style
\pagestyle{mainstyle}
\input{sections/introduction}
% ... more sections ...

% References
\printbibliography[heading=bibintoc,title=参考文献]

% Acknowledgements
\clearpage
\input{sections/acknowledgements}

\end{document}
```

## Documentation

For detailed documentation, please refer to the user guide (tongjithesis-guide.pdf).

## License

This template is licensed under the LaTeX Project Public License (LPPL) version 1.3c or later.

## Maintainer

Current Maintainer: R. Lin

## Acknowledgements

- This project is maintained by the TJ-CSCCG (Tongji University Computer Science Curricula Collection Group)
- Original author: YukuanHU
- Contributors: ganler, skyleaworlder, RizhongLin

## Reporting Issues

Please report any issues or feature requests through the GitHub repository:
https://github.com/TJ-CSCCG/tongji-undergrad-thesis
