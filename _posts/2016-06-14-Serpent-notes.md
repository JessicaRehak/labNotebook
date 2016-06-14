---
layout: post
title: Serpent 2, Day 1
categories: entry
tags: serpent, code, INL
---

Note: I need to add a reference section to this site for myself for
building a library of knowledge when learning about a new code. It'd
be better than a notebook for compiling something that isn't inherently organized
(like a book).

# Serpent compilation

Serpent 2 finally compiled, steps required:

1. Install clang-omp with brew
2. Symbolic link the standard C libraries from where OS X hides them
to `/usr/local/include/standard`
3. Added to makefile:
```
CC       = /usr/local/Cellar/clang-omp/2015-04-01/bin/clang-omp -I
/usr/local/include/standard -I /usr/local/include/libiomp
```
  In retrospect, I see that homebrew puts (what I assume is) a symbolic
  link in `/usr/local/bin`, so I can just use that next time.
4. Commented out GD libraries <- what are these?

# Serpent Notes:

## header.h

- include statements
- Constants: code name, neutron mass, etc
- Max array sizes
- Flags
- Structs
- Function prototypes

### Global arrays and Variables

* **WDB**: writable main datablock; main data, geometry, pointers,
  calc parameters
* **RDB**: pointer to WDB, type-cast to double: prevents editing
  something that isn't a double via compiler warning
* **PRV**: OpenMP private values
* **BUF**: buffer for cycle/batch data for statistics
* **RES1**: results array -> statistics
* **RES2**: results array 2 -> tables of integral data
* **ASCII**: array for storing text
* **ACE**: stores cross-sections and nuclide data, this is freed up
  prior to transport cycle

## tracking.c

Main particle tracking.

If using delta tracking, calls `trk = MoveDT`

## trackmode.c

**Called by:** tracking.c

Determines if delta-tracking or surface-tracking is used for the next
pathlength.

`RDB[DATA_DT_ENFORCE_NEXT_TRACK`: if this is `YES`, will force delta tracking

`RDB[DATA_DT_NTHRESH]`: delta tracking threshold, set to 0.1 in
`initdata.c`. There is a different value for other particles.

`return TRACK_MODE_DT;`: delta track on next collision

`return TRACK_MODE_ST;`: surface track on next collision

## MoveDT.c


