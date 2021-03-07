- [Cricket Introduction](#orgd7b07f9)
- [Coherent Noise](#orgd4c5b92)
- [API](#orgd9b4d60)
  - [Generators](#orgfffec48)
    - [Perlin](#orgedbf255)
    - [Simplex](#orga7fd0e4)
    - [Open-Simplex](#orgb4f905c)
    - [Value](#org8a6b376)
    - [Cellular](#org7bb725e)
    - [Cylinders](#org86b3206)
    - [Spheres](#org40e5bee)
    - [Checker](#org3408896)
    - [Constant](#org9a8cf9e)
    - [FBM: Fractal Brownian Motion](#org3caf3dd)
    - [Billow](#orgffb7256)
    - [Multifractal](#orgd82e26e)
    - [Hybrid-Multifractal](#orge5db75b)
    - [Ridged-Multifractal](#org1f5bbae)
  - [Modifiers](#org91a287e)
    - [+](#orgb2c792c)
    - [-](#orgeef0529)
    - [\*](#orgb454ec2)
    - [/](#orgd8bd30f)
    - [abs](#org1967256)
    - [blend](#org99cc429)
    - [cache](#org1936e64)
    - [clamp](#orgcc80b53)
    - [curve](#org8aac9ce)
    - [displace](#orgd34fd06)
    - [expt](#org939e67e)
    - [fractalize](#org712be18)
    - [max](#org7d56d87)
    - [negate](#orgc102639)
    - [power](#org7ab761a)
    - [rotate](#org42c7d48)
    - [scale](#org84c59ff)
    - [select](#org3b0b1f5)
    - [strengthen](#org7a3cea7)
    - [terrace](#orgbc8421e)
    - [translate](#orgf087c35)
    - [turbulance](#orgabf43cb)
    - [uniform-scale](#orgf9e8102)
  - [Map](#orgc01e49d)
    - [define-gradient](#orgc867aa1)
    - [get-image-pixel](#orgd79e73c)
    - [image](#orga4a00d5)
    - [make-map](#org97584ee)
    - [render-map](#org9b1c019)
    - [write-image](#orgc1532d6)
- [Glossary](#orgf429d15)
- [References](#org267e9f1)
- [Prototyping](#orgd461670)
  - [Org Mode Code Block Examples](#org3e70971)
  - [Org Mode Wisdom](#orgb399f88)
    - [<https://www.gnu.org/software/emacs/refcards/pdf/orgcard.pdf>](#orgbac2604)
    - [<https://orgmode.org/worg/orgcard.html>](#org55b10a2)
    - [<https://orgmode.org/manual/Variable-Index.html>](#org7c0776c)
    - [C-c C-x C-v - org-toggle-inline-images](#org732e4c9)
    - [C-c C-v b - org-babel-execute-buffer.](#org7ce34ab)
- [Org Mode Utilities](#org007483d)


<a id="orgd7b07f9"></a>

# Cricket Introduction


<a id="orgd4c5b92"></a>

# Coherent Noise


<a id="orgd9b4d60"></a>

# API


<a id="orgfffec48"></a>

## Generators


<a id="orgedbf255"></a>

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


<a id="orga7fd0e4"></a>

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


<a id="orgb4f905c"></a>

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


<a id="org8a6b376"></a>

### Value

1.  value-2d

    1.  Parameter List

    2.  Description

    3.  Example

2.  value-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org7bb725e"></a>

### Cellular

1.  cellular-2d

    1.  Parameter List

    2.  Description

    3.  Example

2.  cellular-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org86b3206"></a>

### Cylinders

1.  cylinders-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org40e5bee"></a>

### Spheres

1.  spheres-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org3408896"></a>

### Checker

1.  checker-2d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org9a8cf9e"></a>

### Constant

1.  constant

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org3caf3dd"></a>

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


<a id="orgffb7256"></a>

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


<a id="orgd82e26e"></a>

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


<a id="orge5db75b"></a>

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


<a id="org1f5bbae"></a>

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


<a id="org91a287e"></a>

## Modifiers


<a id="orgb2c792c"></a>

### +

1.  Parameter List

2.  Description

3.  Example


<a id="orgeef0529"></a>

### -

1.  Parameter List

2.  Description

3.  Example


<a id="orgb454ec2"></a>

### \*

1.  Parameter List

2.  Description

3.  Example


<a id="orgd8bd30f"></a>

### /

1.  Parameter List

2.  Description

3.  Example


<a id="org1967256"></a>

### abs

1.  Parameter List

2.  Description

3.  Example


<a id="org99cc429"></a>

### blend

1.  Parameter List

2.  Description

3.  Example


<a id="org1936e64"></a>

### cache

1.  Parameter List

2.  Description

3.  Example


<a id="orgcc80b53"></a>

### clamp

1.  Parameter List

2.  Description

3.  Example


<a id="org8aac9ce"></a>

### curve

1.  Parameter List

2.  Description

3.  Example


<a id="orgd34fd06"></a>

### displace

1.  Parameter List

2.  Description

3.  Example


<a id="org939e67e"></a>

### expt

1.  Parameter List

2.  Description

3.  Example


<a id="org712be18"></a>

### fractalize

1.  Parameter List

2.  Description

3.  Example


<a id="org7d56d87"></a>

### max

1.  Parameter List

2.  Description

3.  Example


<a id="orgc102639"></a>

### negate

1.  Parameter List

2.  Description

3.  Example


<a id="org7ab761a"></a>

### power

1.  Parameter List

2.  Description

3.  Example


<a id="org42c7d48"></a>

### rotate

1.  Parameter List

2.  Description

3.  Example


<a id="org84c59ff"></a>

### scale

1.  Parameter List

2.  Description

3.  Example


<a id="org3b0b1f5"></a>

### select

1.  Parameter List

2.  Description

3.  Example


<a id="org7a3cea7"></a>

### strengthen

1.  Parameter List

2.  Description

3.  Example


<a id="orgbc8421e"></a>

### terrace

1.  Parameter List

2.  Description

3.  Example


<a id="orgf087c35"></a>

### translate

1.  Parameter List

2.  Description

3.  Example


<a id="orgabf43cb"></a>

### turbulance

1.  Parameter List

2.  Description

3.  Example


<a id="orgf9e8102"></a>

### uniform-scale

1.  Parameter List

2.  Description

3.  Example


<a id="orgc01e49d"></a>

## Map


<a id="orgc867aa1"></a>

### define-gradient


<a id="orgd79e73c"></a>

### get-image-pixel


<a id="orga4a00d5"></a>

### image

1.  image-height

2.  image-width

3.  image-data


<a id="org97584ee"></a>

### make-map

1.  map-data

2.  map-height

3.  map-value

4.  map-width


<a id="org9b1c019"></a>

### render-map


<a id="orgc1532d6"></a>

### write-image


<a id="orgf429d15"></a>

# Glossary


<a id="org267e9f1"></a>

# References


<a id="orgd461670"></a>

# Prototyping

Remove this entire section when the org more docs are complete.


<a id="org3e70971"></a>

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


<a id="orgb399f88"></a>

## Org Mode Wisdom


<a id="orgbac2604"></a>

### <https://www.gnu.org/software/emacs/refcards/pdf/orgcard.pdf>


<a id="org55b10a2"></a>

### <https://orgmode.org/worg/orgcard.html>


<a id="org7c0776c"></a>

### <https://orgmode.org/manual/Variable-Index.html>


<a id="org732e4c9"></a>

### C-c C-x C-v - org-toggle-inline-images

Used to toggle all inline images on and off.


<a id="org7ce34ab"></a>

### C-c C-v b - org-babel-execute-buffer.

Execute all code blocks in the buffer and update the results. Must usually


<a id="org007483d"></a>

# Org Mode Utilities

The following utility is a post processor to convert the pathname output of C:WRITE-IMAGE which has then been flatted into a string by org mode&#x2013;with the #P included, into a string of just the filename. This is a pure hack that suffices for this one use case. To support C-c C-v b for recomputing all images, we check path to ensure it is valid.