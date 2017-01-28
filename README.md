# VS Code setup 
The goal of this document is to list out configurations and extensions that I use with VS Code. It aims to be more of a concentrated list and less of a "here's the firehose" `awesome-list` (Even though I like awesome lists and all of the work that goes into making them :clap:)

> After using Atom for about 2 years, I have switched to using VS Code. Why? VS Code is fast. It's almost on par with Sublime Text. It also comes with a few more "batteries included" ⚡️ features, like a terminal and git integration. With all of this being said, this document contains opinions. If you agree with them, great! If not, that's also great!

### Starting out
##### Shortcuts
If you're coming from Atom, you won't feel too far from home 😉

- `Cmd + P` to open any file
- `Cmd + Shift + P` to access the command palette

##### Side Bar 
The following commands are for switching out the view for the Side Bar on the left

- `Cmd + Shift + E` show file explorer
- `Cmd + Shift + F` show find/replace (global)
- `Ctrl + Shift + G` show git tools
- `Cmd + Shift + D` show debugging tools
- `Cmd + Shift + X` show extensions menu

##### Terminal
`Ctrl + (backtick)` although, you'd probably have an easier time remapping this to something like `Ctrl + '`
> Easy, just add a new shortcut 

`Cmd + K`, `Cmd + S`

`{ "key": "ctrl+'", "command": "workbench.action.terminal.toggleTerminal" }`

### Set your User Settings
Open the user settings file, `Cmd + ,`. Here, you'll find all of the settings that can be modified for VS Code. Once you find one that you want to modify, click next to it and it will be copied over into your own settings file. A few good custom settings to start with are font size and font family.

```json
{
  "editor.fontFamily": "Operator Mono",
  "editor.fontSize": 14,
  "editor.tabSize": 2,
  "workbench.activityBar.visible": false,
  "javascript.validate.enable": false
}
```
### Why do you disable javascript validation? 
> `¯\_(ツ)_/¯` I rely on `ESLint`

### The Sweet Setup
Now, for the list of extensions. I'll list links to the VSCode marketplace, as well as the install commands. To install any of these, simply press `Cmd + P` and paste the install command listed next to each extension.

#### Workspace enhancements
- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

  `ext install vscode-eslint`

  > If you use a `.eslintrc` file and have `ESLint` installed either in the project locally or globally, then this _just works_.
  
- [Git Project Manager](https://marketplace.visualstudio.com/items?itemName=felipecaputo.git-project-manager)

  `ext install git-project-manager`
  
  > Damn, this is awesome! `Cmd + Option + P` and start typing a `.git` project. Hit `Enter` to switch to that project in the same window. This supports customization like folder paths to monitor as well as a maximum recursion level to look for `.git` projects.
  
- [NPM Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.npm-intellisense)

  `ext install npm-intellisense`

  > Completions of node modules in your `package.json` dependencies? ✅ Check.
- [Path Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense)

  `ext install path-intellisense`

  > Autocompletion of filenames. And, it even drops the `.js` if you are importing a module.
  
- [Code Runner](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner)

  `ext install code-runner`

  > Handy. Highlight code. Run it! It even lets you customize how certain languages should run.
  
- [Advanced New File](https://marketplace.visualstudio.com/items?itemName=patbenatar.advanced-new-file)

  `ext install advanced-new-file`

  > `Cmd + Option + N`, select a relative directory. Done.
  
- [Open in GitHub](https://marketplace.visualstudio.com/items?itemName=sysoev.vscode-open-in-github)

  `ext install vscode-open-in-github`

  > Nice shortcuts when you need to quickly open a file on GitHub (either in the current branch _or_ master). This will even jump to the line number.
  
#### Language support and syntax highlighting
- [Docker Support](https://marketplace.visualstudio.com/items?itemName=PeterJausovec.vscode-docker)

  `ext install vscode-docker`

  > Create dockerfiles. Syntax highlighting and linting. And, Intellisense on image names from Dockerhub.com
  
- [Sublime Babel](https://marketplace.visualstudio.com/items?itemName=joshpeng.sublime-babel-vscode)

  `ext install sublime-babel-vscode`

  > Significantly improves JavaScript grammar formatting and tokenizing for syntax highlighting

- [GraphQL](https://marketplace.visualstudio.com/items?itemName=mquandalle.graphql)

  `ext install graphql`

  > Syntax highlighting and code snippets for `GraphQL`

- [Tomorrow Kit for Sublime Babel](https://marketplace.visualstudio.com/items?itemName=joshpeng.theme-tomorrowkit-sublime)
  
  `ext install theme-tomorrowkit-sublime`

  > Collection of Tomorrow themes that take advantage of Sublime Babel extension (listed above)
  
- [File Icons](https://marketplace.visualstudio.com/items?itemName=file-icons.file-icons)

  `ext install file-icons`
  
  > Port of `file-icons` package for Atom
