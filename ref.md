- [Cricket Introduction](#org49cc342)
- [Coherent Noise](#org90c81de)
- [API](#org2b201f5)
  - [Generators](#org080a82d)
    - [Perlin](#org572a6d7)
    - [Simplex](#org7b05ee9)
    - [Open-Simplex](#orgc5e17b8)
    - [Value](#org33cca94)
    - [Cellular](#org816eee3)
    - [Cylinders](#org92d4391)
    - [Spheres](#org41846c1)
    - [Checker](#org813b8b5)
    - [Constant](#orgd10cc3e)
    - [FBM: Fractal Brownian Motion](#orgef49749)
    - [Billow](#org3b27533)
    - [Multifractal](#orgf18d531)
    - [Hybrid-Multifractal](#org9a636a5)
    - [Ridged-Multifractal](#org39321c9)
  - [Modifiers](#org118a76c)
    - [+](#orgab53889)
    - [-](#org55b2c71)
    - [\*](#org395b304)
    - [/](#org37fa05f)
    - [abs](#orgf717954)
    - [blend](#org779c5a2)
    - [cache](#org0baa008)
    - [clamp](#orge4556f7)
    - [curve](#org9d65cd4)
    - [displace](#orgac0fcaf)
    - [expt](#org9c2bbdd)
    - [fractalize](#orgbd1d2b3)
    - [max](#orgf69396c)
    - [negate](#orgc4e747e)
    - [power](#orgd117618)
    - [rotate](#org5b59a78)
    - [scale](#org6e5e233)
    - [select](#orgfa9757e)
    - [strengthen](#org95dd552)
    - [terrace](#org3cd81bb)
    - [translate](#orga3b0fcf)
    - [turbulance](#orge861c44)
    - [uniform-scale](#org4f24fec)
  - [Map](#org2ab2925)
    - [define-gradient](#org41cdd35)
    - [get-image-pixel](#org9bdbccd)
    - [image](#org4eb46dc)
    - [make-map](#org69f6b4c)
    - [render-map](#org22b4d8f)
    - [write-image](#org9a60dfd)
- [Glossary](#org73ad775)
- [References](#org54a71c2)
- [Prototyping](#org040e59a)
  - [Org Mode Code Block Examples](#org669581a)
  - [Org Mode Wisdom](#orgb0b5a76)
    - [<https://www.gnu.org/software/emacs/refcards/pdf/orgcard.pdf>](#orga7d0a66)
    - [<https://orgmode.org/worg/orgcard.html>](#org5dab10d)
    - [<https://orgmode.org/manual/Variable-Index.html>](#org24d2cf0)
    - [C-c C-x C-v - org-toggle-inline-images](#org1e65805)
    - [C-c C-v b - org-babel-execute-buffer.](#orgdfc3c01)
- [Org Mode Utilities](#org55a431c)


<a id="org49cc342"></a>

# Cricket Introduction


<a id="org90c81de"></a>

# Coherent Noise


<a id="org2b201f5"></a>

# API


<a id="org080a82d"></a>

## Generators


<a id="org572a6d7"></a>

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


<a id="org7b05ee9"></a>

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


<a id="orgc5e17b8"></a>

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


<a id="org33cca94"></a>

### Value

1.  value-2d

    1.  Parameter List

    2.  Description

    3.  Example

2.  value-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org816eee3"></a>

### Cellular

1.  cellular-2d

    1.  Parameter List

    2.  Description

    3.  Example

2.  cellular-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org92d4391"></a>

### Cylinders

1.  cylinders-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org41846c1"></a>

### Spheres

1.  spheres-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org813b8b5"></a>

### Checker

1.  checker-2d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="orgd10cc3e"></a>

### Constant

1.  constant

    1.  Parameter List

    2.  Description

    3.  Example


<a id="orgef49749"></a>

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


<a id="org3b27533"></a>

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


<a id="orgf18d531"></a>

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


<a id="org9a636a5"></a>

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


<a id="org39321c9"></a>

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


<a id="org118a76c"></a>

## Modifiers


<a id="orgab53889"></a>

### +

1.  Parameter List

2.  Description

3.  Example


<a id="org55b2c71"></a>

### -

1.  Parameter List

2.  Description

3.  Example


<a id="org395b304"></a>

### \*

1.  Parameter List

2.  Description

3.  Example


<a id="org37fa05f"></a>

### /

1.  Parameter List

2.  Description

3.  Example


<a id="orgf717954"></a>

### abs

1.  Parameter List

2.  Description

3.  Example


<a id="org779c5a2"></a>

### blend

1.  Parameter List

2.  Description

3.  Example


<a id="org0baa008"></a>

### cache

1.  Parameter List

2.  Description

3.  Example


<a id="orge4556f7"></a>

### clamp

1.  Parameter List

2.  Description

3.  Example


<a id="org9d65cd4"></a>

### curve

1.  Parameter List

2.  Description

3.  Example


<a id="orgac0fcaf"></a>

### displace

1.  Parameter List

2.  Description

3.  Example


<a id="org9c2bbdd"></a>

### expt

1.  Parameter List

2.  Description

3.  Example


<a id="orgbd1d2b3"></a>

### fractalize

1.  Parameter List

2.  Description

3.  Example


<a id="orgf69396c"></a>

### max

1.  Parameter List

2.  Description

3.  Example


<a id="orgc4e747e"></a>

### negate

1.  Parameter List

2.  Description

3.  Example


<a id="orgd117618"></a>

### power

1.  Parameter List

2.  Description

3.  Example


<a id="org5b59a78"></a>

### rotate

1.  Parameter List

2.  Description

3.  Example


<a id="org6e5e233"></a>

### scale

1.  Parameter List

2.  Description

3.  Example


<a id="orgfa9757e"></a>

### select

1.  Parameter List

2.  Description

3.  Example


<a id="org95dd552"></a>

### strengthen

1.  Parameter List

2.  Description

3.  Example


<a id="org3cd81bb"></a>

### terrace

1.  Parameter List

2.  Description

3.  Example


<a id="orga3b0fcf"></a>

### translate

1.  Parameter List

2.  Description

3.  Example


<a id="orge861c44"></a>

### turbulance

1.  Parameter List

2.  Description

3.  Example


<a id="org4f24fec"></a>

### uniform-scale

1.  Parameter List

2.  Description

3.  Example


<a id="org2ab2925"></a>

## Map


<a id="org41cdd35"></a>

### define-gradient


<a id="org9bdbccd"></a>

### get-image-pixel


<a id="org4eb46dc"></a>

### image

1.  image-height

2.  image-width

3.  image-data


<a id="org69f6b4c"></a>

### make-map

1.  map-data

2.  map-height

3.  map-value

4.  map-width


<a id="org22b4d8f"></a>

### render-map


<a id="org9a60dfd"></a>

### write-image


<a id="org73ad775"></a>

# Glossary


<a id="org54a71c2"></a>

# References


<a id="org040e59a"></a>

# Prototyping

Remove this entire section when the org more docs are complete.


<a id="org669581a"></a>

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


<a id="orgb0b5a76"></a>

## Org Mode Wisdom


<a id="orga7d0a66"></a>

### <https://www.gnu.org/software/emacs/refcards/pdf/orgcard.pdf>


<a id="org5dab10d"></a>

### <https://orgmode.org/worg/orgcard.html>


<a id="org24d2cf0"></a>

### <https://orgmode.org/manual/Variable-Index.html>


<a id="org1e65805"></a>

### C-c C-x C-v - org-toggle-inline-images

Used to toggle all inline images on and off.


<a id="orgdfc3c01"></a>

### C-c C-v b - org-babel-execute-buffer.

Execute all code blocks in the buffer and update the results. Must usually


<a id="org55a431c"></a>

# Org Mode Utilities

The following utility is a post processor to convert the pathname output of C:WRITE-IMAGE which has then been flatted into a string by org mode&#x2013;with the #P included, into a string of just the filename. This is a pure hack that suffices for this one use case. To support C-c C-v b for recomputing all images, we check path to ensure it is valid.