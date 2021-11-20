# awesome-low-level-programming-languages

A curated list of low level programming languages primarily aimed and OS and game
programming.

Excluded are languages relying on managed run-times and garbage collection.


Table of content

- [ATS](#ATS)
- [Ada](#Ada)
- [C](#C)
- [C++](#C++)
- [C3](#C3)
- [Carp](#Carp)
- [Cone](#Cone)
- [D](#D)
- [Forth](#Forth)
- [Jai](#Jai)
- [Nim](#Nim)
- [Oberon](#Oberon)
- [Odin](#Odin)
- [Rust](#Rust)
- [Vala](#Vala)
- [V](#V)
- [Zig](#Zig)

## ATS

* main: http://www.ats-lang.org/
* repo: https://github.com/ats-lang
* documentation:
  - http://ats-lang.sourceforge.net/DOCUMENT/INT2PROGINATS/HTML/book1.html
  - http://www.ats-lang.org/Documents.html
* implementation-language: ATS
* meta-prgramming: TODO
* backends: C
* major projects using the language: TODO
* syntax: functional style
* highlights:
  - proofs, dependent types

```
#include "share/atspre_staload.hats"
#include "share/atspre_staload_libats_ML.hats"

implement
main0() = println! ("Hello, world!")
```

```
fun fibc (n: int) : int = let
  fun loop(n: int, f0: int, f1: int): int =
    if n > 0 then loop(n-1, f1, f0+f1) else f0
  end of [loop]
in
  loop(n, 0, 1)
end // end of [fibc]
```

## Ada

* main: TODO
* repo: TODO
* documentation:
  - awesome-ada https://github.com/ohenley/awesome-ada
  - https://learn.adacore.com/
  - http://groups.umd.umich.edu/cis/course.des/cis400/ada/ada.html
* meta-prgramming: generics
* backends: gcc (gnat), several commerical implementations
* major projects using the language: numerous
* syntax: begin/end, type to the right of identifier
* highlights:
  - design by contract

```
with Ada.Text_IO;

procedure Hello_World is
begin
   Ada.Text_IO.Put_Line ("Hello World");
end Hello_World;
```

```
function fibonacci(n : in integer) return integer is
    f1, f2, fib : integer;
 begin
    f1 := 1;
    f2 := 1;
    for i in 3..n loop
       fib := f1 + f2;
       f1 := f2;
       f2 := fib;
    end loop;
    return fib;
 end fibonacci;
```

## C

* main: TODO
* repo: TODO
* documentation:
  - https://github.com/inputsh/awesome-c
  - https://github.com/uhub/awesome-c
* hello-world: https://en.wikipedia.org/wiki/%22Hello,_World!%22_program#C
* meta-prgramming: pre-processor
* backends: llvm, gcc, numerous others
* major projects using the language: numerous
* syntax: curly braces, type to the left of identifier
* highlights:
  - ubiquitous
  - often used as a backend
  - no namespaces
  - array to pointer auto conversion
  - no defer (or RAII) mechanism
  - lots of undefined / implementation defined behavior

```
#include <stdio.h>

int main(void) 
{
  printf("Hello World!");
}
```

```
int fib(int n) {
    int a = 0;
    int b = 1;
    for (int i = 0; i <= n; i++) {
       int c = a + b;
       a = b;
       b = c;
    }
    return a;
}
```


## C++
* repo:
* documentation:
  - standard https://isocpp.org/std/the-standard
  - reference https://en.cppreference.com/w/
  - awesome-cpp https://github.com/fffaraz/awesome-cpp
  - AwesomePerfCpp https://github.com/fenbf/AwesomePerfCpp
* meta-prgramming:
* backends:  llvm, gcc, numerous others
* major projects using the language: numerous
* syntax: curly braces, type to the left of identifier
* highlights:
  - curly braces, type to the left of identifier
  - large language

```
#include <iostream>

int main() 
{
  std::cout << "Hello World!" << std::endl;
}

```

```
int fib(int n) {
    int a = 0;
    int b = 1;
    for (int i = 0; i <= n; i++) {
       int c = a + b;
       a = b;
       b = c;
    }
    return a;
}
```

## C3

* main: http://www.c3-lang.org/
* repo: https://github.com/c3lang/c3c
* documentation:
  - http://www.c3-lang.org/compare/
* implementation-language: C
* hello-world: http://www.c3-lang.org/firstproject/
* meta-prgramming: generics, semantic macros
* backends: LLVM
* major projects using the language: numerous
* syntax: curly braces, type to the left of identifier
* highlights:
  - evolution of C
  - contracts

```
module hello_world;

import std::io;

fn int main(int argc, char** argv) {
    io::println("Hello World!");
    return 0;
}

```

```
TODO
```

## Carp

* main: https://github.com/carp-lang/Carp
* repo: https://github.com/carp-lang/Carp
* documentation:
  - language guide: https://github.com/carp-lang/Carp/blob/master/docs/LanguageGuide.md
* implementation-language: Haskel
* meta-prgramming: generics
* backends: TODO
* major projects using the language:
* syntax: Lisp like
* highlights:
  - repl
  - ownership tracking

```
import stdio

fn main():
  print <- "Hello world!"
```

```
TODO
```

## Cone

* main: https://cone.jondgoodwin.com/
* repo: https://github.com/jondgoodwin/cone
* documentation:
  - reference: https://cone.jondgoodwin.com/coneref/index.html
* implementation-language: C
* meta-prgramming: macros, generics
* backends: LLVM
* major projects using the language:
* syntax: type to the right of identifier
* highlights:
  - proofs, dependent types
  - co-routines, threads and actors

```
import stdio

fn main():
  print <- "Hello world!"
```

```
TODO

```

## D

* main: https://dlang.org/
* repo: https://github.com/dlang
* documentation:
  - spec https://dlang.org/spec/spec.html
  - overview https://dlang.org/comparison.html
* implementation-language: D
* meta-prgramming: generics
* backends: custom, LLVM
* major projects using the language: numerous
* syntax: curly braces, type to the left of identifier
* highlights:
  - large language

```
import std.stdio;

void main() {
    writeln("Hello, World!");
}
```

```
TODO
```

## Forth

* main: TODO
* repo: TODO
* documentation:
  - http://www.forth.org/
* implementation-language: C, assembler, 
* meta-prgramming: TODO
* backends: Custom
* major projects using the language: TODO
* syntax: unique
* highlights:
 - concatenative programing style
 - many different flavors
 - very easy to implement
 
```
: HELLO ."Hello World " ;

```

```
: FIB ( x -- y ) RECURSIVE
	DUP 2 > IF DUP  1- RECURSE 
		   SWAP 2- RECURSE +  EXIT 
	     ENDIF 
	DROP 1 ;
```

## Jai

* main: TODO
* repo: TODO
* documentation:
  - inofficial https://inductive.no/jai/
  - inofffical https://github.com/BSVino/JaiPrimer/blob/master/JaiPrimer.md
  - Jonathan Blow YT channel https://www.youtube.com/user/jblow888/videos
* implementation-language: C++
* meta-prgramming: macros
* backends: LLVM (?), Custom
* major projects using the language: TODO
* syntax: TODO 
* highlights:
  - compile time execution

```
TODO
```

```
TODO
```

## Nim

* main: https://nim-lang.org/
* repo: https://github.com/nim-lang/Nim
* documentation:
  - https://nim-lang.org/documentation.html
* implementation-language: Nim
* hello-world: https://nim-by-example.github.io/hello_world/
* meta-prgramming: hygienic macro system allows direct manipulation of AST
* backends: C(++), JS
* major projects using the language: TODO
* syntac: python inspired syntax (indentation based)
* highlights:
  - optional GC
  - lifetime tracking
  - largish language

```
echo "Hello World"

```

```
TODO
```


## Oberon-2

* main: http://www.projectoberon.com
* note: Oberon is not just a language but a full system (OS, even HW) 
* repo: TODO
* documentation:
  - spec http://cas.inf.ethz.ch/projects/a2/repository/raw/trunk/LanguageReport/OberonLanguageReport.pdf 
  - http://www.projectoberon.com
  - http://www.ethoberon.ethz.ch/WirthPubl/ProjectOberon.pdf
  - [System](https://inf.ethz.ch/personal/wirth/ProjectOberon/PO.System.pdf)
    [Application](https://inf.ethz.ch/personal/wirth/ProjectOberon/PO.Applications.pdf)
    [Computer](https://inf.ethz.ch/personal/wirth/ProjectOberon/PO.Computer.pdf)
* implementation-language: Oberon
* hello-world: http://groups.umd.umich.edu/cis/course.des/cis400/oberon/hworld.html
* meta-prgramming: None
* backends: Custom
* major projects using the language: Oberon-OS
* syntax: begin/end, type to the right of identifier
* highlights:
  - deliberate small language

```
MODULE Hello;
         IMPORT Oberon, Texts;
  VAR W: Texts.Writer;
  
  PROCEDURE World*;
  BEGIN
    Texts.WriteString(W, "Hello World!");
    Texts.WriteLn(W);
    Texts.Append(Oberon.Log, W.buf);
  END World;

BEGIN
  Texts.OpenWriter(W);
END Hello.
```

```
TODO
```

## Odin

* main: https://odin-lang.org/
* repo: https://github.com/odin-lang/Odin
* documentation:
  - spec https://odin-lang.org/docs/spec/
  - https://www.youtube.com/channel/UCUSck1dOH7VKmG4lRW7tZXg
* implementation-language: C++
* meta-prgramming: generics
* backends: LLVM
* major projects using the language: TODO 
* syntax: curly braces, type to the right of identifier
* highlights:
  - implcit context parameter 

```
package main

import "core:fmt"

main :: proc() {
	fmt.println("Hellope!")
}

```

```
fibonacci :: proc(n: int) -> int {
  switch {
  case n < 1:
    return 0
  case n == 1:
    return 1
  }
  return fibonacci(n-1) + fibonacci(n-2)
}

```

## Rust

* main: https://www.rust-lang.org/
* repo: https://github.com/rust-lang
* documentation:
  - https://doc.rust-lang.org/book/
* implementation-language: V  
* meta-prgramming: hygienic macros
* backends: LLVM
* major projects using the language: numerous (including large parts of firefox)
* syntax: curly braces, type to the right of identifier
* highlights:
  - memory safety focus (ownership semantics)
  - bare metal programming via `no_std` environment
  - steep learning curve
  - large language
  - slow compiles

```
fn main() {
    println!("Hello World!");
}
```

```
fn fibonacci(n: u32) -> u32 {
    match n {
        0 => 1,
        1 => 1,
        _ => fibonacci(n - 1) + fibonacci(n - 2),
    }
}
```

## V

* main: https://vlang.io/
* repo: https://github.com/vlang
* documentation:
  - https://github.com/vlang/v/blob/master/doc/docs.md
* implementation-language: V
* meta-prgramming: generics
* backends: C, LLVM
* major projects using the language: TODO
* syntax: curly braces, type to the right of identifier
* highlights:
  - go derived syntax
  - some confusion around memory-allocators and GC ("autofree")

```
fn main() {
  println('Hello, World!')
}
```

```
fn fn(n int) int {
  mut a := 0
  mut b := 1
  for _ in 0 .. n {
    c := a + b
    a = b
    b = c
  }
  return a
}
```

## Vale

* main: https://vale.dev/
* repo: https://github.com/ValeLang/Vale
* documentation:
  - introduction https://vale.dev/guide/introduction
* implementation-language: Vale, Scala
* meta-prgramming: generics
* backends:
* major projects using the language: TODO
* syntax: curly braces, type to the right of identifier
* highlights:
  - ownership semantics

```
fn main() export {
  println("Hello world!");
}
```

```
TODO
```

## Zig

* main: https://ziglang.org
* repo: https://github.com/ziglang/zig
* documentation:
  - https://ziglang.org/documentation/master/
* implementation-language: C++, Zig
* hello-world: https://ziglang.org/documentation/master/
* meta-prgramming: comptime (including types) 
* backends: LLVM, custom
* major projects using the language: TODO
* syntax: curly braces, type to the right of identifier
* highlights:
  - small language
  - no invisible control-flow

```
const std = @import("std");

pub fn main() !void {
    const stdout = std.io.getStdOut().writer();
    try stdout.print("Hello, {s}!\n", .{"world"});
}

```

```
fn fibonacci(index: u32) u32 {
    if (index < 2) return index;
    return fibonacci(index - 1) + fibonacci(index - 2);
}
```

<!--
## Template

* main:
* repo:
* documentation:
* implementation-language:
* hello-world:
* meta-prgramming:
* backends:
* major projects using the language
* syntax:
* highlights:
-->
