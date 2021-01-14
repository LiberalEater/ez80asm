## EZ80 Assembly for Visual Studio Code
The EZ80 Assembly extension for Visual Studio provides language support for EZ80 Assembly, if you want an extension for z80 and gameboy z80 I also have extensions for those

### Syntax Highlighting
* Labels
* Assembler directives
* Opcodes, registers, and numbers

### Label and equate documentation
* Add markdown documentation in comments
* Hover over a label or equate to see it's documentation
* Peek and find definitions and references of equates and labels
* Automatically searches all included files in the current workspace for documentation
* Option to toggle case-sensitivity

### Intellisense Suggestions
* Start typing and get suggestions based on included symbols and documented ez80 snippets
* Snippet documentation includes flags, bytes, and cycles
* Snippets can be toggled in settings and there are many settings regarding casing of inserted snippets

### Global Include Directories
* Configure a global include directory in settings to automatically search for symbols and documentation
* Directory format can be parent/folder or parent\\\\folder
* Directories can be absolute or relative to the workspace
* Note that changing this setting may require VS Code to reload to reflect changes

### Semantic Highlighting
* Helps to distinguish functions(with ":"), labels (without ":"), and equates
* Make sure you have semantic highlighting on in settings

### Diagnostic Provider
* Note that these diagnostics are specific to the ez80 CPU and spasm-ng assembler
* Error checking while you type
* Can be disabled in settings
* Can check for duplicate declarations in a document (but not included files)
* Won't check .inc files for problems (it can slow down the extension a bit)

### Symbol Renaming
* Rename a label or equate across all included files
* If the declaration is in a .inc file, you have to rename in that file to prevent accidental renaming

### License
This project is subject to [these terms](https://github.com/LiberalEater/ez80asm/blob/main/LICENSE.txt).

### Known Bugs
* Undoing (Ctrl + z) a rename will cause an error if the symbol is in multiple files, to fix, just type anything on the line with the error and save
* Sometimes semantic highlighting can be messed up, to fix, press (Ctrl + a) and (Ctrl + /) x 2 (it basically rescans the document)
* Semantic highlighting fires before rescan

