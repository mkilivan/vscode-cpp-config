# VS Code C++ Config

## How to install
1. Install [VSCode](https://code.visualstudio.com/)
1. Install `clang-format` and `clang-tidy`<br/>
  `sudo apt install clang-format clang-tidy`
1. Install [C/C++](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools) extention<br/>
Launch VS Code Quick Open (Ctrl+P), paste the following command, and press enter.<br/>
`ext install ms-vscode.cpptools`
1. Install [CMake Tools](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cmake-tools) extention<br/>
Launch VS Code Quick Open (Ctrl+P), paste the following command, and press enter.<br/>
`ext install ms-vscode.cmake-tools`
## Available commands (`CTRL-P`)
| Task                           | Keybinding            |
| ------------------------------ | --------------------- |
| `CMake: Run Without Debugging` | <kbd>Shift</kbd>+<kbd>F5</kbd>   |
| `CMake: Build`                 | <kbd>F7</kbd>         |
| `Debug: Start Debugging`       | <kbd>F5</kbd>         |
