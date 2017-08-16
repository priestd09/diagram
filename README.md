## Diagram

Diagram is a CLI tool to generate hand drawn diagrams from ASCII arts. 

It's a full featured CLI application which converts the ASCII text into hand drawn diagrams. The CLI part is based on [gocui](https://github.com/jroimartin/gocui) and the ascii to png conversion is done using the [gg](https://github.com/fogleman/gg) library.

![screencast](images/screencast.gif)

## Installation and usage

```bash
$ go get github.com/esimov/diagram
$ go install

# Start the application
$ diagram
```
A shell script is included to watch the output folder changes and automatically open the generated png files, however `inotifywait` is required for Linux distribution. To install under Linux please run:

```bash
sudo apt install inotify-tools
```

### Key bindings
Key                                     | Description
----------------------------------------|---------------------------------------
<kbd>Tab</kbd>                          | Next Panel
<kbd>Shift+Tab</kbd>                    | Previous Panel
<kbd>Ctrl+s</kbd>                       | Open Save Diagram Modal
<kbd>Ctrl+s</kbd>                       | Save Diagram
<kbd>Ctrl+d</kbd>                       | Convert Ascii to PNG
<kbd>Ctrl+x</kbd>                       | Clear the editor content
<kbd>Ctrl+z</kbd>                       | Restore the editor content
<kbd>PageUp</kbd>                       | Jump to the top
<kbd>PageDown</kbd>                     | Jump to the bottom
<kbd>Home</kbd>                         | Jump to the start line
<kbd>End</kbd>                          | Jump to the end line
<kbd>Ctrl+c</kbd>                       | Quit

## Issues

The app was tested under **Ubuntu** and **MacOS**, but on Mac there are some issues in terms of activating a certain panel by mouse click.

### Acknowledgements
The ascii -> png conversion was ported from [shaky.dart](https://github.com/mraleph/moe-js/blob/master/talks/jsconfeu2012/tools/shaky/web/shaky.dart).

## License

This project is under the MIT License. See the [LICENSE](https://github.com/esimov/diagram/LICENSE) file for the full license text.
