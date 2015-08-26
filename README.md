# AC Slater
A hunky, extensible default setup for the keyboard-driven, tiling window manager [Slate](https://github.com/mattr-/slate), based on https://github.com/n1rvana/dot-slate.

Throw windows around with ease to make tiled layouts such as:

```
+-----------------------------------+  +-----------------------------------+
|                 |                 |  |                |                  |
|      ctrl       |      ctrl       |  |                |      ctrl        |
|      shift      |      shift      |  |                |      shift       |
|        Y        |        P        |  |                |        P         |
|                 |                 |  |     ctrl       |                  |
+-----------------------------------+  |     shift      +------------------+
|           |           |           |  |       H        |                  |
|   ctrl    |   ctrl    |   ctrl    |  |                |      ctrl        |
|   shift   |   shift   |   shift   |  |                |      shift       |
|     M     |     ,     |     .     |  |                |        /         |
|           |           |           |  |                |                  |
+-----------------------------------+  +-----------------------------------+
                                                                            
+-----------------------------------+  +-----------------------------------+
|                       |           |  |           |                       |
|                       |   ctrl    |  |   ctrl    |       ctrl alt        |
|                       |   shift   |  |   shift   |         shift         |
|                       |     O     |  |     U     |           P           |
|      ctrl alt         |           |  |           |                       |
|        shift          +-----------+  +-----------------------------------+
|          H            |           |  |                       |           |
|                       |   ctrl    |  |       ctrl alt        |   ctrl    |
|                       |   shift   |  |         shift         |   shift   |
|                       |     .     |  |           N           |     .     |
|                       |           |  |                       |           |
+-----------------------------------+  +-----------------------------------+
```

## Installation

Install Slate as per [instructions](https://github.com/mattr-/slate#installing-slate), then:

    > git clone https://github.com/jjt/ac-slater.git
    > cp ac-slater/.slate ~/.slate
    > # edit ~/.slate to your liking, set the path to ac-slater
    > # restart Slate and reload config

## Layout

Default bindings use widths of 1/1 (full width), 1/2, 1/3, 2/3 and heights of 1/1 (full height) or 1/2 and are arranged on the right hand side of the keyboard in an intutive fashion.

**Size definitions**  

`1/1`, `1/2`, `1/3`, `2/3`: width in percentages of screen  
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

**Legend**  
```
+-----------+
|           |
|  2/3  TL  |  <----- layout for super key modifier (default: ctrl+alt+shift)
|           |
|     J     |  <----- base key
|           |
|  1/2  TL  |  <----- layout for standard key modifier (default: ctrl+shift)
|           |
+---+-------+
```
`ctrl+shift+J` would make the current window half width, placed in the upper left corner  
`ctrl+alt+shift+J` would make the current window 2/3s width, placed in the upper left corner

### QWERTY Keyboard Layout
```
+-----------+-----------+-----------+-----------+-----------+
|           |           |           |           |           |
|  2/3  TL  |           |           |           |  2/3  TR  |
|           |           |           |           |           |
|     Y     |     U     |     I     |     O     |     P     |
|           |           |           |           |           |
|  1/2  TL  |  1/3  TL  |  1/3  TM  |  1/3  TR  |  1/2  TR  |
|           |           |           |           |           |
+---+-------+---+-------+---+-------+---+-------+---+-------+---+
    |           |           |           |           |           |
    |   2/3 L   |           |           |           |   2/3 R   |
    |           |           |           |           |           |
    |     H     |     J     |     K     |     L     |     ;     |
    |           |           |           |           |           |
    |   1/2 L   |   1/3 L   |   1/3 M   |   1/3 R   |   1/2 R   |
    |           |           |           |           |           |
    +---+-------+---+-------+---+-------+---+-------+---+-------+---+
        |           |           |           |           |           |
        |  2/3  BL  |           |           |           |  2/3  BR  |
        |           |           |           |           |           |
        |     N     |     M     |     ,     |     .     |     /     |
        |           |           |           |           |           |
        |  1/2  BL  |  1/3  BL  |  1/3  BM  |  1/3  BR  |  1/2  BR  |
        |           |           |           |           |           |
        +-----------+-----------+-----------+-----------+-----------+
```
### Colemak Keyboard Layout
```
+-----------+-----------+-----------+-----------+-----------+
|           |           |           |           |           |
|  2/3  TL  |           |           |           |  2/3  TR  |
|           |           |           |           |           |
|     J     |     L     |     U     |     Y     |     ;     |
|           |           |           |           |           |
|  1/2  TL  |  1/3  TL  |  1/3  TM  |  1/3  TR  |  1/2  TR  |
|           |           |           |           |           |
+---+-------+---+-------+---+-------+---+-------+---+-------+---+
    |           |           |           |           |           |
    |   2/3 L   |           |           |           |   2/3 R   |
    |           |           |           |           |           |
    |     H     |     N     |     E     |     I     |     O     |
    |           |           |           |           |           |
    |   1/2 L   |   1/3 L   |   1/3 M   |   1/3 R   |   1/2 R   |
    |           |           |           |           |           |
    +---+-------+---+-------+---+-------+---+-------+---+-------+---+
        |           |           |           |           |           |
        |  2/3  BL  |           |           |           |  2/3  BR  |
        |           |           |           |           |           |
        |     K     |     M     |     ,     |    .      |     /     |
        |           |           |           |           |           |
        |  1/2  BL  |  1/3  BL  |  1/3  BM  |  1/3  BR  |  1/2  BR  |
        |           |           |           |           |           |
        +-----------+-----------+-----------+-----------+-----------+
```

### Extending

Relax, preppy. AC Slater is broken up into separate parts so you can extend it. Here's the default `.slate` file:

```shell
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
source ${ac-slater-path}/layout.slate
source ${ac-slater-path}/bindings.slate

# Post-AC custom config here, ex:
# bind 4:ctrl hint ARSTDHNEIO
```
