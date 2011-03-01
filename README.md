monkey.tmbundle
===============

This bundle lets you to use the Mac OS X editor TextMate as an IDE for the monkey programming language. It is based in part on the existing [blitzmax.bundle](https://github.com/nilium/blitzmax.tmbundle) so thanks to Nilium for that.


## Features

**Auto Completion of Keywords**  
Press the Escape key to cycle through all matches after typing part of a keyword

**Expand Keywords into Code**  
Press the tab key to expand one keyword into one or more lines of code, subsequent presses of tab intelligently jump you through the resulting code allowing you to fill in multiple parameters with minimal key strokes

**Build options**  
Specify target, config and run options in the source - no need for the command line

**Build hotkey**  
Quick and easy build by pressing Command+B

**Context Sensitive Help**  
View the monkey module docs in a popup window

**Quick Start Template**  
One click skeleton template to get you started, build to see instant results

**Syntax Colouring**, **Code Folding** ...and more!

## Installation

To use unzip and double click, or manually move the bundle to:  
`/Users/username/Library/Application Support/TextMate/Bundles/monkey.tmbundle`


## Usage

### Setup

Before you can use the _monkey_ bundle, you must first set the `TM_MONKEY` shell variable.

To do this, open TextMate's preferences (⌘,) and navigate to the _Advanced_ pane.  Select the _Shell Variables_ tab and add the TM\_MONKEY variable, where its value is the location of your _monkey_ installation.  For example, "/Developer/Applications/monkey".  Do not include a trailing slash in the path.

This variable allows you to build your applications (⌘B). Documentation and trans lookups are relative to this location.

### Using Projects

When using projects, you can set the `TM_MONKEY_MAIN_FILE` shell variable for your project and specify the main _monkey_ file to build when you use the Build App (⌘B) command.

To set this variable, open the project drawer and deselect any files, then click the "i" button at the bottom of the drawer to open the project info.  Add the `TM_MONKEY_MAIN_FILE` variable, and set its value to the file relative to the main file project's directory.

### Build Options

When using the Build App and Run App commands, your main source file (either the file you have open or the one specified by `TM_MONKEY_MAIN_FILE`) is quickly scanned for a set of build options to determine how to build and/or run the results.  These build options are available under the Build Options snippets, and are as follows:

- **Release & Debug** - `debug`, `release`  
Specifies whether or not to compile the program in debug mode.
- **Target** - `html5`, `flash`, `xna`, `android`, `ios`, `glfw`, `stdcpp`  
Specifies what type of target to produce. Only targets that are installed correctly on your machine will be available.
- **Run After Build** - `run`  
Executes the resulting output immediately after building it.

Build options are formatted as comments inside your source code and do not have any meaning outside of this bundle.  They are written as:

   `' buildopt: option`

where 'option' is the option you're enabling for the Build & Run commands.  The comments must be on their own lines with only whitespace preceeding them.

## License

monkey.tmundle is made available under a [Creative Commons Attribution-Share Alike 3.0 Unported License](http://creativecommons.org/licenses/by-sa/3.0).

## Support
You can talk about the bundle on the [official monkey forum](http://www.monkeycoder.co.nz/Community/posts.php?topic=69)

## Requirements
- TextMate [http://macromates.com](http://macromates.com)
- monkey [http://www.monkeycoder.co.nz](http://www.monkeycoder.co.nz)

## Changelog

**2011-03-01**  
- Initial public release