# Autolinting for Javascript in VSCode

## Features

Automatically activates/deactivates the correct linters in Visual Studio Code for your current Javascript workspace depending on which configuration files can be found.  
If no configuration can be found, user defined default linters will be used.

Currently supported linters:

* ESLint
* JSHint
* JSCS

## Requirements

All linter extensions you want to use have to be installed in Visual Studio Code.  
You can find these extensions here:

* [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
* [JSHint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.jshint)
* [JSCS](https://marketplace.visualstudio.com/items?itemName=ms-vscode.jscs)

## Extension Settings

If you want to set one or more default linters (for the case that no configuration can be found), you can add a setting to your configuration:

* `jsAutolint.defaultLinters`: Set to an Array containing all linters you want to activate if no known linter configuration can be found (e.g. `["jshint", "jscs"]`).   
Possible Values:
  * `eslint`
  * `jscs`
  * `jshint`

The default linters will be set if you either open a Javascript file while a folder is opened (if you just open single files the linters won't get set automatically) or if you run the command `Automatically set correct Javascript linters` from the command palette.

## Release Notes

### 1.0.0

Initial release
