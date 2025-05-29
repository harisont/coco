---
title: "Co-constructions in UD"
subtitle: "how to annotate, validate, visualize?"
author: "Arianna Masciolini"
theme: "lucid"
logo: "gu.png"
date: "SpLAn-UD workshop, 29.05.2025"
institute: "Språkbanken, University of Gothenburg"
---

## `whoami`
- PhD student at the University of Gothenburg
- current main focus: treebanking L2 Swedish __essays__
- recent side project: annotation of __interactional__ L2 Italian data (StraParla)
- experience with SpLAn-UD: < 1 week

## A first example
\LARGE
> \color{PrimaryColor} what would you do with \color{SecondaryColor} this sentence

- Speaker A: \color{PrimaryColor} blue
- \color{black}Speaker B: \color{SecondaryColor} orange

## Option 1: splitting by speaker

\bigskip

\setlength{\unitlength}{0.2mm}
\begin{picture}(269.0,110.0)
  \color{PrimaryColor}
  \put(0.0,0.0){what}
  \put(46.0,0.0){would}
  \put(101.0,0.0){you}
  \put(147.0,0.0){do}
  \put(193.0,0.0){with}
  \color{black}
  \put(0.0,15.0){{\tiny PRON}}
  \put(46.0,15.0){{\tiny AUX}}
  \put(101.0,15.0){{\tiny PRON}}
  \put(147.0,15.0){{\tiny VERB}}
  \put(193.0,15.0){{\tiny ADP}}
  \put(83.5,30.0){\oval(144.9591836734694,100.0)[t]}
  \put(11.020408163265301,35.0){\vector(0,-1){5.0}}
  \put(76.75,83.0){{\tiny obj}}
  \put(106.5,30.0){\oval(98.02970297029702,66.66666666666667)[t]}
  \put(57.48514851485149,35.0){\vector(0,-1){5.0}}
  \put(99.75,66.33333333333334){{\tiny aux}}
  \put(134.0,30.0){\oval(39.47826086956522,33.333333333333336)[t]}
  \put(114.26086956521739,35.0){\vector(0,-1){5.0}}
  \put(122.75,49.66666666666667){{\tiny nsubj}}
  \put(162.0,110.0){\vector(0,-1){80.0}}
  \put(167.0,100.0){{\tiny root}}
  \put(190.0,30.0){\oval(39.47826086956522,33.333333333333336)[t]}
  \put(209.73913043478262,35.0){\vector(0,-1){5.0}}
  \put(183.25,49.66666666666667){{\tiny \bfseries ?}}
\end{picture}


\vspace{4mm}
\setlength{\unitlength}{0.2mm}
\begin{picture}(128.0,70.0)
  \color{SecondaryColor}
  \put(0.0,0.0){this}
  \put(46.0,0.0){sentence}
  \color{black}
  \put(0.0,15.0){{\tiny DET}}
  \put(46.0,15.0){{\tiny NOUN}}
  \put(33.0,30.0){\oval(39.47826086956522,33.333333333333336)[t]}
  \put(13.26086956521739,35.0){\vector(0,-1){5.0}}
  \put(26.25,49.66666666666667){{\tiny det}}
  \put(61.0,70.0){\vector(0,-1){40.0}}
  \put(66.0,60.0){{\tiny root}}
\end{picture}

- how meaningful is this annotation?
- what to do with "with"?

## Option 2: single sentence
\setlength{\unitlength}{0.2mm}
\begin{picture}(417.0,110.0)
  \color{PrimaryColor}
  \put(0.0,0.0){what}
  \put(46.0,0.0){would}
  \put(101.0,0.0){you}
  \put(147.0,0.0){do}
  \put(193.0,0.0){with}
  \color{SecondaryColor}
  \put(239.0,0.0){this}
  \put(285.0,0.0){sentence}
  \color{black}
  \put(0.0,15.0){{\tiny PRON}}
  \put(46.0,15.0){{\tiny AUX}}
  \put(101.0,15.0){{\tiny PRON}}
  \put(147.0,15.0){{\tiny VERB}}
  \put(193.0,15.0){{\tiny ADP}}
  \put(239.0,15.0){{\tiny DET}}
  \put(285.0,15.0){{\tiny NOUN}}
  \put(83.5,30.0){\oval(144.9591836734694,100.0)[t]}
  \put(11.020408163265301,35.0){\vector(0,-1){5.0}}
  \put(76.75,83.0){{\tiny obj}}
  \put(106.5,30.0){\oval(98.02970297029702,66.66666666666667)[t]}
  \put(57.48514851485149,35.0){\vector(0,-1){5.0}}
  \put(99.75,66.33333333333334){{\tiny aux}}
  \put(134.0,30.0){\oval(39.47826086956522,33.333333333333336)[t]}
  \put(114.26086956521739,35.0){\vector(0,-1){5.0}}
  \put(122.75,49.66666666666667){{\tiny nsubj}}
  \put(162.0,110.0){\vector(0,-1){80.0}}
  \put(167.0,100.0){{\tiny root}}
  \put(249.0,30.0){\oval(88.73913043478261,66.66666666666667)[t]}
  \put(204.6304347826087,35.0){\vector(0,-1){5.0}}
  \put(240.0,66.33333333333334){{\tiny case}}
  \put(272.0,30.0){\oval(39.47826086956522,33.333333333333336)[t]}
  \put(252.26086956521738,35.0){\vector(0,-1){5.0}}
  \put(265.25,49.66666666666667){{\tiny det}}
  \put(236.0,30.0){\oval(135.82608695652175,100.0)[t]}
  \put(303.9130434782609,35.0){\vector(0,-1){5.0}}
  \put(229.25,83.0){{\tiny obl}}
\end{picture}

(with speaker IDs in the MISC field)

- complete sentence
- easy-to-visualize co-construction

## Pile-like constructions
\LARGE
> \color{PrimaryColor} here comes a more difficult case
> \color{white} --------------- \color{SecondaryColor} another example

\large \color{PrimaryColor} A \color{black} and \color{SecondaryColor} B \color{black}: 

- fill in the same slot with different values
- typically (but not necessarily) overlap

## Option 1: splitting by speaker
\vspace{4mm}
\setlength{\unitlength}{0.2mm}
\begin{picture}(361.0,110.0)
  \color{PrimaryColor}
  \put(0.0,0.0){here}
  \put(46.0,0.0){comes}
  \put(101.0,0.0){a}
  \put(138.0,0.0){more}
  \put(184.0,0.0){difficult}
  \put(275.0,0.0){case}
  \color{black}
  \put(0.0,15.0){{\tiny ADV}}
  \put(46.0,15.0){{\tiny VERB}}
  \put(101.0,15.0){{\tiny DET}}
  \put(138.0,15.0){{\tiny ADV}}
  \put(184.0,15.0){{\tiny ADJ}}
  \put(275.0,15.0){{\tiny NOUN}}
  \put(33.0,30.0){\oval(39.47826086956522,33.333333333333336)[t]}
  \put(13.26086956521739,35.0){\vector(0,-1){5.0}}
  \put(19.5,49.66666666666667){{\tiny advmod}}
  \put(61.0,110.0){\vector(0,-1){80.0}}
  \put(66.0,100.0){{\tiny root}}
  \put(198.0,30.0){\oval(172.27586206896552,66.66666666666667)[t]}
  \put(111.86206896551724,35.0){\vector(0,-1){5.0}}
  \put(191.25,66.33333333333334){{\tiny det}}
  \put(171.0,30.0){\oval(39.47826086956522,33.333333333333336)[t]}
  \put(151.26086956521738,35.0){\vector(0,-1){5.0}}
  \put(157.5,49.66666666666667){{\tiny advmod}}
  \put(239.5,30.0){\oval(87.7032967032967,33.333333333333336)[t]}
  \put(195.64835164835165,35.0){\vector(0,-1){5.0}}
  \put(230.5,49.66666666666667){{\tiny amod}}
  \put(180.5,30.0){\oval(227.68995633187774,100.0)[t]}
  \put(294.34497816593887,35.0){\vector(0,-1){5.0}}
  \put(169.25,83.0){{\tiny nsubj}}
\end{picture}

\setlength{\unitlength}{0.2mm}
\begin{picture}(146.0,70.0)
  \color{SecondaryColor}
  \put(0.0,0.0){another}
  \put(73.0,0.0){example}
  \color{black}
  \put(0.0,15.0){{\tiny DET}}
  \put(73.0,15.0){{\tiny NOUN}}
  \put(46.5,30.0){\oval(68.89041095890411,33.333333333333336)[t]}
  \put(12.054794520547944,35.0){\vector(0,-1){5.0}}
  \put(39.75,49.66666666666667){{\tiny det}}
  \put(88.0,70.0){\vector(0,-1){40.0}}
  \put(93.0,60.0){{\tiny root}}
\end{picture}

## Option 2: `reparandum`
\setlength{\unitlength}{0.2mm}
\begin{picture}(527.0,110.0)
  \color{PrimaryColor}
  \put(0.0,0.0){here}
  \put(46.0,0.0){comes}
  \put(101.0,0.0){a}
  \put(138.0,0.0){more}
  \put(184.0,0.0){difficult}
  \put(275.0,0.0){case}
  \color{SecondaryColor}
  \put(321.0,0.0){another}
  \put(394.0,0.0){example}
  \color{black}
  \put(0.0,15.0){{\tiny ADV}}
  \put(46.0,15.0){{\tiny VERB}}
  \put(101.0,15.0){{\tiny DET}}
  \put(138.0,15.0){{\tiny ADV}}
  \put(184.0,15.0){{\tiny ADJ}}
  \put(275.0,15.0){{\tiny NOUN}}
  \put(321.0,15.0){{\tiny DET}}
  \put(394.0,15.0){{\tiny NOUN}}
  \put(33.0,30.0){\oval(39.47826086956522,33.333333333333336)[t]}
  \put(13.26086956521739,35.0){\vector(0,-1){5.0}}
  \put(19.5,49.66666666666667){{\tiny advmod}}
  \put(61.0,110.0){\vector(0,-1){80.0}}
  \put(66.0,100.0){{\tiny root}}
  \put(198.0,30.0){\oval(172.27586206896552,66.66666666666667)[t]}
  \put(111.86206896551724,35.0){\vector(0,-1){5.0}}
  \put(191.25,66.33333333333334){{\tiny det}}
  \put(171.0,30.0){\oval(39.47826086956522,33.333333333333336)[t]}
  \put(151.26086956521738,35.0){\vector(0,-1){5.0}}
  \put(157.5,49.66666666666667){{\tiny advmod}}
  \put(239.5,30.0){\oval(87.7032967032967,33.333333333333336)[t]}
  \put(195.64835164835165,35.0){\vector(0,-1){5.0}}
  \put(230.5,49.66666666666667){{\tiny amod}}
  \put(344.5,30.0){\oval(116.47899159663865,66.66666666666667)[t]}
  \put(286.26050420168065,35.0){\vector(0,-1){5.0}}
  \put(322.0,66.33333333333334){{\tiny \bfseries reparandum}}
  \put(367.5,30.0){\oval(68.89041095890411,33.333333333333336)[t]}
  \put(333.05479452054794,35.0){\vector(0,-1){5.0}}
  \put(360.75,49.66666666666667){{\tiny det}}
  \put(240.0,30.0){\oval(347.13793103448273,100.0)[t]}
  \put(413.5689655172414,35.0){\vector(0,-1){5.0}}
  \put(228.75,83.0){{\tiny nsubj}}
\end{picture}

- makes sense if \color{SecondaryColor} B \color{black} is correcting \color{PrimaryColor} A\color{black}
- \...but that is not always the case

## Option 3: double subject
\bigskip
\bigskip

\setlength{\unitlength}{0.2mm}
\begin{picture}(527.0,130.0)
  \color{PrimaryColor}
  \put(0.0,0.0){here}
  \put(46.0,0.0){comes}
  \put(101.0,0.0){a}
  \put(138.0,0.0){more}
  \put(184.0,0.0){difficult}
  \put(275.0,0.0){case}
  \color{SecondaryColor}
  \put(321.0,0.0){another}
  \put(394.0,0.0){example}
  \color{black}
  \put(0.0,15.0){{\tiny ADV}}
  \put(46.0,15.0){{\tiny VERB}}
  \put(101.0,15.0){{\tiny DET}}
  \put(138.0,15.0){{\tiny ADV}}
  \put(184.0,15.0){{\tiny ADJ}}
  \put(275.0,15.0){{\tiny NOUN}}
  \put(321.0,15.0){{\tiny DET}}
  \put(394.0,15.0){{\tiny NOUN}}
  \put(33.0,30.0){\oval(39.47826086956522,33.333333333333336)[t]}
  \put(13.26086956521739,35.0){\vector(0,-1){5.0}}
  \put(19.5,49.66666666666667){{\tiny advmod}}
  \put(61.0,130.0){\vector(0,-1){100.0}}
  \put(66.0,120.0){{\tiny root}}
  \put(198.0,30.0){\oval(172.27586206896552,66.66666666666667)[t]}
  \put(111.86206896551724,35.0){\vector(0,-1){5.0}}
  \put(191.25,66.33333333333334){{\tiny det}}
  \put(171.0,30.0){\oval(39.47826086956522,33.333333333333336)[t]}
  \put(151.26086956521738,35.0){\vector(0,-1){5.0}}
  \put(157.5,49.66666666666667){{\tiny advmod}}
  \put(239.5,30.0){\oval(87.7032967032967,33.333333333333336)[t]}
  \put(195.64835164835165,35.0){\vector(0,-1){5.0}}
  \put(230.5,49.66666666666667){{\tiny amod}}
  \put(180.5,30.0){\oval(227.68995633187774,100.0)[t]}
  \put(294.34497816593887,35.0){\vector(0,-1){5.0}}
  \put(169.25,83.0){{\tiny \bfseries nsubj}}
  \put(367.5,30.0){\oval(68.89041095890411,33.333333333333336)[t]}
  \put(333.05479452054794,35.0){\vector(0,-1){5.0}}
  \put(360.75,49.66666666666667){{\tiny det}}
  \put(240.0,30.0){\oval(347.13793103448273,133.33333333333334)[t]}
  \put(413.5689655172414,35.0){\vector(0,-1){5.0}}
  \put(228.75,99.66666666666667){{\tiny \bfseries nsubj}}
\end{picture}

- intuitive analysis
- problem:
  \small
  ```
  [Line 55 Node 2]: [L3 Syntax too-many-subjects] 
  Multiple subjects [6, 8] not subtyped as ':outer'. 
  Outer subjects are allowed if a clause acts as the 
  predicate of another clause.
  ```

## Some considerations
- if spoken data is segmented in a speaker-based fashion, some information is inevitably lost or hidden (at least from current UD tools)
- if multi-speaker (co-constructed) "sentences" are allowed, the validator needs to account for speaker information