# WASI Filesystem

A proposed [WebAssembly System Interface](https://github.com/WebAssembly/WASI) API.

### Current Phase

Phase 2

### Champions

- Dan Gohman

### Phase 4 Advancement Criteria

 - Two independent implementations.
 - At least one host implementation on each of:
    - Linux
    - macOS
    - Windows

## Table of Contents

- [Introduction](#introduction)
- [Goals](#goals)
- [Non-goals](#non-goals)
- [API walk-through](#api-walk-through)
- [Detailed design discussion](#detailed-design-discussion)
- [Stakeholder Interest & Feedback](#stakeholder-interest--feedback)
- [References & acknowledgements](#references--acknowledgements)

### Introduction

WASI filesystem provides POSIX-like APIs for accessing traditional
filesystem resources in traditional ways.

### Goals

WASI filesystem aims to be highly compatible with POSIX, so that it's easy
to port existing code to use it, and it's easy to implement, at least on
POSIX systems. To better support Windows, WASI filesystem doesn't insist on
strict POSIX compliance in several respects.

### Non-goals

WASI filesystem is not aiming to be a universal data storage API. Filesystems
have numerous inherent limitations, and WASI filesystem is not attempting to
solve them.

And, Windows and POSIX-like platforms have numerous behavioral differences.
Some of these differences can be hidden, but many cannot, and WASI filesystem
does not attempt to hide most of them.

### API walk-through

TODO

### Detailed design discussion

TODO

### Stakeholder Interest & Feedback

There are currently several major WASI implementations of the WASI filesystem
API. It provides the basis for implementing `getentropy` in wasi-libc, and it's
widely used.

### References & acknowledgements

Many thanks for valuable feedback and advice from:

TODO
