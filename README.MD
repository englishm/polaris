<p align="center">
  <img src="https://github.com/Lartu/polaris/blob/master/IMG/LOGO.PNG">
  <br><br>
  <img src="https://img.shields.io/badge/version-1.0α-blue.svg">
  <img src="https://img.shields.io/badge/apache-_2.0-yellow">
  <a href="https://www.freenode.net"><img src="https://img.shields.io/badge/irc-%23polarislang-navy"></a>
  <a href="https://t.me/polarislang"><img src="https://img.shields.io/badge/-polarislang-295887?logo=telegram"></a>
  <!--<a href="https://travis-ci.org/Lartu/ldpl"><img src="https://img.shields.io/travis/Lartu/ldpl/master"></a>-->
</p>

**Polaris** is a stack-based, interpreted programming language with strings as its only data type.
It has been designed to be **small** in size and **minimal** in language features. **Polaris** was
conceived to run under **MS-DOS** and **Unix** systems, and it consists entirely of a single **.c** file.
The whole interpreter size is under **32 KiB** and it can also be used as an **embeddable language** in
any C or C++ project.

```javascript
/* Polaris Hello World */
("Hello, " @name join print)
>sayHi

"What's your name?: " print
input >name
sayHi%
```

## How to Build Polaris

- If you are on a **Unix** system, clone this repository and then run `cc polaris.c -lm -ansi -pedantic -Wall -o polaris`.
- If you are on a **MS-DOS** system, get [Turbo C](https://edn.embarcadero.com/article/20841). Then from Turbo C open `polaris.c`, change the line `#define OS_TYPE 1` to `#define OS_TYPE 2` and then go to Compile 🡒 Make EXE file. If you get an error stating that the project consists of only one line, change all line breaks in polaris.c (`\n`) to carriage returns + line breaks (`\r\n`).
- If you are on any **other OS**, get your favourite C compiler and build `polaris.c`. Just like that. Polaris is written in strict ANSI C and it should run on any OS that has a C compiler.
- If you want to **embed** Polaris into your own project, include the Polaris source code and then call `eval(<source>);`,
where `<source>` is a C string containing a Polaris script.

## Documentation

The Polaris documentation can be found at www.lartu.net/projects/polaris.

## Roadmap

This is Polaris **1.0α** and it's still under development. There are many features that I'd like to add to the
language that have yet to be implemented. This is a roadmap of them in no particular order:
- [ ] File Reading / Writing
- [x] Random Number Generation
- [ ] Sub-strings
- [ ] String length
- [x] Documentation
- [ ] Functions for easy reading and modifying of Polaris variables from C code.
- [x] Including other source files
- [ ] Sockets
- [X] Pauses
- [x] Escape double quotes in strings
- [X] Flip MS-DOS Switches
- [x] Error message when no file is specified

## Contributing to Polaris

There are many ways to contribute to the Polaris project. You can fix bugs, add issues, write examples,
write software using Polaris, etc. Anything is very welcome. Even telling your colleages about Polaris
is a very easy and useful contribution.

## Getting Help

If you have any questions regarding Polaris you are welcome to submit an [issue](https://github.com/Lartu/polaris/issues) to this repository.

## License

Polaris is distributed under the Apache 2.0 License. The Polaris logo was created by [Lartu](https://github.com/Lartu)
and it is released under a Creative Commons Attribution 4.0 International (CC BY 4.0) license.
