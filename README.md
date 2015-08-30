# AC Slater
A hunky, extensible layout for the tiling window manager [Slate](https://github.com/mattr-/slate), with a set of spacially-intuitive key bindings. Based on the work done in https://github.com/n1rvana/dot-slate.

![Hunk](http://i.imgur.com/A7P1oA9.jpg)

Throw windows around with ease to make tiled layouts such as:

```
+-----------------------------------+     +-----------------------------------+
|                 |                 |     |                |                  |
|      ctrl       |      ctrl       |     |                |      ctrl        |
|      shift      |      shift      |     |                |      shift       |
|        Y        |        P        |     |                |        P         |
|                 |                 |     |     ctrl       |                  |
+-----------------------------------+     |     shift      +------------------+
|           |           |           |     |       H        |                  |
|   ctrl    |   ctrl    |   ctrl    |     |                |      ctrl        |
|   shift   |   shift   |   shift   |     |                |      shift       |
|     M     |     ,     |     .     |     |                |        /         |
|           |           |           |     |                |                  |
+-----------------------------------+     +-----------------------------------+

                                                                               
+-----------------------------------+     +-----------------------------------+
|                       |           |     |           |                       |
|                       |   ctrl    |     |   ctrl    |       ctrl alt        |
|                       |   shift   |     |   shift   |         shift         |
|                       |     O     |     |     U     |           P           |
|      ctrl alt         |           |     |           |                       |
|        shift          +-----------+     +-----------------------------------+
|          H            |           |     |                       |           |
|                       |   ctrl    |     |       ctrl alt        |   ctrl    |
|                       |   shift   |     |         shift         |   shift   |
|                       |     .     |     |           N           |     .     |
|                       |           |     |                       |           |
+-----------------------------------+     +-----------------------------------+
```

## Installation

Install Slate as per [instructions](https://github.com/mattr-/slate#installing-slate), then:

    > git clone https://github.com/jjt/ac-slater.git
    > cp ac-slater/.slate ~/.slate
    > # edit ~/.slate to your liking, set the path to ac-slater
    > # restart Slate and reload config

## Layout

Default bindings use widths of 1/1 (full width), 1/2, 1/3, 2/3 and heights of 1/1 (full height) or 1/2 and are arranged on the right hand side of the keyboard in an intutive fashion.

**Legend**  

`1/1`, `1/2`, `1/3`, `2/3`: width in percentages of screen  
`TOP/BTM/RGT/LFT SCR`: move window to that screen  

`F`: full screen  
`L`: left (full height)  
`M`: middle (full height)  
`R`: right (full height)  
`TL`: top left  
`TM`: top middle  
`TR`: top right  
`BL`: bottom left  
`BM`: bottom middle  
`BR`: bottom right  

**Example**  
```
+-----------+
|  2/3  TL  |  <----- layout for super key modifier (default: ctrl+alt+shift)
|           |
|     J     |  <----- base key
|           |
|  1/2  TL  |  <----- layout for standard key modifier (default: ctrl+shift)
+---+-------+
```
`ctrl+shift+J` would make the current window half width, placed in the upper left corner  
`ctrl+alt+shift+J` would make the current window 2/3s width, placed in the upper left corner

### QWERTY Keyboard Layout
```
+-----------+-----------+-----------+-----------+-----------+
|  2/3  TL  |           |  TOP SCR  |           |  2/3  TR  |
|           |           |           |           |           |
|     Y     |     U     |     I     |     O     |     P     |
|           |           |           |           |           |
|  1/2  TL  |  1/3  TL  |  1/3  TM  |  1/3  TR  |  1/2  TR  |
+---+-------+---+-------+---+-------+---+-------+---+-------+---+
    |   2/3 L   |  LFT SCR  |           |  RGT SCR  |   2/3 R   |
    |           |           |           |           |           |
    |     H     |     J     |     K     |     L     |     ;     |
    |           |           |           |           |           |
    |   1/2 L   |   1/3 L   |   1/3 M   |   1/3 R   |   1/2 R   |
    +---+-------+---+-------+---+-------+---+-------+---+-------+---+
        |  2/3  BL  |           |  BOT SCR  |           |  2/3  BR  |
        |           |           |           |           |           |
        |     N     |     M     |     ,     |     .     |     /     |
        |           |           |           |           |           |
        |  1/2  BL  |  1/3  BL  |  1/3  BM  |  1/3  BR  |  1/2  BR  |
        +-----------+-----------+-----------+-----------+-----------+
```
### Colemak Keyboard Layout
```
+-----------+-----------+-----------+-----------+-----------+
|  2/3  TL  |           |  TOP SCR  |           |  2/3  TR  |
|           |           |           |           |           |
|     J     |     L     |     U     |     Y     |     ;     |
|           |           |           |           |           |
|  1/2  TL  |  1/3  TL  |  1/3  TM  |  1/3  TR  |  1/2  TR  |
+---+-------+---+-------+---+-------+---+-------+---+-------+---+
    |   2/3 L   |  LFT SCR  |           |  RGT SCR  |   2/3 R   |
    |           |           |           |           |           |
    |     H     |     N     |     E     |     I     |     O     |
    |           |           |           |           |           |
    |   1/2 L   |   1/3 L   |   1/3 M   |   1/3 R   |   1/2 R   |
    +---+-------+---+-------+---+-------+---+-------+---+-------+---+
        |  2/3  BL  |           |  BOT SCR  |           |  2/3  BR  |
        |           |           |           |           |           |
        |     K     |     M     |     ,     |    .      |     /     |
        |           |           |           |           |           |
        |  1/2  BL  |  1/3  BL  |  1/3  BM  |  1/3  BR  |  1/2  BR  |
        +-----------+-----------+-----------+-----------+-----------+
```

## Grid system

AC Slater is based on a 12-column, 12-row grid, and defines position and size aliases relative to the screen.

`x0`-`x11` define x coordinates in 1/12th increments  
`y0`-`y11` define y coordinates in 1/12th increments  
`w1`-`w12` define widths in 1/12th increments  
`h1`-`h12` define heights in 1/12th increments  

This makes it trivial to set up your own operations, like `move`:

```shell
# Moves a window to take up the lower left quarter of the screen
move ${x0};${y6} ${w6};${h6}

# Centers a window, and makes it 2/3 screen width, full screen height
move ${x2};${y0} ${w8};${h12}
```

## Extending/Configuration

Relax, preppy. AC Slater is broken up into separate configurable parts so you can extend it. The only thing you'll have to copy and modify is the default `.slate` file:

```shell
# Copy this file into ~/.slate and modify to your heart's content

# Set PATH_TO_AC_SLATER to wherever you cloned ac-slater
alias ac-slater-path PATH_TO_AC_SLATER

# Aliases for key modifiers
# https://github.com/mattr-/slate#allowed-keys
alias ac-slater-key-modifier        shift;ctrl
alias ac-slater-key-modifier-super  shift;ctrl;alt

# Pre-AC custom config goes here, ex:
# config keyboardLayout colemak

# Bring AC Slater to the party
# Comment out any parts that you don't want
source ${ac-slater-path}/config.slate
source ${ac-slater-path}/origin.slate
source ${ac-slater-path}/grid.slate
source ${ac-slater-path}/layout.slate
source ${ac-slater-path}/bindings.slate

# Colemak user? Gotcha covered:
# source ${ac-slater-path}/bindings-colemak.slate

# Post-AC custom config here, ex:
# bind 4:ctrl hint ARSTDHNEIO
```

## Contributing & Feedback

Pull requests and issues are welcome.
