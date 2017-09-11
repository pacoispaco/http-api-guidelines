# Guidelines for designing and implementing HTTP API:s

This document contains some notes on designing and implementing REST-ful HTTP
API:s. I started writing this document simply because I felt a need to document
my own slightly confused ideas about how to do REST-ful HTTP API:s. I hope it
can be of value to other developers struggling with the same issues.

## The starting point

> Begin at the beginning and go on till you come to the end; then stop. -- Lewis Carroll 

These guidelines rest (no pun intended) on the following basic premises:

 * **REST is an architectural style for software systems** as conceived and
   described by Roy Fielding in [chapter 5](https://www.ics.uci.edu/%7Efielding/pubs/dissertation/rest_arch_style.htm)
   of his dissertation on *Architectural Styles and the Design of Network-based
   Software Architectures*. REST is **not the software architecture for any
   specific system** and it is **not a technology or a technological standard
   or protocol**. Actual systems that are designed and implemented in accordance
   with REST can be said to be REST-ful.

 * **HTTP is an application level protocol** which is described in the IETF:s
   [RFC 7231](https://tools.ietf.org/html/rfc7231). It is designed to enable
   and facilitate the design and implementation of software systems that are
   REST-ful.
 
 * REST as an architectural style for software systems leaves a whole number of
   practical design and implementation issues open on how to actually implement
   REST-ful systems. HTTP also leaves a number of practical issues open regarding
   how specific systems using HTTP should be implemented and work and especially
   how they should be implemented and work in order to be REST-ful. 

 * The Unix Philosophy as described by Eric S. Raymond in *[Basics of the Unix
   Philosophy](http://www.catb.org/~esr/writings/taoup/html/ch01s06.html)* is
   good.

 * It would be nice to have a set of practical guidelines for using HTTP to 
   design and implement HTTP API:s that enable systems using the HTTP API to
   be REST-ful.
 
 * In the end we always have to think, invent and write code!

The ambition of these guidelines is to use the REST-architectural style together
with the Unix philosophy as a basis for a set of practical design and
implementation choices for HTTP API:s that are REST-ful but, equally important,
pragmatic and simple.

This document is organized into a number of sections, each dealing with a
particular aspect of designing and implementing REST-ful HTTP API:s.

Happy hacking!
