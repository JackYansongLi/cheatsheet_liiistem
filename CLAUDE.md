# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a LaTeX project that generates a keyboard shortcuts cheatsheet for the Liii STEM editor (https://liiistem.cn/). The cheatsheet documents keyboard shortcuts and their equivalent LaTeX commands for mathematical notation.

## Project Structure

- `main.tex` - Main LaTeX document that includes all sections
- `preamble.tex` - LaTeX preamble with package imports, custom commands, and styling
- `docs/` - Directory containing individual LaTeX files for different mathematical categories:
  - `Common_constructs.tex` - Basic math constructs (superscripts, subscripts, fractions, roots)
  - `Font.tex` - Font styles and mathematical alphabets
  - `greek.tex` - Greek letters
  - `Sets_and_logic.tex` - Set theory and logical symbols
  - `Decorations.tex` - Mathematical decorations
  - `Dots.tex` - Ellipsis and dot notations
  - `Other_symbles.tex` - Miscellaneous symbols
  - `Variable_sized_operators.tex` - Operators that scale with content
  - `Arrow.tex` - Arrow symbols
  - `Fences.tex` - Brackets and delimiters
  - `env_cut.tex` - Environment shortcuts

## Build Commands

To compile the LaTeX document to PDF:

```bash
pdflatex main.tex
```

Or use latexmk for automatic compilation:

```bash
latexmk -pdf main.tex
```

To clean auxiliary files:

```bash
latexmk -c
```

## Key LaTeX Packages Used

- `geometry` - Page layout and margins
- `xcolor` - Color support
- `pgfpages` - Multiple pages per sheet layout
- `fontawesome5` - Icon fonts
- `booktabs`, `makecell`, `xltabular` - Advanced table formatting
- `menukeys` - Professional keyboard shortcut display
- `hyperref` - Hyperlinks
- `amsmath`, `amssymb`, `amsfonts`, `amsthm` - Advanced math typesetting

## Document Format

The cheatsheet uses a three-column table format:
- Column 1: Windows/Linux shortcuts
- Column 2: Mac shortcuts
- Column 3: Equivalent LaTeX commands

Each section is organized by mathematical category and uses custom commands like `\inputrow` for consistent formatting.

## Development Notes

- The document is configured for A4 paper with 1cm margins
- Uses a 2-on-1 layout (two pages per sheet) in landscape orientation
- Fonts: Fira Sans for text, Latin Modern for math
- Custom keyboard shortcut styling with platform-specific formatting
- All LaTeX commands mentioned work in the Liii STEM editor