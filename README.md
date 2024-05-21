# Open Source PyMOL for macOS

Open source [PyMOL](https://pymol.org) is available free of charge and may be installed via the [Homebrew](https://brew.sh/) package manager.

This repository provides a method to install PyMOL v2.6 on macOS. If necessary, a portuguese version of this guide is available [here](https://github.com/cnpem/PyMOL4macOS/blob/main/README_PT.md).

## Download & Installation

Follow these steps to install PyMOL v2.6:

1. Install [Homebrew](https://brew.sh/):

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

2. Install PyMOL dependencies (python, xquartz, tcl-tk, Qt5) using Homebrew:

```bash
brew install Caskroom/cask/xquartz
brew install tcl-tk
brew install python
pip install pyqt5
```

3. Install PyMOL

```bash
brew install brewsci/bio/pymol
```

4. Create an application executable for PyMOL:

- Open Automator, which is in Applications in macOS.
- Create new document, select “Application”.
- Select “Actions” and “Library” in the left pane. Select “Utilities” and “Run Shell Script”. Drag this into the main pane.
- Choose “/bin/bash” as a shell.
- Paste the following: `/usr/local/bin/pymol -M`. If this doesn’t work, check the path to PyMOL using `which pymol` in the terminal, and use this instead.
- Save the application (“File > Save”) to the Desktop and name it “PyMOL”.

5. Launch PyMOL v2.6

In the terminal, run:

```bash
pymol
```

or, you can start PyMOL by double clicking the created application in the desktop.
