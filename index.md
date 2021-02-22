Coding Task: Colour Chart
=========================

This is a command line application to generate various test patterns.
In the simplest case this program will produce a colour ramp starting with one
colour on one side of the display and changing smoothly to a second colour on the other side.
In the most complex case there will be a different colour in each corner of the display and
each pixel on the display will show the appropriate mix of these four colours.


### Implementation Details
* Language
  * C++14
* Compiler
  * GCC-8.1.0
  * Visual Studio 2019 - x86
* Build Machine
  * Ubuntu 16.04
  * Windows 10
* Coding Style
  * Custom coding style with clang-format


### Requirements
* CMake 3.0+
* C++14 or newer compiler


### Usage
```bash
ramp display tl tr [bl] [br]
```
* **display** is the name of the display device
* **tl** is the top left colour value
* **tr** is the top right colour value
* **bl** is the bottom left colour value [optional, defaults to tl]
* **br** is the bottom right colour value [optional, defaults to tr]

The colour values are specified as 16-bit RGB565 pixels in hex or decimal.

## Solution Details

* The implementation has been broken up into short and simple pieces to make it an easier read. This also made it easier
  to test.
* The solution has been delivered as a CMake project. It has been compiled and tested on Ubuntu 16.10 and Windows.
* Since the RGB565 format is endian specific, an inline method used to determine endianness, the application should work
  on both little-endian and big-endian architecture, but it has been tested <ins>only on a little-endian machine</ins>.
* Two sets of test group (test_Cli and test_ColourChart) added, and it builds by defaults as part of the project.
* For error handling, exceptions are used. Depending on arguments, the following exceptions may be thrown:
  | Command                      | Exception Type   | Exception Description                |
  |------------------------------|------------------|--------------------------------------|
  | ramp display                 | Invalid argument | Missing arguments                    |
  | ramp display 0 0 0 foo0123   | Invalid argument | Input is not a valid decimal number. |
  | ramp display 0 0 0 0xfoo0123 | Invalid argument | Input is not a valid hex number.     |
  | ramp display 0 0 0 70000     | Out of range     | Input is out ouf range [0 - 65535]   |
  | ramp display 0 0 0 0x12345   | Out of range     | Input is out ouf range [0 - 65535]   |

## Customize

The display's default size is defined in Display.cpp as follows and can be configured at the compile-time, but it can
be accessed only at run time due to provided interface. So it is considered as an argument to the main application.
If the display size is smaller then 2x2, then the application will throw `invalid argument` type exception with
`Display size is too small` description.

```C++
namespace {
  constexpr uint16_t Width = 640;
  constexpr uint16_t Height = 360;
} // namespace
```
### References
* https://en.wikipedia.org/wiki/Bilinear_interpolation
