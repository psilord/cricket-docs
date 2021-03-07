- [Cricket Introduction](#orgaebf8d6)
- [Coherent Noise](#orge6f8336)
- [API](#orgadd95f2)
  - [Generators](#orga07c46a)
    - [Perlin](#org0573c78)
    - [Simplex](#org956a1ff)
    - [Open-Simplex](#org6a1a48e)
    - [Value](#orgcb9f948)
    - [Cellular](#org42ae026)
    - [Cylinders](#orgac1a419)
    - [Spheres](#org98bb044)
    - [Checker](#org10d3645)
    - [Constant](#org7fc9a72)
    - [FBM: Fractal Brownian Motion](#orgb8ce93f)
    - [Billow](#org8fee7eb)
    - [Multifractal](#orgea581a6)
    - [Hybrid-Multifractal](#org0302246)
    - [Ridged-Multifractal](#org2851384)
  - [Modifiers](#orga30769f)
    - [+](#org3a9e387)
    - [-](#org46812df)
    - [\*](#org9446b62)
    - [/](#orgb606a6b)
    - [abs](#org872f7b1)
    - [blend](#orgb109b29)
    - [cache](#org7f630de)
    - [clamp](#org8d19b7c)
    - [curve](#org43a1e96)
    - [displace](#org6573b45)
    - [expt](#org24f4311)
    - [fractalize](#org832c5dd)
    - [max](#orge4f0b64)
    - [negate](#org0b2b6fd)
    - [power](#org2bb4785)
    - [rotate](#org513a096)
    - [scale](#orgdba7b06)
    - [select](#org275e6e6)
    - [strengthen](#orgf6579e8)
    - [terrace](#orgbb83386)
    - [translate](#org1493b71)
    - [turbulance](#org54a23f0)
    - [uniform-scale](#org222132f)
  - [Map](#org8f7341c)
    - [define-gradient](#orgc585f8a)
    - [get-image-pixel](#org48a31b8)
    - [image](#org661e767)
    - [make-map](#org6306b48)
    - [render-map](#orgc159ab9)
    - [write-image](#org73bdb60)
- [Glossary](#orgbfa7cb9)
- [References](#orgbf5411e)
- [Prototyping](#orgfdd6c6a)
  - [Org Mode Code Block Examples](#org055dd25)
  - [Org Mode Wisdom](#org667a45e)
    - [<https://www.gnu.org/software/emacs/refcards/pdf/orgcard.pdf>](#org7127fa9)
    - [<https://orgmode.org/worg/orgcard.html>](#orgff3ed3e)
    - [<https://orgmode.org/manual/Variable-Index.html>](#org4b46685)
    - [C-c C-x C-v - org-toggle-inline-images](#org9294bc3)
    - [C-c C-v b - org-babel-execute-buffer.](#org25cb8f4)
- [Org Mode Utilities](#org1017b88)


<a id="orgaebf8d6"></a>

# Cricket Introduction


<a id="orge6f8336"></a>

# Coherent Noise


<a id="orgadd95f2"></a>

# API


<a id="orga07c46a"></a>

## Generators


<a id="org0573c78"></a>

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


<a id="org956a1ff"></a>

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


<a id="org6a1a48e"></a>

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


<a id="orgcb9f948"></a>

### Value

1.  value-2d

    1.  Parameter List

    2.  Description

    3.  Example

2.  value-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org42ae026"></a>

### Cellular

1.  cellular-2d

    1.  Parameter List

    2.  Description

    3.  Example

2.  cellular-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="orgac1a419"></a>

### Cylinders

1.  cylinders-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org98bb044"></a>

### Spheres

1.  spheres-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org10d3645"></a>

### Checker

1.  checker-2d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org7fc9a72"></a>

### Constant

1.  constant

    1.  Parameter List

    2.  Description

    3.  Example


<a id="orgb8ce93f"></a>

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


<a id="org8fee7eb"></a>

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


<a id="orgea581a6"></a>

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


<a id="org0302246"></a>

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


<a id="org2851384"></a>

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


<a id="orga30769f"></a>

## Modifiers


<a id="org3a9e387"></a>

### +

1.  Parameter List

2.  Description

3.  Example


<a id="org46812df"></a>

### -

1.  Parameter List

2.  Description

3.  Example


<a id="org9446b62"></a>

### \*

1.  Parameter List

2.  Description

3.  Example


<a id="orgb606a6b"></a>

### /

1.  Parameter List

2.  Description

3.  Example


<a id="org872f7b1"></a>

### abs

1.  Parameter List

2.  Description

3.  Example


<a id="orgb109b29"></a>

### blend

1.  Parameter List

2.  Description

3.  Example


<a id="org7f630de"></a>

### cache

1.  Parameter List

2.  Description

3.  Example


<a id="org8d19b7c"></a>

### clamp

1.  Parameter List

2.  Description

3.  Example


<a id="org43a1e96"></a>

### curve

1.  Parameter List

2.  Description

3.  Example


<a id="org6573b45"></a>

### displace

1.  Parameter List

2.  Description

3.  Example


<a id="org24f4311"></a>

### expt

1.  Parameter List

2.  Description

3.  Example


<a id="org832c5dd"></a>

### fractalize

1.  Parameter List

2.  Description

3.  Example


<a id="orge4f0b64"></a>

### max

1.  Parameter List

2.  Description

3.  Example


<a id="org0b2b6fd"></a>

### negate

1.  Parameter List

2.  Description

3.  Example


<a id="org2bb4785"></a>

### power

1.  Parameter List

2.  Description

3.  Example


<a id="org513a096"></a>

### rotate

1.  Parameter List

2.  Description

3.  Example


<a id="orgdba7b06"></a>

### scale

1.  Parameter List

2.  Description

3.  Example


<a id="org275e6e6"></a>

### select

1.  Parameter List

2.  Description

3.  Example


<a id="orgf6579e8"></a>

### strengthen

1.  Parameter List

2.  Description

3.  Example


<a id="orgbb83386"></a>

### terrace

1.  Parameter List

2.  Description

3.  Example


<a id="org1493b71"></a>

### translate

1.  Parameter List

2.  Description

3.  Example


<a id="org54a23f0"></a>

### turbulance

1.  Parameter List

2.  Description

3.  Example


<a id="org222132f"></a>

### uniform-scale

1.  Parameter List

2.  Description

3.  Example


<a id="org8f7341c"></a>

## Map


<a id="orgc585f8a"></a>

### define-gradient


<a id="org48a31b8"></a>

### get-image-pixel


<a id="org661e767"></a>

### image

1.  image-height

2.  image-width

3.  image-data


<a id="org6306b48"></a>

### make-map

1.  map-data

2.  map-height

3.  map-value

4.  map-width


<a id="orgc159ab9"></a>

### render-map


<a id="org73bdb60"></a>

### write-image


<a id="orgbfa7cb9"></a>

# Glossary


<a id="orgbf5411e"></a>

# References


<a id="orgfdd6c6a"></a>

# Prototyping

Remove this entire section when the org more docs are complete.


<a id="org055dd25"></a>

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

![img](./img/proto/proto-0.png)

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

![img](./img/proto/proto-1.png)

Documentation retrival test:

The documentation string for PERLIN-2D is:

    Construct a sampler that, when sampled, outputs 2-dimensional Perlin Improved noise values
    ranging from -1.0 to 1.0.

    `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
    supplied, one will be generated automatically which will negatively affect the reproducibility of
    the noise (optional, default: NIL).


<a id="org667a45e"></a>

## Org Mode Wisdom


<a id="org7127fa9"></a>

### <https://www.gnu.org/software/emacs/refcards/pdf/orgcard.pdf>


<a id="orgff3ed3e"></a>

### <https://orgmode.org/worg/orgcard.html>


<a id="org4b46685"></a>

### <https://orgmode.org/manual/Variable-Index.html>


<a id="org9294bc3"></a>

### C-c C-x C-v - org-toggle-inline-images

Used to toggle all inline images on and off.


<a id="org25cb8f4"></a>

### C-c C-v b - org-babel-execute-buffer.

Execute all code blocks in the buffer and update the results. Must usually


<a id="org1017b88"></a>

# Org Mode Utilities

The following utility is a post processor to convert the absolute pathname of C:WRITE-IMAGE which has been flatted into a string by org mode&#x2013;with the #P and double quotes included(!), into a string of just the relative filename given the cwd of theemacs process. This is a pure hack that suffices for this one use case so I can develop these docs with a fast workflow.