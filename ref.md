- [Cricket Introduction](#orgea151df)
- [Coherent Noise](#org10d1198)
- [API](#org3e0dc1c)
  - [Generators](#orgc0f7fec)
    - [Perlin](#orge4861a0)
    - [Simplex](#org9bd7186)
    - [Open-Simplex](#orgdba888f)
    - [Value](#orgba435b3)
    - [Cellular](#orgdff5ced)
    - [Cylinders](#org6730c2c)
    - [Spheres](#org00aa0df)
    - [Checker](#org0ea5031)
    - [Constant](#orgb067255)
    - [FBM: Fractal Brownian Motion](#orgfea4358)
    - [Billow](#org0795970)
    - [Multifractal](#orgb5a5c3d)
    - [Hybrid-Multifractal](#org95c9a45)
    - [Ridged-Multifractal](#orga139655)
  - [Modifiers](#orgefaa847)
    - [+](#org3a7cb87)
    - [-](#org1a0581f)
    - [\*](#org62b8b86)
    - [/](#org6c0c552)
    - [abs](#orgc3bcd1c)
    - [blend](#org7d53eee)
    - [cache](#org56ca270)
    - [clamp](#org68dab80)
    - [curve](#org97d3cd7)
    - [displace](#orgdb33892)
    - [expt](#org40a468a)
    - [fractalize](#org8653483)
    - [max](#orgedb3d2f)
    - [negate](#org2fdc2db)
    - [power](#orgc5551d6)
    - [rotate](#org8977706)
    - [scale](#org00e3251)
    - [select](#org47b30c2)
    - [strengthen](#orgecd3bd6)
    - [terrace](#org559d0e9)
    - [translate](#orgf045b0f)
    - [turbulance](#orgcc8ef4f)
    - [uniform-scale](#orgaf6add7)
  - [Map](#org7062baf)
    - [define-gradient](#org1c442a8)
    - [get-image-pixel](#org7eb1770)
    - [image](#orgcf4a6d8)
    - [make-map](#orgef386a9)
    - [render-map](#orgb7db437)
    - [write-image](#orgcea8b6f)
- [Glossary](#orgc6f4d58)
- [References](#org1284e81)
- [Prototyping](#org7f21719)
  - [Org Mode Code Block Examples](#orgc54c8d6)
  - [Org Mode Wisdom](#org49ddc2e)
    - [<https://www.gnu.org/software/emacs/refcards/pdf/orgcard.pdf>](#org439f748)
    - [<https://orgmode.org/worg/orgcard.html>](#orgb35d1ec)
    - [<https://orgmode.org/manual/Variable-Index.html>](#org6d0f571)
    - [C-c C-x C-v - org-toggle-inline-images](#orge757164)
    - [C-c C-v b - org-babel-execute-buffer.](#org7536cc8)
- [Org Mode Utilities](#org65786ab)


<a id="orgea151df"></a>

# Cricket Introduction


<a id="org10d1198"></a>

# Coherent Noise


<a id="org3e0dc1c"></a>

# API


<a id="orgc0f7fec"></a>

## Generators


<a id="orge4861a0"></a>

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


<a id="org9bd7186"></a>

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


<a id="orgdba888f"></a>

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


<a id="orgba435b3"></a>

### Value

1.  value-2d

    1.  Parameter List

    2.  Description

    3.  Example

2.  value-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="orgdff5ced"></a>

### Cellular

1.  cellular-2d

    1.  Parameter List

    2.  Description

    3.  Example

2.  cellular-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org6730c2c"></a>

### Cylinders

1.  cylinders-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org00aa0df"></a>

### Spheres

1.  spheres-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org0ea5031"></a>

### Checker

1.  checker-2d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="orgb067255"></a>

### Constant

1.  constant

    1.  Parameter List

    2.  Description

    3.  Example


<a id="orgfea4358"></a>

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


<a id="org0795970"></a>

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


<a id="orgb5a5c3d"></a>

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


<a id="org95c9a45"></a>

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


<a id="orga139655"></a>

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


<a id="orgefaa847"></a>

## Modifiers


<a id="org3a7cb87"></a>

### +

1.  Parameter List

2.  Description

3.  Example


<a id="org1a0581f"></a>

### -

1.  Parameter List

2.  Description

3.  Example


<a id="org62b8b86"></a>

### \*

1.  Parameter List

2.  Description

3.  Example


<a id="org6c0c552"></a>

### /

1.  Parameter List

2.  Description

3.  Example


<a id="orgc3bcd1c"></a>

### abs

1.  Parameter List

2.  Description

3.  Example


<a id="org7d53eee"></a>

### blend

1.  Parameter List

2.  Description

3.  Example


<a id="org56ca270"></a>

### cache

1.  Parameter List

2.  Description

3.  Example


<a id="org68dab80"></a>

### clamp

1.  Parameter List

2.  Description

3.  Example


<a id="org97d3cd7"></a>

### curve

1.  Parameter List

2.  Description

3.  Example


<a id="orgdb33892"></a>

### displace

1.  Parameter List

2.  Description

3.  Example


<a id="org40a468a"></a>

### expt

1.  Parameter List

2.  Description

3.  Example


<a id="org8653483"></a>

### fractalize

1.  Parameter List

2.  Description

3.  Example


<a id="orgedb3d2f"></a>

### max

1.  Parameter List

2.  Description

3.  Example


<a id="org2fdc2db"></a>

### negate

1.  Parameter List

2.  Description

3.  Example


<a id="orgc5551d6"></a>

### power

1.  Parameter List

2.  Description

3.  Example


<a id="org8977706"></a>

### rotate

1.  Parameter List

2.  Description

3.  Example


<a id="org00e3251"></a>

### scale

1.  Parameter List

2.  Description

3.  Example


<a id="org47b30c2"></a>

### select

1.  Parameter List

2.  Description

3.  Example


<a id="orgecd3bd6"></a>

### strengthen

1.  Parameter List

2.  Description

3.  Example


<a id="org559d0e9"></a>

### terrace

1.  Parameter List

2.  Description

3.  Example


<a id="orgf045b0f"></a>

### translate

1.  Parameter List

2.  Description

3.  Example


<a id="orgcc8ef4f"></a>

### turbulance

1.  Parameter List

2.  Description

3.  Example


<a id="orgaf6add7"></a>

### uniform-scale

1.  Parameter List

2.  Description

3.  Example


<a id="org7062baf"></a>

## Map


<a id="org1c442a8"></a>

### define-gradient


<a id="org7eb1770"></a>

### get-image-pixel


<a id="orgcf4a6d8"></a>

### image

1.  image-height

2.  image-width

3.  image-data


<a id="orgef386a9"></a>

### make-map

1.  map-data

2.  map-height

3.  map-value

4.  map-width


<a id="orgb7db437"></a>

### render-map


<a id="orgcea8b6f"></a>

### write-image


<a id="orgc6f4d58"></a>

# Glossary


<a id="org1284e81"></a>

# References


<a id="org7f21719"></a>

# Prototyping

Remove this entire section when the org more docs are complete.


<a id="orgc54c8d6"></a>

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


<a id="org49ddc2e"></a>

## Org Mode Wisdom


<a id="org439f748"></a>

### <https://www.gnu.org/software/emacs/refcards/pdf/orgcard.pdf>


<a id="orgb35d1ec"></a>

### <https://orgmode.org/worg/orgcard.html>


<a id="org6d0f571"></a>

### <https://orgmode.org/manual/Variable-Index.html>


<a id="orge757164"></a>

### C-c C-x C-v - org-toggle-inline-images

Used to toggle all inline images on and off.


<a id="org7536cc8"></a>

### C-c C-v b - org-babel-execute-buffer.

Execute all code blocks in the buffer and update the results. Must usually


<a id="org65786ab"></a>

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