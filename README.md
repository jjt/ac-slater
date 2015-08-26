# ac-slater
A sensible setup for [Slate](https://github.com/mattr-/slate), based on https://github.com/n1rvana/dot-slate.

## Installation

Install Slate as per [instructions](https://github.com/mattr-/slate#installing-slate), then:

    > git clone https://github.com/jjt/ac-slater.git
    > cp ac-slater/.slate ~/.slate
    > # edit ~/.slate to your liking, set the path to ac-slater
    > # restart Slate and reload config

## Layout Bindings

Default bindings use widths of 1/1 (full width), 1/2, 1/3, 2/3 and heights of 1/1 (full height) or 1/2.

**Size definitions**  

`1/1`, `1/2`, `1/3`, `2/3`: width in percentages of screen  
`F`: full screen  
`L`: left (full height)  
`M`: middle (full height)  
`R`: right (full height)  
`UL`: upper left  
`UM`: upper middle  
`UR`: upper right  
`BL`: bottom left  
`BM`: bottom middle  
`BR`: bottom right  

**Legend**  
```
+-----------+
|           |
|  2/3  UL  |  <----- layout for super key modifier (default: ctrl+alt+shift)
|           |
|     J     |  <----- base key
|           |
|  1/2  UL  |  <----- layout for standard key modifier (default: ctrl+shift)
|           |
+---+-------+
```
`ctrl+shift+J` would make the current window half width, placed in the upper left corner  
`ctrl+alt+shift+J` would make the current window 2/3s width, placed in the upper left corner

### QWERTY
```
+-----------+-----------+-----------+-----------+-----------+
|           |           |           |           |           |
|  2/3  UL  |           |           |           |  2/3  UR  |
|           |           |           |           |           |
|     Y     |     U     |     I     |     O     |     P     |
|           |           |           |           |           |
|  1/2  UL  |  1/3  UL  |  1/3  UM  |  1/3  UR  |  1/2  UR  |
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
### Colemak
```
+-----------+-----------+-----------+-----------+-----------+
|           |           |           |           |           |
|  2/3  UL  |           |           |           |  2/3  UR  |
|           |           |           |           |           |
|     J     |     L     |     U     |     Y     |     ;     |
|           |           |           |           |           |
|  1/2  UL  |  1/3  UL  |  1/3  UM  |  1/3  UR  |  1/2  UR  |
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
