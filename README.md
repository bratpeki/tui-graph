# term-graph-lib: A text-based graphing library written in C

## Repo tree

```
term-graph-lib
├── ex
│   ├── cub.c          Cub function example
│   ├── lin.c          Linear function example
│   └── sqr.c          Square function example
└── src
    └── include
        └── graph.h    Graph source header file
```

## What is it?

`term-graph-lib` is a single-header library for function graphing in the terminal in C.

## How does it work?

Below are the results of compiling the code examples from `ex` and running the output files.

### Linear functions

```
$ make lin; ./lin
A linear function of y = -2*x + (3)
x.....................^......................
.xx...................|......................
...xx.................|......................
....xxx...............|......................
......xxx.............|......................
........xxx...........|......................
..........xx..........|......................
............xxx.......|......................
..............xx......|......................
................xx....|......................
..................xx..|......................
...................xxx|......................
----------------------xxx------------------->
......................|.xxx..................
......................|...xxx................
......................|.....xx...............
......................|.......xx.............
......................|.........xx...........
......................|...........xx.........
......................|.............xx.......
......................|..............xxx.....
......................|.................xx...
......................|..................xxx.
......................|....................x.
......................|......................
```

### Square functions

```
$ make sqr; ./sqr
Square function y=x^2
x.....................^......................
.x....................|....................x.
..x...................|...................x..
...x..................|..................x...
....x.................|.................x....
.....x................|................x.....
......xx..............|..............xx......
.......xx.............|.............xx.......
........xxx...........|...........xxx........
..........xx..........|..........xx..........
............xx........|........xx............
..............xxx.....|.....xxx..............
----------------xxxxxxxxxxxxx--------------->
......................|......................
......................|......................
......................|......................
......................|......................
......................|......................
......................|......................
......................|......................
......................|......................
......................|......................
......................|......................
......................|......................
......................|......................
```

### Cube functions

```
$ make cub; ./cub
Cube function y=x^3
......................^......................
......................|....................x.
......................|....................x.
......................|...................x..
......................|..................x...
......................|.................x....
......................|................xx....
......................|...............xx.....
......................|..............xx......
......................|.............x........
......................|...........xx.........
......................|........xxx...........
-------------xxxxxxxxxxxxxxxxxxx------------>
...........xxx........|......................
.........xx...........|......................
........x.............|......................
......xx..............|......................
.....xx...............|......................
....xx................|......................
....x.................|......................
...x..................|......................
..x...................|......................
.x....................|......................
.x....................|......................
x.....................|......................
```

## How do I use it?

To use it `term-graph-lib`, simply import the library into your project and call the functions within it.

The functions are listed below:

| Function      | Use case                                       |
| ------------- | ---------------------------------------------- |
| graphCreate   | Create the graph character array and return it |
| graphDraw     | Display the graph character array              |
