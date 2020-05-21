# VS Code C++ Config

## How to install
1. Install [VS Code](https://code.visualstudio.com/)
1. Install `clang-format` and `clang-tidy`<br/>
  `sudo apt install clang-format clang-tidy`
1. Install the following VS Code extentions

| Extention | Launch VS Code Quick Open (Ctrl+P), paste the following command, and press enter
| --------- | --------------------------------------------------------------------------------
|[C/C++](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools)|`ext install ms-vscode.cpptools` |
|[CMake Tools](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cmake-tools)|`ext install ms-vscode.cpptools` |
|[C/C++ Advanced Lint](https://marketplace.visualstudio.com/items?itemName=jbenden.c-cpp-flylint)|`ext install jbenden.c-cpp-flylint` |
## Available VS Code commands (`CTRL-P`)
| Task                           | Keybinding                       |
| ------------------------------ | -------------------------------- |
| `CMake: Run Without Debugging` | <kbd>Shift</kbd>+<kbd>F5</kbd>   |
| `CMake: Build`                 | <kbd>F7</kbd>                    |
| `Debug: Start Debugging`       | <kbd>F5</kbd>                    |

## General CMake Options
CMake options are variables that can either be ON or OFF, with a controllable default. You can set an option either with CMake Gui tools or the command line via -D.

### ENABLE_DOXYGEN
(Defaults to OFF) If enabled, the Doxygen documents will be built.

### ENABLE_CPPCHECK
(Defaults to OFF) Enable static analysis with cppcheck

### ENABLE_CLANG_TIDY 
(Defaults to OFF) Enable static analysis with clang-tidy
