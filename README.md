# Bulkrename 
* This script provides a command line tool 
that can called through the command `bulkrename`.
* This tool allows you to refactor files, similar 
to how the `bulkrename` command works in the file 
manager [ranger](https://github.com/ranger/ranger).
* By default, `bulkrename` will list all of the files
in the current directory in a vim buffer, and allow you
to interactively rename these files, by simply changing 
the file names in the vim buffer.
* This tool also comes with options for recursively 
renaming files and directories across the directory path
that is passed in.

## Requirements
* python 3.6
* python module: click
* This script should run appropriately on MacOS/Linux/Windows systems, but
the script has not been tested on Windows.

If the click module is not already downloaded in your environment, 
the installation command will download it for you. 

## Installation
Download command:
```
git clone https://github.com/Jim-Shaddix/bulkrename.git
```
Install command:
```
pip install --editable .
```

## Usage
```
bulkrename --help

Usage: bulkrename [OPTIONS] [PATH]

  Refactors all of file names in the provided directory. By default,
  refactoring is done on the current directory, and is only done on non-dot
  files.

Options:
  -f, --files             [Default = True]  refactor files.
  -dotf, --dot-files      refactor dot files.
  -d, --directories       refactor directories.
  -dotd, --dot-direc      refactor dot directories.
  -r, --recursive         recursively refactor through directories.
  -dotr, --recursive-dot  recursively refactor through dot directories.
  -v, --verbose           Display what each relative file path was changed to.
  -dr, --dry-run          Display what each file path will be changed to,
                          without performing the changes.
  --help                  Show this message and exit.
```

Below is a simple example of how the script works without any arguments.

![example](bulkrename.gif)
