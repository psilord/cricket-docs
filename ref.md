- [Cricket Introduction](#org23afd07)
- [Coherent Noise](#orgf307d8e)
- [API](#org399c985)
  - [Generators](#org888a7d0)
  - [Modifiers](#orge2761a0)
  - [Map](#org7c6bea3)
- [Glossary](#org9ee3f3f)
- [References](#orgb9b97d9)
- [Prototyping](#org9007d57)
  - [Org Mode Code Block Examples](#orga96f416)
  - [Org Mode Wisdom](#orgef33d2e)
- [Org Mode Utilities](#org29cfd6d)



<a id="org23afd07"></a>

# Cricket Introduction


<a id="orgf307d8e"></a>

# Coherent Noise


<a id="org399c985"></a>

# API


<a id="org888a7d0"></a>

## Generators


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


### Value

1.  value-2d

    1.  Parameter List

    2.  Description

    3.  Example

2.  value-3d

    1.  Parameter List

    2.  Description

    3.  Example


### Cellular

1.  cellular-2d

    1.  Parameter List

    2.  Description

    3.  Example

2.  cellular-3d

    1.  Parameter List

    2.  Description

    3.  Example


### Cylinders

1.  cylinders-3d

    1.  Parameter List

    2.  Description

    3.  Example


### Spheres

1.  spheres-3d

    1.  Parameter List

    2.  Description

    3.  Example


### Checker

1.  checker-2d

    1.  Parameter List

    2.  Description

    3.  Example


### Constant

1.  constant

    1.  Parameter List

    2.  Description

    3.  Example


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


<a id="orge2761a0"></a>

## Modifiers


### +

1.  Parameter List

2.  Description

3.  Example


### -

1.  Parameter List

2.  Description

3.  Example


### \*

1.  Parameter List

2.  Description

3.  Example


### /

1.  Parameter List

2.  Description

3.  Example


### abs

1.  Parameter List

2.  Description

3.  Example


### blend

1.  Parameter List

2.  Description

3.  Example


### cache

1.  Parameter List

2.  Description

3.  Example


### clamp

1.  Parameter List

2.  Description

3.  Example


### curve

1.  Parameter List

2.  Description

3.  Example


### displace

1.  Parameter List

2.  Description

3.  Example


### expt

1.  Parameter List

2.  Description

3.  Example


### fractalize

1.  Parameter List

2.  Description

3.  Example


### max

1.  Parameter List

2.  Description

3.  Example


### negate

1.  Parameter List

2.  Description

3.  Example


### power

1.  Parameter List

2.  Description

3.  Example


### rotate

1.  Parameter List

2.  Description

3.  Example


### scale

1.  Parameter List

2.  Description

3.  Example


### select

1.  Parameter List

2.  Description

3.  Example


### strengthen

1.  Parameter List

2.  Description

3.  Example


### terrace

1.  Parameter List

2.  Description

3.  Example


### translate

1.  Parameter List

2.  Description

3.  Example


### turbulance

1.  Parameter List

2.  Description

3.  Example


### uniform-scale

1.  Parameter List

2.  Description

3.  Example


<a id="org7c6bea3"></a>

## Map


### define-gradient


### get-image-pixel


### image

1.  image-height

2.  image-width

3.  image-data


### make-map

1.  map-data

2.  map-height

3.  map-value

4.  map-width


### render-map


### write-image


<a id="org9ee3f3f"></a>

# Glossary


<a id="orgb9b97d9"></a>

# References


<a id="org9007d57"></a>

# Prototyping

Remove this entire section when the org more docs are complete.


<a id="orga96f416"></a>

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

**(perlin-2d &key seed)**

    Construct a sampler that, when sampled, outputs 2-dimensional Perlin Improved noise values
    ranging from -1.0 to 1.0.

    `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
    supplied, one will be generated automatically which will negatively affect the reproducibility of
    the noise (optional, default: NIL).


<a id="orgef33d2e"></a>

## Org Mode Wisdom


### <https://www.gnu.org/software/emacs/refcards/pdf/orgcard.pdf>


### <https://orgmode.org/worg/orgcard.html>


### <https://orgmode.org/manual/Variable-Index.html>


### C-c C-x C-v - org-toggle-inline-images

Used to toggle all inline images on and off.


### C-c C-v b - org-babel-execute-buffer.

Execute all code blocks in the buffer and update the results. Must usually


<a id="org29cfd6d"></a>

# Org Mode Utilities

The following utility is a post processor to convert the absolute pathname of C:WRITE-IMAGE which has been flatted into a string by org mode&#x2013;with the #P and double quotes included(!), into a string of just the relative filename given the cwd of theemacs process. This is a pure hack that suffices for this one use case so I can develop these docs with a fast workflow.