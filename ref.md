- [Cricket Introduction](#orgc6bdf75)
- [Coherent Noise](#org5eaa574)
- [API](#orgee59134)
  - [Generators](#orgd73617a)
    - [Perlin](#org394f57e)
    - [Simplex](#org57d7f5a)
    - [Open-Simplex](#orgbb04eeb)
    - [Value](#orgb368bec)
    - [Cellular](#org3b7fe04)
    - [Cylinders](#orgcbd4e23)
    - [Spheres](#orga14e8e4)
    - [Checker](#org83b3dfd)
    - [Constant](#org4df401b)
    - [FBM: Fractal Brownian Motion](#orgf785833)
    - [Billow](#org8cbe3fe)
    - [Multifractal](#org31dcecf)
    - [Hybrid-Multifractal](#org5174c37)
    - [Ridged-Multifractal](#org3174a80)
  - [Modifiers](#orgd39509b)
    - [+](#org3075bea)
    - [-](#org94e81ca)
    - [\*](#orgfd7fcad)
    - [/](#orga55915f)
    - [abs](#org81f28f6)
    - [blend](#orgfb0fc8f)
    - [cache](#orgee0aab3)
    - [clamp](#org19cf916)
    - [curve](#orgc33d055)
    - [displace](#org48647d9)
    - [expt](#org4a94769)
    - [fractalize](#orgfe17f3e)
    - [max](#org5b92215)
    - [negate](#org43a4e0b)
    - [power](#org1a4383a)
    - [rotate](#org89ad9ca)
    - [scale](#org023a7bb)
    - [select](#org827f1f5)
    - [strengthen](#org5e2850a)
    - [terrace](#org248419b)
    - [translate](#org73cb96c)
    - [turbulance](#org16711d0)
    - [uniform-scale](#org6ba2501)
  - [Map](#orgd265e9d)
    - [define-gradient](#org69366c2)
    - [get-image-pixel](#org0b52d5d)
    - [image](#orgdb224a1)
    - [make-map](#org9dd7137)
    - [render-map](#orgf603aa9)
    - [write-image](#org257631d)
- [Glossary](#orga7d1238)
- [References](#org2b1cfc4)
- [Prototyping](#org81e00fe)
  - [Org Mode Code Block Examples](#org8e2c140)
  - [Org Mode Wisdom](#org60aa5fc)
    - [<https://www.gnu.org/software/emacs/refcards/pdf/orgcard.pdf>](#orgb33015a)
    - [<https://orgmode.org/worg/orgcard.html>](#org371513e)
    - [<https://orgmode.org/manual/Variable-Index.html>](#org15a5b98)
    - [C-c C-x C-v - org-toggle-inline-images](#orgad49ea5)
    - [C-c C-v b - org-babel-execute-buffer.](#org7d46bc4)
- [Org Mode Utilities](#org14b3920)


<a id="orgc6bdf75"></a>

# Cricket Introduction


<a id="org5eaa574"></a>

# Coherent Noise


<a id="orgee59134"></a>

# API


<a id="orgd73617a"></a>

## Generators


<a id="org394f57e"></a>

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


<a id="org57d7f5a"></a>

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


<a id="orgbb04eeb"></a>

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


<a id="orgb368bec"></a>

### Value

1.  value-2d

    1.  Parameter List

    2.  Description

    3.  Example

2.  value-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org3b7fe04"></a>

### Cellular

1.  cellular-2d

    1.  Parameter List

    2.  Description

    3.  Example

2.  cellular-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="orgcbd4e23"></a>

### Cylinders

1.  cylinders-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="orga14e8e4"></a>

### Spheres

1.  spheres-3d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org83b3dfd"></a>

### Checker

1.  checker-2d

    1.  Parameter List

    2.  Description

    3.  Example


<a id="org4df401b"></a>

### Constant

1.  constant

    1.  Parameter List

    2.  Description

    3.  Example


<a id="orgf785833"></a>

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


<a id="org8cbe3fe"></a>

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


<a id="org31dcecf"></a>

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


<a id="org5174c37"></a>

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


<a id="org3174a80"></a>

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


<a id="orgd39509b"></a>

## Modifiers


<a id="org3075bea"></a>

### +

1.  Parameter List

2.  Description

3.  Example


<a id="org94e81ca"></a>

### -

1.  Parameter List

2.  Description

3.  Example


<a id="orgfd7fcad"></a>

### \*

1.  Parameter List

2.  Description

3.  Example


<a id="orga55915f"></a>

### /

1.  Parameter List

2.  Description

3.  Example


<a id="org81f28f6"></a>

### abs

1.  Parameter List

2.  Description

3.  Example


<a id="orgfb0fc8f"></a>

### blend

1.  Parameter List

2.  Description

3.  Example


<a id="orgee0aab3"></a>

### cache

1.  Parameter List

2.  Description

3.  Example


<a id="org19cf916"></a>

### clamp

1.  Parameter List

2.  Description

3.  Example


<a id="orgc33d055"></a>

### curve

1.  Parameter List

2.  Description

3.  Example


<a id="org48647d9"></a>

### displace

1.  Parameter List

2.  Description

3.  Example


<a id="org4a94769"></a>

### expt

1.  Parameter List

2.  Description

3.  Example


<a id="orgfe17f3e"></a>

### fractalize

1.  Parameter List

2.  Description

3.  Example


<a id="org5b92215"></a>

### max

1.  Parameter List

2.  Description

3.  Example


<a id="org43a4e0b"></a>

### negate

1.  Parameter List

2.  Description

3.  Example


<a id="org1a4383a"></a>

### power

1.  Parameter List

2.  Description

3.  Example


<a id="org89ad9ca"></a>

### rotate

1.  Parameter List

2.  Description

3.  Example


<a id="org023a7bb"></a>

### scale

1.  Parameter List

2.  Description

3.  Example


<a id="org827f1f5"></a>

### select

1.  Parameter List

2.  Description

3.  Example


<a id="org5e2850a"></a>

### strengthen

1.  Parameter List

2.  Description

3.  Example


<a id="org248419b"></a>

### terrace

1.  Parameter List

2.  Description

3.  Example


<a id="org73cb96c"></a>

### translate

1.  Parameter List

2.  Description

3.  Example


<a id="org16711d0"></a>

### turbulance

1.  Parameter List

2.  Description

3.  Example


<a id="org6ba2501"></a>

### uniform-scale

1.  Parameter List

2.  Description

3.  Example


<a id="orgd265e9d"></a>

## Map


<a id="org69366c2"></a>

### define-gradient


<a id="org0b52d5d"></a>

### get-image-pixel


<a id="orgdb224a1"></a>

### image

1.  image-height

2.  image-width

3.  image-data


<a id="org9dd7137"></a>

### make-map

1.  map-data

2.  map-height

3.  map-value

4.  map-width


<a id="orgf603aa9"></a>

### render-map


<a id="org257631d"></a>

### write-image


<a id="orga7d1238"></a>

# Glossary


<a id="org2b1cfc4"></a>

# References


<a id="org81e00fe"></a>

# Prototyping

Remove this entire section when the org more docs are complete.


<a id="org8e2c140"></a>

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


<a id="org60aa5fc"></a>

## Org Mode Wisdom


<a id="orgb33015a"></a>

### <https://www.gnu.org/software/emacs/refcards/pdf/orgcard.pdf>


<a id="org371513e"></a>

### <https://orgmode.org/worg/orgcard.html>


<a id="org15a5b98"></a>

### <https://orgmode.org/manual/Variable-Index.html>


<a id="orgad49ea5"></a>

### C-c C-x C-v - org-toggle-inline-images

Used to toggle all inline images on and off.


<a id="org7d46bc4"></a>

### C-c C-v b - org-babel-execute-buffer.

Execute all code blocks in the buffer and update the results. Must usually


<a id="org14b3920"></a>

# Org Mode Utilities

The following utility is a post processor to convert the absolute pathname of C:WRITE-IMAGE which has been flatted into a string by org mode&#x2013;with the #P and double quotes included(!), into a string of just the relative filename given the cwd of theemacs process. This is a pure hack that suffices for this one use case so I can develop these docs with a fast workflow.