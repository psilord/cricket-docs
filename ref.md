- [Cricket Introduction](#org65e2a72)
- [Coherent Noise](#orge916185)
- [API](#org1025850)
  - [Generators](#org0aaa721)
    - [Perlin](#orgb1bd702)
    - [Simplex](#orgc8dbc35)
    - [Open-Simplex](#orgbac99bb)
    - [Value](#org9316394)
    - [Cellular](#orga3d8f0a)
    - [Cylinders](#org2226f76)
    - [Spheres](#org8d1ffd2)
    - [Checker](#orgdffb91f)
    - [Constant](#orgb517a8b)
    - [FBM: Fractal Brownian Motion](#orge2f3f09)
    - [Billow](#orgcab5257)
    - [Multifractal](#orgac72643)
    - [Hybrid-Multifractal](#org236da07)
    - [Ridged-Multifractal](#org869db2d)
  - [Modifiers](#orgc53f7ec)
    - [+](#orgf218ca4)
    - [-](#org7d66c0e)
    - [\*](#org6a2177e)
    - [/](#org58e003b)
    - [abs](#orgda3d6fb)
    - [blend](#org8ff3388)
    - [cache](#org62921c1)
    - [clamp](#org88019cd)
    - [curve](#orgf334633)
    - [displace](#org9dde60d)
    - [expt](#org3b32cac)
    - [fractalize](#org376b8ea)
    - [max](#orged7b26e)
    - [negate](#org79de906)
    - [power](#orgfb6d1d7)
    - [rotate](#org1526830)
    - [scale](#org6523046)
    - [select](#orgd53b79b)
    - [strengthen](#orga3be9c5)
    - [terrace](#org641dfb7)
    - [translate](#org40625d7)
    - [turbulance](#org36823a9)
    - [uniform-scale](#orgf417611)
  - [Map](#org8928c8c)
    - [define-gradient](#org7b9fab9)
    - [get-image-pixel](#org11c7118)
    - [image](#org01369b3)
    - [make-map](#orga4d91a1)
    - [render-map](#org70c2fe6)
    - [write-image](#org6fdcd7f)
- [Glossary](#orge4f5947)
- [References](#org29fb856)
- [Prototyping](#orge8320f2)
  - [Org Mode Code Block Examples](#orgde68133)
  - [Org Mode Wisdom](#org735796a)
    - [<https://www.gnu.org/software/emacs/refcards/pdf/orgcard.pdf>](#org2909681)
    - [<https://orgmode.org/worg/orgcard.html>](#orgada089b)
    - [<https://orgmode.org/manual/Variable-Index.html>](#orgd0364b7)
    - [C-c C-x C-v - org-toggle-inline-images](#org9c3f813)
    - [C-c C-v b - org-babel-execute-buffer.](#org36b9ef8)
- [Org Mode Utilities](#orgbcc6c45)


<a id="org65e2a72"></a>

# Cricket Introduction


<a id="orge916185"></a>

# Coherent Noise


<a id="org1025850"></a>

# API


<a id="org0aaa721"></a>

## Generators


<a id="orgb1bd702"></a>

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


<a id="orgc8dbc35"></a>

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


<a id="orgbac99bb"></a>

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


<a id="org9316394"></a>

### Value

1.  value-2d

    1.  Parameter List

    2.  Description

    3.  Example

2.  value-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="orga3d8f0a"></a>

### Cellular

1.  cellular-2d

    1.  Parameter List

    2.  Description

    3.  Example

2.  cellular-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org2226f76"></a>

### Cylinders

1.  cylinders-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org8d1ffd2"></a>

### Spheres

1.  spheres-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="orgdffb91f"></a>

### Checker

1.  checker-2d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="orgb517a8b"></a>

### Constant

1.  constant

    1.  Parameter List

    2.  Description

    3.  Example


<a id="orge2f3f09"></a>

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


<a id="orgcab5257"></a>

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


<a id="orgac72643"></a>

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


<a id="org236da07"></a>

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


<a id="org869db2d"></a>

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


<a id="orgc53f7ec"></a>

## Modifiers


<a id="orgf218ca4"></a>

### +

1.  Parameter List

2.  Description

3.  Example


<a id="org7d66c0e"></a>

### -

1.  Parameter List

2.  Description

3.  Example


<a id="org6a2177e"></a>

### \*

1.  Parameter List

2.  Description

3.  Example


<a id="org58e003b"></a>

### /

1.  Parameter List

2.  Description

3.  Example


<a id="orgda3d6fb"></a>

### abs

1.  Parameter List

2.  Description

3.  Example


<a id="org8ff3388"></a>

### blend

1.  Parameter List

2.  Description

3.  Example


<a id="org62921c1"></a>

### cache

1.  Parameter List

2.  Description

3.  Example


<a id="org88019cd"></a>

### clamp

1.  Parameter List

2.  Description

3.  Example


<a id="orgf334633"></a>

### curve

1.  Parameter List

2.  Description

3.  Example


<a id="org9dde60d"></a>

### displace

1.  Parameter List

2.  Description

3.  Example


<a id="org3b32cac"></a>

### expt

1.  Parameter List

2.  Description

3.  Example


<a id="org376b8ea"></a>

### fractalize

1.  Parameter List

2.  Description

3.  Example


<a id="orged7b26e"></a>

### max

1.  Parameter List

2.  Description

3.  Example


<a id="org79de906"></a>

### negate

1.  Parameter List

2.  Description

3.  Example


<a id="orgfb6d1d7"></a>

### power

1.  Parameter List

2.  Description

3.  Example


<a id="org1526830"></a>

### rotate

1.  Parameter List

2.  Description

3.  Example


<a id="org6523046"></a>

### scale

1.  Parameter List

2.  Description

3.  Example


<a id="orgd53b79b"></a>

### select

1.  Parameter List

2.  Description

3.  Example


<a id="orga3be9c5"></a>

### strengthen

1.  Parameter List

2.  Description

3.  Example


<a id="org641dfb7"></a>

### terrace

1.  Parameter List

2.  Description

3.  Example


<a id="org40625d7"></a>

### translate

1.  Parameter List

2.  Description

3.  Example


<a id="org36823a9"></a>

### turbulance

1.  Parameter List

2.  Description

3.  Example


<a id="orgf417611"></a>

### uniform-scale

1.  Parameter List

2.  Description

3.  Example


<a id="org8928c8c"></a>

## Map


<a id="org7b9fab9"></a>

### define-gradient


<a id="org11c7118"></a>

### get-image-pixel


<a id="org01369b3"></a>

### image

1.  image-height

2.  image-width

3.  image-data


<a id="orga4d91a1"></a>

### make-map

1.  map-data

2.  map-height

3.  map-value

4.  map-width


<a id="org70c2fe6"></a>

### render-map


<a id="org6fdcd7f"></a>

### write-image


<a id="orge4f5947"></a>

# Glossary


<a id="org29fb856"></a>

# References


<a id="orge8320f2"></a>

# Prototyping

Remove this entire section when the org more docs are complete.


<a id="orgde68133"></a>

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


<a id="org735796a"></a>

## Org Mode Wisdom


<a id="org2909681"></a>

### <https://www.gnu.org/software/emacs/refcards/pdf/orgcard.pdf>


<a id="orgada089b"></a>

### <https://orgmode.org/worg/orgcard.html>


<a id="orgd0364b7"></a>

### <https://orgmode.org/manual/Variable-Index.html>


<a id="org9c3f813"></a>

### C-c C-x C-v - org-toggle-inline-images

Used to toggle all inline images on and off.


<a id="org36b9ef8"></a>

### C-c C-v b - org-babel-execute-buffer.

Execute all code blocks in the buffer and update the results. Must usually


<a id="orgbcc6c45"></a>

# Org Mode Utilities

The following utility is a post processor to convert the pathname output of C:WRITE-IMAGE which has then been flatted into a string by org mode&#x2013;with the #P included, into a string of just the filename. This is a pure hack that suffices for this one use case. To support C-c C-v b for recomputing all images, we check path to ensure it is valid.

```lisp
;; The 'path' will be the STRING "#P/some/path/name" so I'll extracct out
;; the portion I need as the file name. Used to post process ends of
;; examples that have WRITE-IMAGE at the end.
(format t "~A"
        ;; TODO: convert to COND, make more precise in how it fails and what
        ;; it accepts. Maybe make some more static images to indicate the
        ;; failure condition.
        (if (and path
                 (vectorp path)
                 (> (length path) 2)
                 (string= (subseq path 0 2) "#P"))
            (subseq (namestring path) 2)
            "img/static/broken.png"))
```