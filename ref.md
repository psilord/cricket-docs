- [Cricket Introduction](#org52acf79)
- [Coherent Noise](#org4a53d38)
- [API](#org600ab96)
  - [Generators](#org334d7bf)
    - [Perlin](#orgacf47e4)
    - [Simplex](#org0930268)
    - [Open-Simplex](#orgd9b3934)
    - [Value](#orgf0c0a3b)
    - [Cellular](#orgd14817b)
    - [Cylinders](#orga993ad5)
    - [Spheres](#orge4044e0)
    - [Checker](#org21c99e9)
    - [Constant](#org215b557)
    - [FBM: Fractal Brownian Motion](#org231f351)
    - [Billow](#org31f652f)
    - [Multifractal](#org5580546)
    - [Hybrid-Multifractal](#orga11e485)
    - [Ridged-Multifractal](#orgc0a8047)
  - [Modifiers](#org481d509)
    - [+](#org14548ef)
    - [-](#orga6e2d0e)
    - [\*](#orga9ba526)
    - [/](#org08bb12e)
    - [abs](#orgeee3419)
    - [blend](#orgb531d66)
    - [cache](#org4213726)
    - [clamp](#orgd90faa9)
    - [curve](#orgf23911d)
    - [displace](#orgfe8e5b4)
    - [expt](#orgfe95634)
    - [fractalize](#org161f621)
    - [max](#org904849f)
    - [negate](#orge1cd4a0)
    - [power](#org0b92ea3)
    - [rotate](#orgfb78a4b)
    - [scale](#orgbfb8c25)
    - [select](#org160da52)
    - [strengthen](#org489a6dd)
    - [terrace](#org2b6e850)
    - [translate](#orgdd81b67)
    - [turbulance](#orgfc65451)
    - [uniform-scale](#orgbbc3b6c)
  - [Map](#org7655689)
    - [define-gradient](#orgf6a6654)
    - [get-image-pixel](#org7a466d3)
    - [image](#org24fb152)
    - [make-map](#orgac077b3)
    - [render-map](#orge367609)
    - [write-image](#org84c2a23)
- [Glossary](#orgd4de3eb)
- [References](#org5798778)
- [Prototyping](#org519dc54)
  - [Org Mode Code Block Examples](#org9caa40b)
  - [Org Mode Wisdom](#org9b68357)
    - [<https://www.gnu.org/software/emacs/refcards/pdf/orgcard.pdf>](#org4b09dfe)
    - [<https://orgmode.org/worg/orgcard.html>](#org3473036)
    - [<https://orgmode.org/manual/Variable-Index.html>](#org82983ab)
    - [C-c C-x C-v - org-toggle-inline-images](#org59446a1)
    - [C-c C-v b - org-babel-execute-buffer.](#org308ce7b)
- [Org Mode Utilities](#org35e23a5)


<a id="org52acf79"></a>

# Cricket Introduction


<a id="org4a53d38"></a>

# Coherent Noise


<a id="org600ab96"></a>

# API


<a id="org334d7bf"></a>

## Generators


<a id="orgacf47e4"></a>

### Perlin

1.  perlin-1d

    1.  Parameter List

    2.  Description

    3.  Example

2.  perlin-2d

    1.  Parameter List

    2.  Description

    3.  Example

3.  perlin-3d

    1.  Parameter List

    2.  Description

    3.  Example

4.  perlin-4d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org0930268"></a>

### Simplex

1.  simplex-1d

    1.  Parameter List

    2.  Description

    3.  Example

2.  simplex-2d

    1.  Parameter List

    2.  Description

    3.  Example

3.  simplex-3d

    1.  Parameter List

    2.  Description

    3.  Example

4.  simplex-4d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="orgd9b3934"></a>

### Open-Simplex

1.  open-simplex-2d

    1.  Parameter List

    2.  Description

    3.  Example

2.  open-simplex-3d

    1.  Parameter List

    2.  Description

    3.  Example

3.  open-simplex-4d

    1.  Parameter List

    2.  Description

    3.  Example

4.  open-simplex2f-2d

    1.  Parameter List

    2.  Description

    3.  Example

5.  open-simplex2f-3d

    1.  Parameter List

    2.  Description

    3.  Example

6.  open-simplex2f-4d

    1.  Parameter List

    2.  Description

    3.  Example

7.  open-simplex2s-2d

    1.  Parameter List

    2.  Description

    3.  Example

8.  open-simplex2s-3d

    1.  Parameter List

    2.  Description

    3.  Example

9.  open-simplex2s-4d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="orgf0c0a3b"></a>

### Value

1.  value-2d

    1.  Parameter List

    2.  Description

    3.  Example

2.  value-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="orgd14817b"></a>

### Cellular

1.  cellular-2d

    1.  Parameter List

    2.  Description

    3.  Example

2.  cellular-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="orga993ad5"></a>

### Cylinders

1.  cylinders-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="orge4044e0"></a>

### Spheres

1.  spheres-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org21c99e9"></a>

### Checker

1.  checker-2d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org215b557"></a>

### Constant

1.  constant

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org231f351"></a>

### FBM: Fractal Brownian Motion

1.  fbm-2d

    1.  Parameter List

    2.  Description

    3.  Example

2.  fbm-3d

    1.  Parameter List

    2.  Description

    3.  Example

3.  fbm-4d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org31f652f"></a>

### Billow

1.  billow-2d

    1.  Parameter List

    2.  Description

    3.  Example

2.  billow-3d

    1.  Parameter List

    2.  Description

    3.  Example

3.  billow-4d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org5580546"></a>

### Multifractal

1.  multifractal-2d

    1.  Parameter List

    2.  Description

    3.  Example

2.  multifractal-3d

    1.  Parameter List

    2.  Description

    3.  Example

3.  multifractal-4d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="orga11e485"></a>

### Hybrid-Multifractal

1.  hybrid-multifractal-2d

    1.  Parameter List

    2.  Description

    3.  Example

2.  hybrid-multifractal-3d

    1.  Parameter List

    2.  Description

    3.  Example

3.  hybrid-multifractal-4d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="orgc0a8047"></a>

### Ridged-Multifractal

1.  ridged-multifractal-2d

    1.  Parameter List

    2.  Description

    3.  Example

2.  ridged-multifractal-3d

    1.  Parameter List

    2.  Description

    3.  Example

3.  ridged-multifractal-4d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org481d509"></a>

## Modifiers


<a id="org14548ef"></a>

### +

1.  Parameter List

2.  Description

3.  Example


<a id="orga6e2d0e"></a>

### -

1.  Parameter List

2.  Description

3.  Example


<a id="orga9ba526"></a>

### \*

1.  Parameter List

2.  Description

3.  Example


<a id="org08bb12e"></a>

### /

1.  Parameter List

2.  Description

3.  Example


<a id="orgeee3419"></a>

### abs

1.  Parameter List

2.  Description

3.  Example


<a id="orgb531d66"></a>

### blend

1.  Parameter List

2.  Description

3.  Example


<a id="org4213726"></a>

### cache

1.  Parameter List

2.  Description

3.  Example


<a id="orgd90faa9"></a>

### clamp

1.  Parameter List

2.  Description

3.  Example


<a id="orgf23911d"></a>

### curve

1.  Parameter List

2.  Description

3.  Example


<a id="orgfe8e5b4"></a>

### displace

1.  Parameter List

2.  Description

3.  Example


<a id="orgfe95634"></a>

### expt

1.  Parameter List

2.  Description

3.  Example


<a id="org161f621"></a>

### fractalize

1.  Parameter List

2.  Description

3.  Example


<a id="org904849f"></a>

### max

1.  Parameter List

2.  Description

3.  Example


<a id="orge1cd4a0"></a>

### negate

1.  Parameter List

2.  Description

3.  Example


<a id="org0b92ea3"></a>

### power

1.  Parameter List

2.  Description

3.  Example


<a id="orgfb78a4b"></a>

### rotate

1.  Parameter List

2.  Description

3.  Example


<a id="orgbfb8c25"></a>

### scale

1.  Parameter List

2.  Description

3.  Example


<a id="org160da52"></a>

### select

1.  Parameter List

2.  Description

3.  Example


<a id="org489a6dd"></a>

### strengthen

1.  Parameter List

2.  Description

3.  Example


<a id="org2b6e850"></a>

### terrace

1.  Parameter List

2.  Description

3.  Example


<a id="orgdd81b67"></a>

### translate

1.  Parameter List

2.  Description

3.  Example


<a id="orgfc65451"></a>

### turbulance

1.  Parameter List

2.  Description

3.  Example


<a id="orgbbc3b6c"></a>

### uniform-scale

1.  Parameter List

2.  Description

3.  Example


<a id="org7655689"></a>

## Map


<a id="orgf6a6654"></a>

### define-gradient


<a id="org7a466d3"></a>

### get-image-pixel


<a id="org24fb152"></a>

### image

1.  image-height

2.  image-width

3.  image-data


<a id="orgac077b3"></a>

### make-map

1.  map-data

2.  map-height

3.  map-value

4.  map-width


<a id="orge367609"></a>

### render-map


<a id="org84c2a23"></a>

### write-image


<a id="orgd4de3eb"></a>

# Glossary


<a id="org5798778"></a>

# References


<a id="org519dc54"></a>

# Prototyping

Remove this entire section when the org more docs are complete.


<a id="org9caa40b"></a>

## Org Mode Code Block Examples

This is an example of how to configure org-mode so that when I execute a block of common lisp the image it generates is places realtime inlined into the org document as appropriate.

```shell
echo "Hello world"
```

```lisp
(ql:quickload :cricket)
(defpackage #:my-package
  (:local-nicknames (#:c #:cricket))
  (:use #:cl))
(in-package #:my-package) ;; <- doesn't affect repl!
```

```lisp
(c:-> (c:checker-2d :seed "example")
  ;;(c:uniform-scale 1/4)
  (c:fractalize :fbm :octaves 3)
  (c:make-map :width 256 :height 256)
  (c:render-map)
  (c:write-image arg))
```

![img](/home/psilord/quicklisp/local-projects/cricket-docs/img/proto/proto-0.png)

Example text.

```lisp
(c:-> (c:perlin-3d :seed "example")
  (c:uniform-scale 1.5)
  (c:fractalize :fbm :frequency 1.3 :octaves 6 :lacunarity 3 :persistence 0.22)
  (c:turbulence (c:open-simplex-3d :seed "foo") :power 1.2 :roughness 4)
  (c:make-map :width 256 :height 256)
  (c:render-map :gradient :terrain)
  (c:write-image arg))
```

![img](/home/psilord/quicklisp/local-projects/cricket-docs/img/proto/proto-1.png)

Documentation retrival test:

The documentation string for PERLIN-2D is:

    Construct a sampler that, when sampled, outputs 2-dimensional Perlin Improved noise values
    ranging from -1.0 to 1.0.

    `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
    supplied, one will be generated automatically which will negatively affect the reproducibility of
    the noise (optional, default: NIL).


<a id="org9b68357"></a>

## Org Mode Wisdom


<a id="org4b09dfe"></a>

### <https://www.gnu.org/software/emacs/refcards/pdf/orgcard.pdf>


<a id="org3473036"></a>

### <https://orgmode.org/worg/orgcard.html>


<a id="org82983ab"></a>

### <https://orgmode.org/manual/Variable-Index.html>


<a id="org59446a1"></a>

### C-c C-x C-v - org-toggle-inline-images

Used to toggle all inline images on and off.


<a id="org308ce7b"></a>

### C-c C-v b - org-babel-execute-buffer.

Execute all code blocks in the buffer and update the results. Must usually


<a id="org35e23a5"></a>

# Org Mode Utilities

The following utility is a post processor to convert the pathname output of C:WRITE-IMAGE which has then been flatted into a string by org mode&#x2013;with the #P included, into a string of just the filename. This is a pure hack that suffices for this one use case. To support C-c C-v b for recomputing all images, we check path to ensure it is valid.