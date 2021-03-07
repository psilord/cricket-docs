
# Table of Contents

1.  [Cricket Introduction](#org488271a)
2.  [Coherent Noise](#org38292db)
3.  [API](#orgc3c320d)
    1.  [Generators](#orgda91a3c)
        1.  [Perlin](#org2988bc0)
        2.  [Simplex](#org4e2fac9)
        3.  [Open-Simplex](#orgc3f628a)
        4.  [Value](#org43ffa2c)
        5.  [Cellular](#org0b47e34)
        6.  [Cylinders](#orgad5b7fe)
        7.  [Spheres](#orgcf50907)
        8.  [Checker](#orgc7230ac)
        9.  [Constant](#orge992a1c)
        10. [FBM: Fractal Brownian Motion](#org793084e)
        11. [Billow](#orgc855c80)
        12. [Multifractal](#org8996717)
        13. [Hybrid-Multifractal](#org62ca71f)
        14. [Ridged-Multifractal](#orgfe20775)
    2.  [Modifiers](#org29412b2)
        1.  [+](#org2229410)
        2.  [-](#orgde4a732)
        3.  [\*](#org5db7d9c)
        4.  [/](#orgbc639ed)
        5.  [abs](#org6385c8b)
        6.  [blend](#org9f85135)
        7.  [cache](#org2082db0)
        8.  [clamp](#org21c1799)
        9.  [curve](#orgfca2e4f)
        10. [displace](#orge0c7d03)
        11. [expt](#org6a3c82a)
        12. [fractalize](#org2d85897)
        13. [max](#orgac9b5e9)
        14. [negate](#org5ab8e93)
        15. [power](#org3bf1a80)
        16. [rotate](#org68a0219)
        17. [scale](#orga572f19)
        18. [select](#org0c5a86e)
        19. [strengthen](#orgc3c2374)
        20. [terrace](#orgf8eb825)
        21. [translate](#org1b248ec)
        22. [turbulance](#orgfe04a9e)
        23. [uniform-scale](#orgec1135d)
    3.  [Map](#orgd24564c)
        1.  [define-gradient](#org8214fe0)
        2.  [get-image-pixel](#org46cc10f)
        3.  [image](#org20b3435)
        4.  [make-map](#orgd325e84)
        5.  [render-map](#org5f0931d)
        6.  [write-image](#org3bac850)
4.  [Glossary](#org3e9ab36)
5.  [References](#orgd10c5fe)
6.  [Prototyping](#orgace3b7e)
    1.  [Org Mode Code Block Examples](#orgd210985)
    2.  [Org Mode Wisdom](#org5dbd542)
        1.  [https://www.gnu.org/software/emacs/refcards/pdf/orgcard.pdf](#orgba9a884)
        2.  [https://orgmode.org/worg/orgcard.html](#org08c0e81)
        3.  [https://orgmode.org/manual/Variable-Index.html](#orgefd72a5)
        4.  [C-c C-x C-v - org-toggle-inline-images](#org5b6263f)
        5.  [C-c C-v b - org-babel-execute-buffer.](#orgcc046d6)
7.  [Org Mode Utilities](#org6d38770)


<a id="org488271a"></a>

# Cricket Introduction


<a id="org38292db"></a>

# Coherent Noise


<a id="orgc3c320d"></a>

# API


<a id="orgda91a3c"></a>

## Generators


<a id="org2988bc0"></a>

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


<a id="org4e2fac9"></a>

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


<a id="orgc3f628a"></a>

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


<a id="org43ffa2c"></a>

### Value

1.  value-2d

    1.  Parameter List

    2.  Description

    3.  Example

2.  value-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org0b47e34"></a>

### Cellular

1.  cellular-2d

    1.  Parameter List

    2.  Description

    3.  Example

2.  cellular-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="orgad5b7fe"></a>

### Cylinders

1.  cylinders-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="orgcf50907"></a>

### Spheres

1.  spheres-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="orgc7230ac"></a>

### Checker

1.  checker-2d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="orge992a1c"></a>

### Constant

1.  constant

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org793084e"></a>

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


<a id="orgc855c80"></a>

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


<a id="org8996717"></a>

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


<a id="org62ca71f"></a>

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


<a id="orgfe20775"></a>

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


<a id="org29412b2"></a>

## Modifiers


<a id="org2229410"></a>

### +

1.  Parameter List

2.  Description

3.  Example


<a id="orgde4a732"></a>

### -

1.  Parameter List

2.  Description

3.  Example


<a id="org5db7d9c"></a>

### \*

1.  Parameter List

2.  Description

3.  Example


<a id="orgbc639ed"></a>

### /

1.  Parameter List

2.  Description

3.  Example


<a id="org6385c8b"></a>

### abs

1.  Parameter List

2.  Description

3.  Example


<a id="org9f85135"></a>

### blend

1.  Parameter List

2.  Description

3.  Example


<a id="org2082db0"></a>

### cache

1.  Parameter List

2.  Description

3.  Example


<a id="org21c1799"></a>

### clamp

1.  Parameter List

2.  Description

3.  Example


<a id="orgfca2e4f"></a>

### curve

1.  Parameter List

2.  Description

3.  Example


<a id="orge0c7d03"></a>

### displace

1.  Parameter List

2.  Description

3.  Example


<a id="org6a3c82a"></a>

### expt

1.  Parameter List

2.  Description

3.  Example


<a id="org2d85897"></a>

### fractalize

1.  Parameter List

2.  Description

3.  Example


<a id="orgac9b5e9"></a>

### max

1.  Parameter List

2.  Description

3.  Example


<a id="org5ab8e93"></a>

### negate

1.  Parameter List

2.  Description

3.  Example


<a id="org3bf1a80"></a>

### power

1.  Parameter List

2.  Description

3.  Example


<a id="org68a0219"></a>

### rotate

1.  Parameter List

2.  Description

3.  Example


<a id="orga572f19"></a>

### scale

1.  Parameter List

2.  Description

3.  Example


<a id="org0c5a86e"></a>

### select

1.  Parameter List

2.  Description

3.  Example


<a id="orgc3c2374"></a>

### strengthen

1.  Parameter List

2.  Description

3.  Example


<a id="orgf8eb825"></a>

### terrace

1.  Parameter List

2.  Description

3.  Example


<a id="org1b248ec"></a>

### translate

1.  Parameter List

2.  Description

3.  Example


<a id="orgfe04a9e"></a>

### turbulance

1.  Parameter List

2.  Description

3.  Example


<a id="orgec1135d"></a>

### uniform-scale

1.  Parameter List

2.  Description

3.  Example


<a id="orgd24564c"></a>

## Map


<a id="org8214fe0"></a>

### define-gradient


<a id="org46cc10f"></a>

### get-image-pixel


<a id="org20b3435"></a>

### image

1.  image-height

2.  image-width

3.  image-data


<a id="orgd325e84"></a>

### make-map

1.  map-data

2.  map-height

3.  map-value

4.  map-width


<a id="org5f0931d"></a>

### render-map


<a id="org3bac850"></a>

### write-image


<a id="org3e9ab36"></a>

# Glossary


<a id="orgd10c5fe"></a>

# References


<a id="orgace3b7e"></a>

# Prototyping

Remove this entire section when the org more docs are complete.


<a id="orgd210985"></a>

## Org Mode Code Block Examples

This is an example of how to configure org-mode so that when I execute
a block of common lisp the image it generates is places realtime inlined
into the org document as appropriate.

    echo "Hello world"

    (ql:quickload :cricket)
    (defpackage #:my-package
      (:local-nicknames (#:c #:cricket))
      (:use #:cl))
    (in-package #:my-package) ;; <- doesn't affect repl!

    (c:-> (c:checker-2d :seed "example")
      ;;(c:uniform-scale 1/4)
      (c:fractalize :fbm :octaves 3)
      (c:make-map :width 256 :height 256)
      (c:render-map)
      (c:write-image arg))

![img](/home/psilord/quicklisp/local-projects/cricket-docs/img/proto/proto-0.png)

Example text.

    (c:-> (c:perlin-3d :seed "example")
      (c:uniform-scale 1.5)
      (c:fractalize :fbm :frequency 1.3 :octaves 6 :lacunarity 3 :persistence 0.22)
      (c:turbulence (c:open-simplex-3d :seed "foo") :power 1.2 :roughness 4)
      (c:make-map :width 256 :height 256)
      (c:render-map :gradient :terrain)
      (c:write-image arg))

![img](/home/psilord/quicklisp/local-projects/cricket-docs/img/proto/proto-1.png)

Documentation retrival test:

The documentation string for PERLIN-2D is:

    Construct a sampler that, when sampled, outputs 2-dimensional Perlin Improved noise values
    ranging from -1.0 to 1.0.

    `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
    supplied, one will be generated automatically which will negatively affect the reproducibility of
    the noise (optional, default: NIL).


<a id="org5dbd542"></a>

## Org Mode Wisdom


<a id="orgba9a884"></a>

### <https://www.gnu.org/software/emacs/refcards/pdf/orgcard.pdf>


<a id="org08c0e81"></a>

### <https://orgmode.org/worg/orgcard.html>


<a id="orgefd72a5"></a>

### <https://orgmode.org/manual/Variable-Index.html>


<a id="org5b6263f"></a>

### C-c C-x C-v - org-toggle-inline-images

Used to toggle all inline images on and off.


<a id="orgcc046d6"></a>

### C-c C-v b - org-babel-execute-buffer.

Execute all code blocks in the buffer and update the results.
Must usually


<a id="org6d38770"></a>

# Org Mode Utilities

The following utility is a post processor to convert the pathname output of
C:WRITE-IMAGE which has then been flatted into a string by org mode&#x2013;with
the #P included, into a string of just the filename. This is a pure
hack that suffices for this one use case. To support C-c C-v b for
recomputing all images, we check path to ensure it is valid.

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
