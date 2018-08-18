# Part 2 - Become a VSCode Power User

## Table of Contents

1.  [Why VSCode?](#why-vscode)
1.  [Command Palette](#vscode-command-palette)
1.  [Settings](#vscode-settings)
1.  [Shortcuts](#vscode-shortcuts)
1.  [Keybindings](#vscode-keybindings)
1.  [Debugger](#vscode-debugger)
1.  [Version Control](#vscode-version-control)
1.  [Integrated Terminal](#vscode-integrated-terminal)
1.  [Emmet](#emmet)
1.  [Snippets](#vscode-snippets)
1.  [Extensions](#vscode-extensions)
1.  [Summary](#what-we-learned)

---

> _Weeks of coding can save you hours of planning. - Unknown_

---

## Why VSCode?

I've used a variety of other text editors (Brackets, Atom, Sublime, and Vim). I prefer VSCode for its robust IDE functionality, customizable settings, and user-friendly interface.

1. Install VSCode

- [ ] [Install on macOS](https://code.visualstudio.com/docs/setup/mac)
- [ ] [Install on Windows](https://code.visualstudio.com/docs/setup/windows)
- [ ] [Install on Linux](https://code.visualstudio.com/docs/setup/linux)

Please find a list of important features, settings, and tools included below. I consider knowledge of these functions essential to improving the speed and ease your development workflow with VSCode.

I'm not an expert programmer and this is not an exhaustive list of VSCode features. I probably only use 5-10% of this text editor's potential during my typical development workflow. If I fail to mention your favorite feature make a pull request and I'll likely include it.

---

## VSCode Command Palette

This is where all the magic happens. Stop searching, opening, and configuring manually- use the command palette!

### Command Palette

- [ ] Type <kbd>cmd/ctrl</kbd> + <kbd>shift</kbd> + <kbd>p</kbd> to open the command palette.

- [ ] The default `>` indicates you are in the VSCode command shell - this is where native and extension commands live.

### Symbolic Search

- [ ] Type <kbd>cmd/ctrl</kbd> + <kbd>shift</kbd> + <kbd>o</kbd> to open the symbolic search palette.

- [ ] The default `@` indicates you are doing a symbolic search - this is a smart search that searches by 'symbols' present in the currently open file. In Javascript, symbols are function declarations, in CSS they are selectors, and in markdown they are headers- etc.

### Fuzzy File Search

- [ ] Type <kbd>cmd/ctrl</kbd> + <kbd>p</kbd> to open the fuzzy file search.

- [ ] No leading character indicates you are conducting a fuzzy file search. Use this feature to quickly switch to files.

### Go to Line Search

- [ ] Type <kbd>cmd/ctrl</kbd> + <kbd>g</kbd> to open the Go to Line search.

- [ ] The default `:` indicates you are in the Go to Line search - this allows you to quickly go to a specific line.

[VSCode Command Palette Docs](https://code.visualstudio.com/docs/getstarted/userinterface)

---

## VSCode Settings

To open settings with the command line:

- [ ] Type <kbd>cmd/ctrl</kbd> + <kbd>shift</kbd> + <kbd>p</kbd> to open the command palette

- [ ] Type `Preferences: Open Settings`

- [ ] To edit settings type/paste custom settings in JSON format in the user settings window on the right

### Please find the custom settings I use below:

#### Emmet Specific Settings

```javascript
{
  // An array of languages where Emmet abbreviations should not be expanded.
  "emmet.excludeLanguages": [
    "markdown"
  ],
  // Path to a folder containing Emmet profiles and snippets.'
  // Enable Emmet abbreviations in languages that are not supported by default. Add a mapping here between the language and emmet supported language.
  // E.g.: {"vue-html": "html", "javascript": "javascriptreact"}
  "emmet.includeLanguages": {},
  // When set to false, the whole file is parsed to determine if current position is valid for expanding Emmet abbreviations. When set to true, only the content around the current position in css/scss/less files is parsed.
  "emmet.optimizeStylesheetParsing": true,
  // Preferences used to modify behavior of some actions and resolvers of Emmet.
  "emmet.preferences": {},
  // Shows possible Emmet abbreviations as suggestions. Not applicable in stylesheets or when emmet.showExpandedAbbreviation is set to "never".
  "emmet.showAbbreviationSuggestions": true,
  // Shows expanded Emmet abbreviations as suggestions.
  // The option "inMarkupAndStylesheetFilesOnly" applies to html, haml, jade, slim, xml, xsl, css, scss, sass, less and stylus.
  // The option "always" applies to all parts of the file regardless of markup/css.
  "emmet.showExpandedAbbreviation": "always",
  // If true, then Emmet suggestions will show up as snippets allowing you to order them as per editor.snippetSuggestions setting.
  "emmet.showSuggestionsAsSnippets": false,
  // Define profile for specified syntax or use your own profile with specific rules.
  "emmet.syntaxProfiles": {},
  // When enabled, Emmet abbreviations are expanded when pressing TAB.
  "emmet.triggerExpansionOnTab": false,
  // Variables to be used in Emmet snippets
  "emmet.variables": {},
}
```

#### Prettier Specific Settings

```javascript
{
  //Prettier settings
  "editor.formatOnSave": true,
  // Enable per-language
  "[javascript]": {
  "editor.formatOnSave": true
}
```

#### Theme Specific Settings

```javascript
{
  //Theme settings
  "workbench.colorTheme": "Cobalt2",
  "editor.fontFamily": "Inconsolata, Operator Mono, Menlo, Monaco, 'Courier New', monospace",
  "editor.fontSize": 20,
  "editor.lineHeight": 25,
  "editor.letterSpacing": 0.5,
  "files.trimTrailingWhitespace": true,
  "editor.fontWeight": "400",
  "prettier.eslintIntegration": true,
  "editor.cursorStyle": "line",
  "editor.cursorWidth": 5,
  "editor.cursorBlinking": "solid",
  "editor.wordWrap": "on",
  "editor.renderWhitespace": "all",
  "window.zoomLevel": 2,
  "workbench.startupEditor": "newUntitledFile",
  "explorer.confirmDragAndDrop": false,
  "explorer.confirmDelete": false,
}
```

#### Terminal Specific Settings

```javascript
{
  // Terminal settings
  "terminal.integrated.fontSize": 24,
  "terminal.integrated.lineHeight": 1,
  "terminal.integrated.fontFamily": "Inconsolata"
}
```

#### Todo Highlighter Specific Settings

```javascript
{
  // Todo Highlighter settings
  "todohighlight.isEnable": true,
  "todohighlight.keywords": [
    "TBD",
    "TODO"
  ]
}
```

#### cSpell Checker Specific Settings

```javascript
{
  // cSpell settings
  "cSpell.userWords": [
    "exampleWordToAddToGlobalDictionary",
  ]
}
```

---

## VSCode Shortcuts

To view/edit shortcuts with the command line:

- [ ] Type <kbd>cmd/ctrl</kbd> + <kbd>shift</kbd> + <kbd>p</kbd> to open the command palette

- [ ] Type `Preferences: Open Keyboard Shortcuts`

#### Memorize these shortcuts to improve your workflow

Cut line <kbd>cmd/ctrl</kbd> + <kbd>x</kbd>

Select multiple items <kbd>cmd/ctrl</kbd> + <kbd>d</kbd>

[Complete list for macOS](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf)

[Complete list for Windows](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)

---

## VSCode Keybindings

To view/edit keybindings with the command line:

- [ ] Type <kbd>cmd/ctrl</kbd> + <kbd>shift</kbd> + <kbd>p</kbd> to open the command palette

- [ ] Type `Preferences: Open Keyboard Shortcuts`

- [ ] Select `keybindings.json`

### Please find some essential keybinding additions below:

#### macOS

```javascript
[
  {
    // bubble move a line up
    key: "cmd+shift+up",
    command: "editor.action.moveLinesUpAction",
    when: "editorTextFocus"
  },
  {
    // bubble move a line down
    key: "cmd+shift+down",
    command: "editor.action.moveLinesDownAction",
    when: "editorTextFocus"
  },
  {
    // duplicate a line
    key: "cmd+shift+d",
    command: "editor.action.copyLinesDownAction",
    when: "editorTextFocus && !editorReadonly"
  }
];
```

#### Linux

---

> _Linux is only free if your time has no value. - Jamie Zawinski_

---

```javascript
[
  {
    // bubble move a line up
    key: "ctrl+shift+gup",
    command: "editor.action.moveLinesUpAction",
    when: "editorTextFocus"
  },
  {
    // bubble move a line down
    key: "ctrl+shift+down",
    command: "editor.action.moveLinesDownAction",
    when: "editorTextFocus"
  },
  {
    // duplicate a line
    key: "ctrl+shift+d",
    command: "editor.action.copyLinesDownAction",
    when: "editorTextFocus && !editorReadonly"
  }
];
```

#### Now these helpful shortcuts are available to you

Bubble move a line up <kbd>cmd/ctrl</kbd> + <kbd>shift</kbd> + <kbd>up</kbd>

Bubble move a line down <kbd>cmd/ctrl</kbd> + <kbd>shift</kbd> + <kbd>down</kbd>

Duplicate a line <kbd>cmd/ctrl</kbd> + <kbd>shift</kbd> + <kbd>d</kbd>

[VSCode Keybinding docs](https://code.visualstudio.com/docs/getstarted/keybindings)

---

## VSCode Debugger

To use the VSCode integrated debugger:

1. Go to the VSCode debugger with <kbd>cmd/ctrl</kbd> + <kbd>shift</kbd> + <kbd>alt</kbd> + <kbd>d</kbd>

[VSCode Debugger Docs](https://code.visualstudio.com/docs/editor/debugging)

---

## VSCode Version Control

To use the VSCode integrated version control:

1. Go to VSCode integrated version with <kbd>cmd/ctrl</kbd> + <kbd>shift</kbd> + <kbd>g</kbd>

[VSCode Version Control Docs](https://code.visualstudio.com/docs/editor/versioncontrol)

---

## VSCode Integrated Terminal

To use the VSCode integrated terminal:

1. Show VSCode integrated terminal with <kbd>cmd/ctrl</kbd> + <kbd>`</kbd>

[VSCode Integrated Terminal Docs](https://code.visualstudio.com/docs/editor/integrated-terminal)

---

## Emmet

Built into VSCode and accessed like snippets.

[Emmet Docs](https://docs.emmet.io/)

[Emmet Cheatsheet](https://docs.emmet.io/cheat-sheet/)

---

## VSCode Snippets

To view/create VSCode Snippets:

1. Go to the VSCode Command Palette with <kbd>cmd/ctrl</kbd> + <kbd>shift</kbd> + <kbd>p</kbd>
1. Type `Preferences: Configure User Snippets`
1. To create a new snippet, type `New Global Snippets File`

[VSCode Snippets Docs](https://code.visualstudio.com/docs/editor/userdefinedsnippets)

---

## VSCode Extensions

### Please find a curated list of VSCode extensions below

To view/install extensions:

1. Go to VSCode extensions with <kbd>cmd/ctrl</kbd> + <kbd>shift</kbd> + <kbd>x</kbd>

#### AutoClose Tag

_Automatically add HTML/XML close tag, same as Visual Studio IDE or Sublime Text_

```sh
code --install-extension formulahendry.auto-close-tag
```

#### AutoImport

_Automatically finds, parses and provides code actions and code completion for all available imports_

```sh
code --install-extension steoates.autoimport
```

#### AutoRename Tag

_Automatically rename paired HTML/XML tag, same as Visual Studio IDE does_

```sh
code --install-extension formulahendry.auto-rename-tag
```

#### Cobalt2

_🔥 Official theme by Wes Bos_

```sh
code --install-extension wesbos.theme-cobalt2
```

#### Code Spell Checker

_A basic spell checker that works well with camelCase code._

```sh
code --install-extension streetsidesoftware.code-spell-checker
```

#### Color Highlight - css

_This extension styles css/web colors found in your document_

```sh
code --install-extension naumovs.color-highlight
```

#### Docker

_Adds syntax highlighting, commands, hover tips, and linting for Dockerfile and docker-compose files_

```sh
code --install-extension peterjausovec.vscode-docker
```

#### ESLint

_Integrates ESLint JavaScript into VS Code_

```sh
code --install-extension dbaeumer.vscode-eslint
```

#### Git History

_View git log, file history, compare branches or commits_

```sh
code --install-extension donjayamanne.githistory
```

#### CSS ClassNames

_CSS class name completion for the HTML class attribute based on the definitions found in your workspace_

```sh
code --install-extension zignd.html-css-class-completion
```

#### NodeJS Modules

_Autocompletes Node.js modules in import statements_

```sh
code --install-extension leizongmin.node-module-intellisense
```

#### Prettier

_VS Code package to format your JavaScript / TypeScript / CSS using Prettier_

```sh
code --install-extension esbenp.prettier-vscode
```

[★ Learn how to integrate Prettier with ESLint/airbnb's style guide ★](https://blog.echobind.com/integrating-prettier-eslint-airbnb-style-guide-in-vscode-47f07b5d7d6a)

#### TODO Highlight

_Highlight TODO, FIXME and other annotations within your code._

```sh
code --install-extension wayou.vscode-todo-highlight
```

#### Trailing Spaces

_Highlight trailing spaces and delete them in a flash!_

```sh
code --install-extension shardulm94.trailing-spaces
```

#### VSCode Icons

_Icons for Visual Studio Code_

```sh
code --install-extension robertohuertasm.vscode-icons
```

#### VSCode Random

_This extension generates random data directly into VS Code_

```sh
code --install-extension jrebocho.vscode-random
```

#### What we learned

- Understand breadth and depth of VSCode functionality
- Utilize key features and add-ons to maximize development experience

[Go to Part 3 - Code Faster/Better/Stronger at Hack Reactor](https://github.com/nvincenthill/streamlineyourworkflow/tree/master/Part%203/PART3.md)
