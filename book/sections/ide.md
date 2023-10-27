# IDE

Using an Integrated development environment (IDE) will certainly save you time,
but the advantages of using an IDE go beyond that. Below are some IDE advantages

1. Syntax highlighting
2. Text autocompletion
3. Refactoring options
4. Easily Importing libraries
5. Build, compile, or run

## Visual Studio Code

You may already have a preferred IDE that you use regularly, however we strongly
suggest that you use VS Code for this course and afterwards replicate the setup
as you choose. If you already have VS Code installed please make sure it is
updated to the latest version.

To install VS Code follow the instructions [here](https://code.visualstudio.com/).

Below are some VSC advantages

1. IntelliSense: Go beyond syntax highlighting and autocomplete
2. Run & Debug: Debug code right from the editor
3. Built-in Git: Review diffs, stage files, and make commits right from the editor.
4. Extensible and customizable: Install extensions to add new languages, themes, debuggers, and to connect to additional services.

### VSC Example: automatically using black

> Configure VSC to use Black

Open Settings: Code (or File) > Preferences > Settings

- Search for `python formatting provider` and choose `black`
- Search for `format on save` and check the box to enable

> Select interpreter

Open `Command Palette`: View > `Command Palette..` (or `Ctrl+Shift+P`)

- Search for `Python: Select Interpreter`
- Choose the correct environment

Now the Black package is going to fix your codes layout every time you save a
code file.

### VSC Extensions

#### Useful Extensions

- Extension: GitLens — Git supercharged
- Extension: autoDocstring - Python Docstring Generator
- Extension: Code Spell Checker
- Extension: markdownlint
- Extension: Markdown All in One
