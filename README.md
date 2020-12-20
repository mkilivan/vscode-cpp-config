# VS Code C++ Config

This is a template C++ project for [VS Code](https://code.visualstudio.com/).

To install dependencies the following tools are recomended:
- for Windows : [choco](https://chocolatey.org/install)
- for MacOS : [brew](https://brew.sh/)
### Dependencies

* [gcc 7+](https://gcc.gnu.org/)
	<details>
	<summary>Install command</summary>

	- Debian/Ubuntu:

			sudo apt install build-essential

	- Windows:

			choco install mingw -y

	- MacOS:

			brew install gcc
	</details>

* [clang 6+](https://clang.llvm.org/)
	<details>
	<summary>Install command</summary>

	- Debian/Ubuntu:

			bash -c "$(wget -O - https://apt.llvm.org/llvm.sh)"

	- Windows:

		Visual Studio 2019 ships with LLVM (see the Visual Studio section). However, to install LLVM separately:

			choco install llvm -y

		llvm-utils for using external LLVM with Visual Studio generator:

			git clone https://github.com/zufuliu/llvm-utils.git
			cd llvm-utils/VS2017
			.\install.bat

	- MacOS:

			brew install llvm
	</details>
* [CMake 3.15+](https://cmake.org/)
	<details>
	<summary>Install Command</summary>

	- Debian/Ubuntu:

			sudo apt-get install cmake

	- Windows:

			choco install cmake -y --installargs 'ADD_CMAKE_TO_PATH=""User""'

	- MacOS:

			brew install cmake

	</details>
### Optional Dependencies
* [Doxygen](http://doxygen.nl/)
	<details>
	<summary>Install Command</summary>

	- Debian/Ubuntu:

			sudo apt-get install doxygen
			sudo apt-get install graphviz

	- Windows:

			choco install doxygen.install -y
			choco install graphviz -y

	- MacOS:

			brew install doxygen
			brew install graphviz

	</details>
* [Cppcheck](http://cppcheck.sourceforge.net/)
	<details>
	<summary>Install Command</summary>

	- Debian/Ubuntu:

			sudo apt-get install cppcheck

	- Windows:

			choco install cppcheck -y

	- MacOS:

			brew install cppcheck

	</details>
### VS Code extentions

| Extention | Launch VS Code Quick Open (Ctrl+P), paste the following command, and press enter
| --------- | --------------------------------------------------------------------------------
|[C/C++](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools)|`ext install ms-vscode.cpptools` |
|[CMake Tools](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cmake-tools)|`ext install ms-vscode.cpptools` |
|[C/C++ Advanced Lint](https://marketplace.visualstudio.com/items?itemName=jbenden.c-cpp-flylint)|`ext install jbenden.c-cpp-flylint` |
### Available VS Code commands (`CTRL-P`)
| Task                           | Keybinding                       |
| ------------------------------ | -------------------------------- |
| `CMake: Run Without Debugging` | <kbd>Shift</kbd>+<kbd>F5</kbd>   |
| `CMake: Build`                 | <kbd>F7</kbd>                    |
| `Debug: Start Debugging`       | <kbd>F5</kbd>                    |

### General CMake Options
CMake options are variables that can either be ON or OFF, with a controllable default. You can set an option either with CMake Gui tools or the command line via -D.

#### ENABLE_DOXYGEN
(Defaults to OFF) If enabled, the Doxygen documents will be built.

#### ENABLE_CPPCHECK
(Defaults to OFF) Enable static analysis with cppcheck

#### ENABLE_CLANG_TIDY
(Defaults to OFF) Enable static analysis with clang-tidy
