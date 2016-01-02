# Tessellated Intelligence System Best Practices - Patterns of Node Communication

An (eventually) comprehensive spoiler for [Zachtronics'](http://www.zachtronics.com/) [TIS-100](http://www.zachtronics.com/tis-100/)

## About

This is a collection of notes on the TIS-100 architecture, optimization techniques, and annotated solutions to some of the easier problems.

## Part I: General Information

### [Chapter 1: Implementation Details](chapter01.md)

This chapter documents various syntax quirks and undefined behaviors, such as integer overflows (everything is clipped to +/- 999), segfaults (can't happen), and multiple simultaneous reads and writes to a Stack Memory Node.

### [Chapter 2: Instruction Timings](chapter02.md)

In short: writing to a port takes two cycles (or more if it blocks) unless a Stack Memory Node is doing the writing; reading from a port takes one cycle (or more if it blocks); everything else takes one cycle.

## Part II: TIS-100 Spoilers

### [Chapter 3: Self-Test Diagnostic through Signal Multiplexer](chapter03.md)

An introduction to loops, parallelization using `ANY`, and `switch` statements with `JRO`.

### [Chapter 4: Sequence Generator through Interrupt Handler](chapter04.md)

Pipelining: it's like parallelism, but in series!

### [Chapter 5: Signal Pattern Detector through Signal Multiplier](chapter05.md)

State machines; avoiding gratuitous `SWP/SAV`s; preventing stack underflows without using a counter.

### [Chapter 6: Image Test Pattern 1 through Histogram Viewer](chapter06.md)

Pretty pictures!

### [Chapter 7: Signal Window Filter through Sequence Sorter](chapter07.md)

A crash course in algorithms.

### [Chapter 8: [REDACTED] and [REDACTED]](chapter08.md)

[REDACTED]

## Part III: TIS-NET Spoilers

## Authors

[George Schaertl](https://github.com/kk4ead) (KK4EAD)

[CaitSith2](https://github.com/CaitSith2) -- many optimized solutions

## License

CC BY-SA 4.0

[Next](chapter01.md)
