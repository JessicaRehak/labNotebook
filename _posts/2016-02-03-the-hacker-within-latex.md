---
layout: post
title: THW - LaTeX
tags: THW
categories: meeting
---

## Editors:

* Lyx - WYSIWYG Mac editor
* TeXmaker - compiles as you go
* TeXshop

## Writing

* Equation reference used to ref an equation `eqref{}` - what is the
difference between this and normal `ref`? This requires `amsmath`,
apparently it will add parenthesis around the reference.
* If you add double curly braces around fields in `bibtex` it
  will maintain correct capitalization.
* Acronym document: You can make an acronym document that contains
  `\newacronym{TRSO}{TRISO}{Blah blah}`. First field is what you want
  to call in `\gls`, second is the acronym, third is the spelled out acronym. Then use
  (for a file called acros.tex):

    `\include{acros}`

	`\makeglossaries`

  Then use `\gls{acronym}` to spell it out the first time.

* Use package `tabu` to do both column and row wrap.
* `\newcommand{}` : can use this to create new commands, or just text
  that you might want to change throughout the paper, then just run it
  to get the text. So if you update it, it will change. This is good
  for making problem sets if you want to change it year to year
  without having to go through the entire thing and find the issue.
* `exam` document class. Lets you define questions and write solutions
  and assign points. Will tabulate all the points; can choose to print
  the answers or not. `\documentclass[10pt answers]{exam}` will not
  display the answers. Can add conditional statements to add spacing.
