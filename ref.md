- [Cricket Introduction](#org6930de0)
- [Coherent Noise](#orgece53af)
- [API](#org893d4e5)
  - [Generators](#org86f57c7)
    - [Perlin](#org4d2480e)
    - [Simplex](#orgb030a34)
    - [Open-Simplex](#orgf967dad)
    - [Open-Simplex 2F (Fast)](#orgbadb0cb)
    - [Open-Simplex 2S (Smooth)](#org42b46ca)
    - [Value](#org36d55ec)
    - [Cellular](#orge90a9b4)
    - [Cylinders](#orgd60885b)
    - [Spheres](#org24708e9)
    - [Checker](#orgeb46ca7)
    - [Constant](#org7f6867e)
    - [FBM: Fractal Brownian Motion](#orgac81b4e)
    - [Billow](#org325e3a9)
    - [Multifractal](#org810d1df)
    - [Hybrid-Multifractal](#orgf7d9fd7)
    - [Ridged-Multifractal](#org7693ea9)
  - [Modifiers](#org552292c)
    - [Function: **(+ source1 source2)**](#org3bf19a2)
    - [Function: **(- source1 source2)**](#orgb9cb987)
    - [Function: **(\*** **source1 source2)**](#org5845394)
    - [Function: **(/ source1 source2)**](#org246edd7)
    - [Function: **(abs source)**](#org91190ed)
    - [Function: **(blend source1 source2 control)**](#org625bcf5)
    - [cache](#org2c053c2)
    - [clamp](#orga46b98d)
    - [curve](#org88356b3)
    - [displace](#orgea87ebd)
    - [expt](#org12c76e4)
    - [fractalize](#orgb205f43)
    - [max](#org2e60806)
    - [negate](#org24686d1)
    - [power](#org20556cc)
    - [rotate](#orgd7715e0)
    - [scale](#org49ea366)
    - [select](#org6d3ad49)
    - [strengthen](#orgc5eee24)
    - [terrace](#org7c1f07f)
    - [translate](#org54e3b4c)
    - [turbulance](#org6d17bc3)
    - [uniform-scale](#org849107d)
  - [Map](#orgafbcba4)
    - [define-gradient](#org7bfcd95)
    - [get-image-pixel](#org687de69)
    - [image](#org96722f6)
    - [make-map](#orgbbe0d05)
    - [render-map](#org9273da5)
    - [write-image](#org10e6459)
- [Glossary](#orge1cc014)
- [References](#org027d79e)
- [Prototyping](#orgac16fa8)
  - [Org Mode Code Block Examples](#org71b7d8a)
  - [Org Mode Wisdom](#orgd1349db)
    - [<https://www.gnu.org/software/emacs/refcards/pdf/orgcard.pdf>](#org4e02c8e)
    - [<https://orgmode.org/worg/orgcard.html>](#org6999dea)
    - [<https://orgmode.org/manual/Variable-Index.html>](#org4f737b4)
    - [C-c C-x C-v - org-toggle-inline-images](#org18b6192)
    - [C-c C-v b - org-babel-execute-buffer.](#org3a89303)


<a id="org6930de0"></a>

# Cricket Introduction

This document describes the `cricket` coherent noise library. It is in the process of being written.


<a id="orgece53af"></a>

# Coherent Noise


<a id="org893d4e5"></a>

# API

Cricket's API is split into three main pieces: Generators which generate a source signal of noise, Modifiers which mutate, combine, or otherwise alter a noise signal, and Maps which control how noise gets rendered to an in memory image (which can then be stored to disk).

All of the examples show at least the simplest use of the noise function with no additional affects on it. Some examples may demonstrate additional effects in the parameter space of the functions.

For all of these examples, for package brevity, assume that this piece of code has been run in your REPL:

```lisp
(ql:quickload :cricket)
(defpackage #:my-package
  (:local-nicknames (#:c #:cricket))
  (:use #:cl))
(in-package #:my-package)
```


<a id="org86f57c7"></a>

## Generators

The Generators are demonstrated with no modifications applied to the noise signal.


<a id="org4d2480e"></a>

### Perlin

1.  Function: **(perlin-1d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs 1-dimensional Perlin Improved noise values
            ranging from -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        We encode the 1D noise into a 2D image by simply repeating the noise for each row.

        ```lisp
        (c:-> (c:perlin-1d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/perlin-1d-ex0.png)

2.  Function: **(perlin-2d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs 2-dimensional Perlin Improved noise values
            ranging from -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        ```lisp
        (c:-> (c:perlin-2d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/perlin-2d-ex0.png)

3.  Function: **(perlin-3d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs 3-dimensional Perlin Improved noise values
            ranging from -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        ```lisp
        (c:-> (c:perlin-3d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/perlin-3d-ex0.png)

4.  Function: **(perlin-4d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs 4-dimensional Perlin Improved noise values
            ranging from -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        ```lisp
        (c:-> (c:perlin-4d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/perlin-4d-ex0.png)


<a id="orgb030a34"></a>

### Simplex

1.  Function: **(simplex-1d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs 1-dimensional Simplex noise values ranging from
            -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        We encode the 1D noise into a 2D image by simply repeating the noise for each row.

        ```lisp
        (c:-> (c:simplex-1d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/simplex-1d-ex0.png)

2.  Function: **(simplex-2d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs 2-dimensional Simplex noise values ranging from
            -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        ```lisp
        (c:-> (c:simplex-2d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/simplex-2d-ex0.png)

3.  Function: **(simplex-3d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs 3-dimensional Simplex noise values ranging from
            -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        ```lisp
        (c:-> (c:simplex-3d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/simplex-3d-ex0.png)

4.  Function: **(simplex-4d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs 4-dimensional Simplex noise values ranging from
            -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        ```lisp
        (c:-> (c:simplex-4d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/simplex-4d-ex0.png)


<a id="orgf967dad"></a>

### Open-Simplex

1.  Function: **(open-simplex-2d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs 2-dimensional OpenSimplex noise values ranging
            from -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        ```lisp
        (c:-> (c:open-simplex-2d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/open-simplex-2d-ex0.png)

2.  Function: **(open-simplex-3d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs 3-dimensional OpenSimplex noise values ranging
            from -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        ```lisp
        (c:-> (c:open-simplex-3d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/open-simplex-3d-ex0.png)

3.  Function: **(open-simplex-4d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs 4-dimensional OpenSimplex noise values ranging
            from -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        ```lisp
        (c:-> (c:open-simplex-4d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/open-simplex-4d-ex0.png)

        TBD


<a id="orgbadb0cb"></a>

### Open-Simplex 2F (Fast)

1.  Function: **(open-simplex2f-2d &key seed (orientation :standard))**

    1.  Description

            Construct a sampler that, when sampled, outputs 2-dimensional OpenSimplex2F noise values ranging
            from -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

            `orientation`: One of `:standard` or `:x/y`, denoting the orientation of the lattice. `:x/y` has the
            Y axis pointing down the main diagonal, which might be more suitable for a game where Y is
            vertical (optional, default: `:standard`).

    2.  Example

        ```lisp
        (c:-> (c:open-simplex2f-2d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/open-simplex2f-2d-ex0.png)

2.  Function: **(open-simplex2f-3d &key seed (orientation :standard))**

    1.  Description

            Construct a sampler that, when sampled, outputs 3-dimensional OpenSimplex2F noise values ranging
            from -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

            `orientation`: One of `:standard`, `:xy/z`, or `:xz/y`, denoting the orientation of the lattice.
            `:xy/z` has better visual isotropy in XY, and `:xz/y` has better visual isotropy in XZ (optional,
            default: `:standard`).

    2.  Example

        ```lisp
        (c:-> (c:open-simplex2f-3d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/open-simplex2f-3d-ex0.png)

        TBD

3.  Function: **(open-simplex2f-4d &key seed (orientation :standard))**

    1.  Description

            Construct a sampler that, when sampled, outputs 4-dimensional OpenSimplex2F noise values ranging
            from -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

            `orientation`: One of `:standard`, `:xy/zw`, `:xz/yw`, or `:xyz/w`, denoting the orientation of the
            lattice. `:xy/zw` is recommended for 3D terrain where X/Y or Z/W are horizontal. `:xz/yw` is
            recommended for 3D terrain where X/Z or Y/W are horizontal. `:xyz/w` is recommended for time-varied
            animations of 3D objects, where W is time (optional, default: `:standard`).

    2.  Example

        ```lisp
        (c:-> (c:open-simplex2f-4d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/open-simplex2f-4d-ex0.png)


<a id="org42b46ca"></a>

### Open-Simplex 2S (Smooth)

1.  Function: **(open-simplex2s-2d &key seed (orientation :standard))**

    1.  Description

            Construct a sampler that, when sampled, outputs 2-dimensional OpenSimplex2S noise values ranging
            from -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

            `orientation`: One of `:standard` or `:x/y`, denoting the orientation of the lattice. `:x/y` has the
            Y axis pointing down the main diagonal, which might be more suitable for a game where Y is
            vertical (optional, default: `:standard`).

    2.  Example

        ```lisp
        (c:-> (c:open-simplex2s-2d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/open-simplex2s-2d-ex0.png)

        TBD

2.  Function: **(open-simplex2s-3d &key seed (orientation :standard))**

    1.  Description

            Construct a sampler that, when sampled, outputs 3-dimensional OpenSimplex2S noise values ranging
            from -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

            `orientation`: One of `:standard`, `:xy/z`, or `:xz/y`, denoting the orientation of the lattice.
            `:xy/z` has better visual isotropy in XY, and `:xz/y` has better visual isotropy in XZ (optional,
            default: `:standard`).

    2.  Example

        ```lisp
        (c:-> (c:open-simplex2s-3d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/open-simplex2s-3d-ex0.png)

        TBD

3.  Function: **(open-simplex2s-4d &key seed (orientation :standard))**

    1.  Description

            Construct a sampler that, when sampled, outputs 4-dimensional OpenSimplex2S noise values ranging
            from -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

            `orientation`: One of `:standard`, `:xy/zw`, `:xz/yw`, or `:xyz/w`, denoting the orientation of the
            lattice. `:xy/zw` is recommended for 3D terrain where X/Y or Z/W are horizontal. `:xz/yw` is
            recommended for 3D terrain where X/Z or Y/W are horizontal. `:xyz/w` is recommended for time-varied
            animations of 3D objects, where W is time (optional, default: `:standard`).

    2.  Example

        ```lisp
        (c:-> (c:open-simplex2s-4d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/open-simplex2s-4d-ex0.png)


<a id="org36d55ec"></a>

### Value

1.  Function: **(value-2d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs 2-dimensional value noise values ranging from
            -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        ```lisp
        (c:-> (c:value-2d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/value-2d-ex0.png)

        TBD

2.  Function: **(value-3d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs 3-dimensional value noise values ranging from
            -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        ```lisp
        (c:-> (c:value-3d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/value-3d-ex0.png)

        TBD


<a id="orge90a9b4"></a>

### Cellular

1.  Function: **(cellular-2d &key seed (distance-method :euclidean) (output-type :f1) (jitter 1.0d0))**

    1.  Description

            Construct a sampler that, when sampled, outputs 2-dimensional cellular noise values ranging from
            -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

            `distance-method`: One of `:manhattan`, `:euclidean`, `:euclidean-squared`, `:chebyshev`, or
            `:minkowski4`, denoting the distance function to use (optional, default: `:euclidean`).

            `output-type`: One of `:value`, `:f1`, `:f2`, `:f1+f2`, `:f2-f1`, `:f1*f2`, or `:f1/f2` denoting the
            features to use (optional, default: `:f1`).

            `jitter`: A real number between 0.0 and 1.0, with values closer to one randomly distributing cells
            away from their grid alignment (optional, default: 1.0).

    2.  Example

        ```lisp
        (c:-> (c:cellular-2d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/cellular-2d-ex0.png)

        TBD

2.  Function: **(cellular-3d &key seed (distance-method :euclidean) (output-type :f1) (jitter 1.0d0))**

    1.  Description

            Construct a sampler that, when sampled, outputs 3-dimensional cellular noise values ranging from
            -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

            `distance-method`: One of `:manhattan`, `:euclidean`, `:euclidean-squared`, `:chebyshev`, or
            `:minkowski4`, denoting the distance function to use (optional, default: `:euclidean`).

            `output-type`: One of `:value`, `:f1`, `:f2`, `:f1+f2`, `:f2-f1`, `:f1*f2`, or `:f1/f2` denoting the
            features to use (optional, default: `:f1`).

            `jitter`: A real number between 0.0 and 1.0, with values closer to one randomly distributing cells
            away from their grid alignment (optional, default: 1.0).

    2.  Example

        ```lisp
        (c:-> (c:cellular-3d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/cellular-3d-ex0.png)


<a id="orgd60885b"></a>

### Cylinders

1.  Function: **(cylinders-3d &key seed (frequency 1.0d0))**

    1.  Description

            Construct a sampler that, when sampled, outputs 3-dimensional concentric cylinder values ranging
            from -1.0 to 1.0. The cylinders are oriented with their length along the Z axis.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

            `frequency`: The frequency of the signal, which controls how small or large the cylinders are
            (optional, default: 1.0).

    2.  Example

        ```lisp
        (c:-> (c:cylinders-3d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/cylinders-3d-ex0.png)

        TBD


<a id="org24708e9"></a>

### Spheres

1.  Function: **(spheres-3d &key seed (frequency 1.0d0))**

    1.  Description

            Construct a sampler that, when sampled, outputs 3-dimensional concentric sphere values ranging
            from -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

            `frequency`: The frequency of the signal, which controls how small or large the spheres are
            (optional, default: 1.0).

    2.  Example

        ```lisp
        (c:-> (c:spheres-3d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/spheres-3d-ex0.png)


<a id="orgeb46ca7"></a>

### Checker

1.  Function: **(checker-2d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs a 2-dimensional checkered grid pattern, with
            values being either -1.0 or 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        ```lisp
        (c:-> (c:checker-2d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/checker-2d-ex0.png)

        TBD


<a id="org7f6867e"></a>

### Constant

1.  Function: **(constant value &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs the constant `value` supplied. This is useful for
            debugging and applications where you need to combine a constant value.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        We get gray with this result because the constant 0 is in the middle between -1 which is black, and 1, which is white.

        ```lisp
        (c:-> (c:constant 0 :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/constant-ex0.png)


<a id="orgac81b4e"></a>

### FBM: Fractal Brownian Motion

1.  Function: **(fbm-2d &key seed (generator #'cricket:open-simplex2f-2d) (octaves 4) (frequency 1.0) (lacunarity 2.0) (persistence 0.5))**

    1.  Description

            Construct a sampler that, when sampled, outputs the application of multiple octaves of a
            2-dimensional fractional Brownian motion noise, using the supplied `generator` function to construct
            each octave's sampler.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

            `generator`: a function object pointing to one of the built-in 2-dimensional generators that is used
            to construct a different sampler, each with a different seed, for each octave (optional, default
            `#'open-simplex2f-2d`).

            `octaves`: An integer between 1 and 32, denoting the number of octaves to apply (optional, default:
            4).

            `frequency`: The frequency of the first octave's signal (optional, default: 1.0).

            `lacunarity`: A multiplier that determines how quickly the frequency increases for successive
            octaves (optional, default: 2.0).

            `persistence`: A multiplier that determines how quickly the amplitude diminishes for successive
            octaves (optional, default 0.5).

    2.  Example

        ```lisp
        (c:-> (c:fbm-2d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/fbm-2d-ex0.png)

2.  Function: **(fbm-3d &key seed (generator #'cricket:open-simplex2f-3d) (octaves 4) (frequency 1.0) (lacunarity 2.0) (persistence 0.5))**

    1.  Description

            Construct a sampler that, when sampled, outputs the application of multiple octaves of a
            3-dimensional fractional Brownian motion noise, using the supplied `generator` function to construct
            each octave's sampler.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

            `generator`: a function object pointing to one of the built-in 3-dimensional generators that is used
            to construct a different sampler, each with a different seed, for each octave (optional, default
            `#'open-simplex2f-3d`).

            `octaves`: An integer between 1 and 32, denoting the number of octaves to apply (optional, default:
            4).

            `frequency`: The frequency of the first octave's signal (optional, default: 1.0).

            `lacunarity`: A multiplier that determines how quickly the frequency increases for successive
            octaves (optional, default: 2.0).

            `persistence`: A multiplier that determines how quickly the amplitude diminishes for successive
            octaves (optional, default 0.5).

    2.  Example

        ```lisp
        (c:-> (c:fbm-3d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/fbm-3d-ex0.png)

3.  Function: **(fbm-4d &key seed (generator #'cricket:open-simplex2f-4d) (octaves 4) (frequency 1.0) (lacunarity 2.0) (persistence 0.5))**

    1.  Description

            Construct a sampler that, when sampled, outputs the application of multiple octaves of a
            4-dimensional fractional Brownian motion noise, using the supplied `generator` function to construct
            each octave's sampler.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

            `generator`: a function object pointing to one of the built-in 4-dimensional generators that is used
            to construct a different sampler, each with a different seed, for each octave (optional, default
            `#'open-simplex2f-4d`).

            `octaves`: An integer between 1 and 32, denoting the number of octaves to apply (optional, default:
            4).

            `frequency`: The frequency of the first octave's signal (optional, default: 1.0).

            `lacunarity`: A multiplier that determines how quickly the frequency increases for successive
            octaves (optional, default: 2.0).

            `persistence`: A multiplier that determines how quickly the amplitude diminishes for successive
            octaves (optional, default 0.5).

    2.  Example

        ```lisp
        (c:-> (c:fbm-4d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/fbm-4d-ex0.png)


<a id="org325e3a9"></a>

### Billow

1.  Function: **(billow-2d &key seed (generator #'cricket:open-simplex2s-2d) (octaves 4) (frequency 1.0) (lacunarity 2.0) (persistence 0.5))**

    1.  Description

            Construct a sampler that, when sampled, outputs the application of multiple octaves of a
            2-dimensional billow fractal noise, using the supplied `generator` function to construct each
            octave's sampler.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

            `generator`: a function object pointing to one of the built-in 2-dimensional generators that is used
            to construct a different sampler, each with a different seed, for each octave (optional, default
            `#'open-simplex2s-2d`).

            `octaves`: An integer between 1 and 32, denoting the number of octaves to apply (optional, default:
            4).

            `frequency`: The frequency of the first octave's signal (optional, default: 1.0).

            `lacunarity`: A multiplier that determines how quickly the frequency increases for successive
            octaves (optional, default: 2.0).

            `persistence`: A multiplier that determines how quickly the amplitude diminishes for successive
            octaves (optional, default 0.5).

    2.  Example

        ```lisp
        (c:-> (c:billow-2d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/billow-2d-ex0.png)

        TBD

2.  Function: **(billow-3d &key seed (generator #'cricket:open-simplex2s-3d) (octaves 4) (frequency 1.0) (lacunarity 2.0) (persistence 0.5))**

    1.  Description

            Construct a sampler that, when sampled, outputs the application of multiple octaves of a
            3-dimensional billow fractal noise, using the supplied `generator` function to construct each
            octave's sampler.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

            `generator`: a function object pointing to one of the built-in 3-dimensional generators that is used
            to construct a different sampler, each with a different seed, for each octave (optional, default
            `#'open-simplex2s-3d`).

            `octaves`: An integer between 1 and 32, denoting the number of octaves to apply (optional, default:
            4).

            `frequency`: The frequency of the first octave's signal (optional, default: 1.0).

            `lacunarity`: A multiplier that determines how quickly the frequency increases for successive
            octaves (optional, default: 2.0).

            `persistence`: A multiplier that determines how quickly the amplitude diminishes for successive
            octaves (optional, default 0.5).

    2.  Example

        ```lisp
        (c:-> (c:billow-3d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/billow-3d-ex0.png)

3.  Function: **(billow-4d &key seed (generator #'cricket:open-simplex2s-4d) (octaves 4) (frequency 1.0) (lacunarity 2.0) (persistence 0.5))**

    1.  Description

            Construct a sampler that, when sampled, outputs the application of multiple octaves of a
            4-dimensional billow fractal noise, using the supplied `generator` function to construct each
            octave's sampler.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

            `generator`: a function object pointing to one of the built-in 4-dimensional generators that is used
            to construct a different sampler, each with a different seed, for each octave (optional, default
            `#'open-simplex2s-4d`).

            `octaves`: An integer between 1 and 32, denoting the number of octaves to apply (optional, default:
            4).

            `frequency`: The frequency of the first octave's signal (optional, default: 1.0).

            `lacunarity`: A multiplier that determines how quickly the frequency increases for successive
            octaves (optional, default: 2.0).

            `persistence`: A multiplier that determines how quickly the amplitude diminishes for successive
            octaves (optional, default 0.5).

    2.  Example

        ```lisp
        (c:-> (c:billow-4d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/billow-4d-ex0.png)


<a id="org810d1df"></a>

### Multifractal

1.  Function: (**multifractal-2d &key seed (generator #'cricket:open-simplex2s-2d) (octaves 4) (frequency 1.0) (lacunarity 2.0) (persistence 0.5))**

    1.  Description

            Construct a sampler that, when sampled, outputs the application of multiple octaves of a
            2-dimensional multifractal noise, using the supplied `generator` function to construct each octave's
            sampler.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

            `generator`: a function object pointing to one of the built-in 2-dimensional generators that is used
            to construct a different sampler, each with a different seed, for each octave (optional, default
            `#'open-simplex2s-2d`).

            `octaves`: An integer between 1 and 32, denoting the number of octaves to apply (optional, default:
            4).

            `frequency`: The frequency of the first octave's signal (optional, default: 1.0).

            `lacunarity`: A multiplier that determines how quickly the frequency increases for successive
            octaves (optional, default: 2.0).

            `persistence`: A multiplier that determines how quickly the amplitude diminishes for successive
            octaves (optional, default 0.5).

    2.  Example

        ```lisp
        (c:-> (c:multifractal-2d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/multifractal-2d-ex0.png)

        TBD

2.  Function: (**multifractal-3d &key seed (generator #'cricket:open-simplex2s-3d) (octaves 4) (frequency 1.0) (lacunarity 2.0) (persistence 0.5))**

    1.  Description

            Construct a sampler that, when sampled, outputs the application of multiple octaves of a
            3-dimensional multifractal noise, using the supplied `generator` function to construct each octave's
            sampler.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

            `generator`: a function object pointing to one of the built-in 3-dimensional generators that is used
            to construct a different sampler, each with a different seed, for each octave (optional, default
            `#'open-simplex2s-3d`).

            `octaves`: An integer between 1 and 32, denoting the number of octaves to apply (optional, default:
            4).

            `frequency`: The frequency of the first octave's signal (optional, default: 1.0).

            `lacunarity`: A multiplier that determines how quickly the frequency increases for successive
            octaves (optional, default: 2.0).

            `persistence`: A multiplier that determines how quickly the amplitude diminishes for successive
            octaves (optional, default 0.5).

    2.  Example

        ```lisp
        (c:-> (c:multifractal-3d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/multifractal-3d-ex0.png)

        TBD

3.  Function: (**multifractal-4d &key seed (generator #'cricket:open-simplex2s-4d) (octaves 4) (frequency 1.0) (lacunarity 2.0) (persistence 0.5))**

    1.  Description

            Construct a sampler that, when sampled, outputs the application of multiple octaves of a
            4-dimensional multifractal noise, using the supplied `generator` function to construct each octave's
            sampler.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

            `generator`: a function object pointing to one of the built-in 4-dimensional generators that is used
            to construct a different sampler, each with a different seed, for each octave (optional, default
            `#'open-simplex2s-4d`).

            `octaves`: An integer between 1 and 32, denoting the number of octaves to apply (optional, default:
            4).

            `frequency`: The frequency of the first octave's signal (optional, default: 1.0).

            `lacunarity`: A multiplier that determines how quickly the frequency increases for successive
            octaves (optional, default: 2.0).

            `persistence`: A multiplier that determines how quickly the amplitude diminishes for successive
            octaves (optional, default 0.5).

    2.  Example

        ```lisp
        (c:-> (c:multifractal-4d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/multifractal-4d-ex0.png)


<a id="orgf7d9fd7"></a>

### Hybrid-Multifractal

1.  Function: **(hybrid-multifractal-2d &key seed (generator #'cricket:open-simplex2s-2d) (octaves 4) (frequency 1.0) (lacunarity 2.0) (persistence 0.25))**

    1.  Description

            Construct a sampler that, when sampled, outputs the application of multiple octaves of a
            2-dimensional hybrid multifractal noise, using the supplied `generator` function to construct each
            octave's sampler.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

            `generator`: a function object pointing to one of the built-in 2-dimensional generators that is used
            to construct a different sampler, each with a different seed, for each octave (optional, default
            `#'open-simplex2s-2d`).

            `octaves`: An integer between 1 and 32, denoting the number of octaves to apply (optional, default:
            4).

            `frequency`: The frequency of the first octave's signal (optional, default: 1.0).

            `lacunarity`: A multiplier that determines how quickly the frequency increases for successive
            octaves (optional, default: 2.0).

            `persistence`: A multiplier that determines how quickly the amplitude diminishes for successive
            octaves (optional, default 0.25).

    2.  Example

        ```lisp
        (c:-> (c:hybrid-multifractal-2d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/hybrid-multifractal-2d-ex0.png)

2.  Function: **(hybrid-multifractal-3d &key seed (generator #'cricket:open-simplex2s-3d) (octaves 4) (frequency 1.0) (lacunarity 2.0) (persistence 0.25))**

    1.  Description

            Construct a sampler that, when sampled, outputs the application of multiple octaves of a
            3-dimensional hybrid multifractal noise, using the supplied `generator` function to construct each
            octave's sampler.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

            `generator`: a function object pointing to one of the built-in 3-dimensional generators that is used
            to construct a different sampler, each with a different seed, for each octave (optional, default
            `#'open-simplex2s-3d`).

            `octaves`: An integer between 1 and 32, denoting the number of octaves to apply (optional, default:
            4).

            `frequency`: The frequency of the first octave's signal (optional, default: 1.0).

            `lacunarity`: A multiplier that determines how quickly the frequency increases for successive
            octaves (optional, default: 2.0).

            `persistence`: A multiplier that determines how quickly the amplitude diminishes for successive
            octaves (optional, default 0.25).

    2.  Example

        ```lisp
        (c:-> (c:hybrid-multifractal-3d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/hybrid-multifractal-3d-ex0.png)

3.  Function: **(hybrid-multifractal-4d &key seed (generator #'cricket:open-simplex2s-4d) (octaves 4) (frequency 1.0) (lacunarity 2.0) (persistence 0.25))**

    1.  Description

            Construct a sampler that, when sampled, outputs the application of multiple octaves of a
            4-dimensional hybrid multifractal noise, using the supplied `generator` function to construct each
            octave's sampler.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

            `generator`: a function object pointing to one of the built-in 4-dimensional generators that is used
            to construct a different sampler, each with a different seed, for each octave (optional, default
            `#'open-simplex2s-4d`).

            `octaves`: An integer between 1 and 32, denoting the number of octaves to apply (optional, default:
            4).

            `frequency`: The frequency of the first octave's signal (optional, default: 1.0).

            `lacunarity`: A multiplier that determines how quickly the frequency increases for successive
            octaves (optional, default: 2.0).

            `persistence`: A multiplier that determines how quickly the amplitude diminishes for successive
            octaves (optional, default 0.25).

    2.  Example

        ```lisp
        (c:-> (c:hybrid-multifractal-4d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/hybrid-multifractal-4d-ex0.png)


<a id="org7693ea9"></a>

### Ridged-Multifractal

1.  Function: **(ridged-multifractal-2d &key seed (generator #'cricket:open-simplex2s-2d) (octaves 4) (frequency 1.0) (lacunarity 2.0) (persistence 1.0) (attenuation 2.0))**

    1.  Description

            Construct a sampler that, when sampled, outputs the application of multiple octaves of a
            2-dimensional ridged multifractal noise, using the supplied `generator` function to construct each
            octave's sampler.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

            `generator`: a function object pointing to one of the built-in 2-dimensional generators that is used
            to construct a different sampler, each with a different seed, for each octave (optional, default
            `#'open-simplex2s-2d`).

            `octaves`: An integer between 1 and 32, denoting the number of octaves to apply (optional, default:
            4).

            `frequency`: The frequency of the first octave's signal (optional, default: 1.0).

            `lacunarity`: A multiplier that determines how quickly the frequency increases for successive
            octaves (optional, default: 2.0).

            `persistence`: A multiplier that determines how quickly the amplitude diminishes for successive
            octaves (optional, default 1.0).

            `attenuation`: The attenuation to apply to the weight of each octave (optional, default: 2.0).

    2.  Example

        ```lisp
        (c:-> (c:ridged-multifractal-2d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/ridged-multifractal-2d-ex0.png)

2.  Function: **(ridged-multifractal-3d &key seed (generator #'cricket:open-simplex2s-3d) (octaves 4) (frequency 1.0) (lacunarity 2.0) (persistence 1.0) (attenuation 2.0))**

    1.  Description

            Construct a sampler that, when sampled, outputs the application of multiple octaves of a
            3-dimensional ridged multifractal noise, using the supplied `generator` function to construct each
            octave's sampler.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

            `generator`: a function object pointing to one of the built-in 3-dimensional generators that is used
            to construct a different sampler, each with a different seed, for each octave (optional, default
            `#'open-simplex2s-3d`).

            `octaves`: An integer between 1 and 32, denoting the number of octaves to apply (optional, default:
            4).

            `frequency`: The frequency of the first octave's signal (optional, default: 1.0).

            `lacunarity`: A multiplier that determines how quickly the frequency increases for successive
            octaves (optional, default: 2.0).

            `persistence`: A multiplier that determines how quickly the amplitude diminishes for successive
            octaves (optional, default 1.0).

            `attenuation`: The attenuation to apply to the weight of each octave (optional, default: 2.0).

    2.  Example

        ```lisp
        (c:-> (c:ridged-multifractal-3d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/ridged-multifractal-3d-ex0.png)

3.  Function: **(ridged-multifractal-4d &key seed (generator #'cricket:open-simplex2s-4d) (octaves 4) (frequency 1.0) (lacunarity 2.0) (persistence 1.0) (attenuation 2.0))**

    1.  Description

            Construct a sampler that, when sampled, outputs the application of multiple octaves of a
            4-dimensional ridged multifractal noise, using the supplied `generator` function to construct each
            octave's sampler.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

            `generator`: a function object pointing to one of the built-in 4-dimensional generators that is used
            to construct a different sampler, each with a different seed, for each octave (optional, default
            `#'open-simplex2s-4d`).

            `octaves`: An integer between 1 and 32, denoting the number of octaves to apply (optional, default:
            4).

            `frequency`: The frequency of the first octave's signal (optional, default: 1.0).

            `lacunarity`: A multiplier that determines how quickly the frequency increases for successive
            octaves (optional, default: 2.0).

            `persistence`: A multiplier that determines how quickly the amplitude diminishes for successive
            octaves (optional, default 1.0).

            `attenuation`: The attenuation to apply to the weight of each octave (optional, default: 2.0).

    2.  Example

        ```lisp
        (c:-> (c:ridged-multifractal-4d :seed "example")
          (c:make-map :width 256 :height 256)
          (c:render-map)
          (c:write-image arg))
        ```

        ![img](./img/api/ridged-multifractal-4d-ex0.png)


<a id="org552292c"></a>

## Modifiers

Some of examples in these modifiers use `strengthen` in the resultant noise signal in order to rescale the output so it fits into the color range of the image. Otherwise, as minimal examples as possible are constructed.


<a id="org3bf19a2"></a>

### Function: **(+ source1 source2)**

1.  Description

        Construct a sampler that, when sampled, outputs the result of adding the outputs of `source1` and
        `source2`.

        `source1`: The first input sampler (required).

        `source2`: The second input sampler (required).

2.  Example

    This example averages two noise sources together.

    ```lisp
    (c:-> (c:+ (c:billow-2d :seed "example")
               (c:checker-2d :seed "example"))
      (c:strengthen 1/2)
      (c:make-map :width 256 :height 256)
      (c:render-map)
      (c:write-image arg))
    ```

    ![img](./img/api/plus-ex0.png)


<a id="orgb9cb987"></a>

### Function: **(- source1 source2)**

1.  Description

        Construct a sampler that, when sampled, outputs the result of subtracting the output `source2`
        from the output of `source1`.

        `source1`: The first input sampler (required).

        `source2`: The second input sampler (required).

2.  Example

    ```lisp
    (c:-> (c:- (c:checker-2d :seed "example")
               (c:checker-2d :seed "example"))
      (c:make-map :width 256 :height 256)
      (c:render-map)
      (c:write-image arg))
    ```

    ![img](./img/api/minus-ex0.png)


<a id="org5845394"></a>

### Function: **(\*** **source1 source2)**

1.  Description

        Construct a sampler that, when sampled, outputs the result of multiplying the outputs of
        `source1` and `source2`.

        `source1`: The first input sampler (required).

        `source2`: The second input sampler (required).

2.  Example

    The multiplication occurs in the [-1, 1] domain by default.

    ```lisp
    (c:-> (c:* (c:billow-2d :seed "example")
               (c:checker-2d :seed "example"))
      (c:make-map :width 256 :height 256)
      (c:render-map)
      (c:write-image arg))
    ```

    ![img](./img/api/times-ex0.png)

    If you wanted to use the checker noise like a mask, you must rescale both noises into the [0, 1] domain, perform the multiplication there, and rescale it back to [-1, 1] domain.

    ```lisp
    (c:-> (c:* (c:-> (c:billow-2d :seed "example")
                 (c:strengthen 1/2 :bias .5))
               (c:-> (c:checker-2d :seed "example")
                 (c:strengthen 1/2 :bias .5)))
      (c:strengthen 2 :bias -1)
      (c:make-map :width 256 :height 256)
      (c:render-map)
      (c:write-image arg))
    ```

    ![img](./img/api/times-ex1.png)


<a id="org246edd7"></a>

### Function: **(/ source1 source2)**

1.  Description

        Construct a sampler that, when sampled, outputs the result of dividing the output `source1` by
        the output of `source2`.

        `source1`: The first input sampler (required).

        `source2`: The second input sampler (required).

2.  Example

    The division occurs in the [-1, 1] domain by default.

    Any denominator which is zero will result in a zero result from the division.

    ```lisp
    (c:-> (c:/ (c:spheres-3d :seed "example")
               (c:checker-2d :seed "example"))
      (c:make-map :width 256 :height 256)
      (c:render-map)
      (c:write-image arg))
    ```

    ![img](./img/api/div-ex0.png)

    If you want the division to be in terms of the black to white range, the sources and result must be normalized into the 0 to 1 domain to perform the processing there, and then converted back to the -1 to 1 domain afterwards.

    ```lisp
    (c:-> (c:/ (c:-> (c:spheres-3d :seed "example")
                 (c:strengthen 1/2 :bias .5))
               (c:-> (c:checker-2d :seed "example")
                 (c:strengthen 1/2 :bias .5)))
      (c:strengthen 2 :bias -1)
      (c:make-map :width 256 :height 256)
      (c:render-map)
      (c:write-image arg))
    ```

    ![img](./img/api/div-ex1.png)


<a id="org91190ed"></a>

### Function: **(abs source)**

1.  Description

        Construct a sampler that, when sampled, outputs the absolute value of the output of `source`.

        `source`: The input sampler (required).

2.  Example

    ```lisp
    (c:-> (c:spheres-3d :seed "example")
      (c:abs)
      (c:make-map :width 256 :height 256)
      (c:render-map)
      (c:write-image arg))
    ```

    ![img](./img/api/abs-ex0.png)


<a id="org625bcf5"></a>

### Function: **(blend source1 source2 control)**

1.  Description

        Construct a sampler that, when sampled, outputs a blend between the outputs of `source1` and
        `source2`, by means of a linear interpolation using the output value of `control` as the
        interpolation parameter.

        If the output of `control` is negative, the blended output is weighted towards the output of
        `source1`. If the output of `control` is positive, the blended output is weighted towards the output
        of `source2`.

        `source1`: The sampler to weight towards if the output of `control` is negative (required).

        `source2`: The sampler to weight towards if the output of `control` is positive (required).

        `control`: The sampler that determines the weight of the blending operation (required).

2.  Example

    This example shows the control noise as being the checker-2d so in white areas of the checker we take 100% of the billow-2d and in the black portion of the checker we take 100% of the spheres-3d noise.

    ```lisp
    (c:-> (c:blend (c:spheres-3d :seed "example")
                   (c:billow-2d :seed "example")
                   (c:checker-2d :seed "example"))
      (c:make-map :width 256 :height 256)
      (c:render-map)
      (c:write-image arg))
    ```

    ![img](./img/api/blend-ex0.png)

    In this example, we use a spheres-3d (see above) as the control noise that produces smooth values from -1 to 1. We see how when the sphere-3d values are near -1 (black) we choose the checker-2d pattern and when near 1 (white) we choose the billow-2d pattern. Any value in between interpolates from the checker-2d to the billow-2d noise.

    TODO: I believe c:blend has a bug, confim it. -psilord

    ```lisp
    (c:-> (c:blend (c:checker-2d :seed "example")
                   (c:billow-2d :seed "example")
                   (c:spheres-3d :seed "example"))
      (c:make-map :width 256 :height 256)
      (c:render-map)
      (c:write-image arg))
    ```

    ![img](./img/api/blend-ex1.png)


<a id="org2c053c2"></a>

### cache


<a id="orga46b98d"></a>

### clamp


<a id="org88356b3"></a>

### curve


<a id="orgea87ebd"></a>

### displace


<a id="org12c76e4"></a>

### expt


<a id="orgb205f43"></a>

### fractalize


<a id="org2e60806"></a>

### max


<a id="org24686d1"></a>

### negate


<a id="org20556cc"></a>

### power


<a id="orgd7715e0"></a>

### rotate


<a id="org49ea366"></a>

### scale


<a id="org6d3ad49"></a>

### select


<a id="orgc5eee24"></a>

### strengthen


<a id="org7c1f07f"></a>

### terrace


<a id="org54e3b4c"></a>

### translate


<a id="org6d17bc3"></a>

### turbulance


<a id="org849107d"></a>

### uniform-scale


<a id="orgafbcba4"></a>

## Map


<a id="org7bfcd95"></a>

### define-gradient


<a id="org687de69"></a>

### get-image-pixel


<a id="org96722f6"></a>

### image

1.  image-height

2.  image-width

3.  image-data


<a id="orgbbe0d05"></a>

### make-map

1.  map-data

2.  map-height

3.  map-value

4.  map-width


<a id="org9273da5"></a>

### render-map


<a id="org10e6459"></a>

### write-image


<a id="orge1cc014"></a>

# Glossary


<a id="org027d79e"></a>

# References


<a id="orgac16fa8"></a>

# Prototyping

Remove this entire section when the org more docs are complete.


<a id="org71b7d8a"></a>

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
  (c:fractalize :fbm :octaves 5)
  (c:make-map :width 256 :height 256)
  (c:render-map)
  (c:write-image arg))
```

![img](./img/proto/proto-0.png)

Example text.

;; #+HEADER: :dir ~/quicklisp/local-projects/cricket-docs/img/proto

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

```lisp
(c:define-gradient (wood)
  (-1 (189 94 4 255))
  (0.5 (144 48 6 255))
  (1.0 (60 10 8 255)))

(c:-> (c:+ (c:cylinders-3d :seed "a" :frequency 16)
           (c:-> (c:multifractal-3d :seed "a" :frequency 48 :lacunarity 2.20703125 :octaves 3)
             (c:scale :z 4)
             (c:strengthen 0.25 :bias 0.125)))
  (c:turbulence (c:perlin-3d :seed "a") :frequency 4 :power (/ 256) :roughness 4)
  (c:translate :y 1.48)
  (c:rotate :x 1.46607)
  (c:turbulence (c:perlin-3d :seed "a") :frequency 2 :power (/ 64) :roughness 4)
  (c:rotate :z pi)
  (c:make-map :width 256 :height 256)
  (c:render-map :gradient 'wood)
  (c:write-image arg))
```

![img](./img/proto/proto-2.png)

```lisp
(c:define-gradient (jade)
  (-1 (24 146 102 255))
  (0 (78 154 115 255))
  (0.25 (128 204 165 255))
  (0.375 (78 154 115 255))
  (1 (29 135 102 255)))

(c:-> (c:+ (c:ridged-multifractal-3d :seed "a" :octaves 6 :frequency 2 :lacunarity 2.20703125)
           (c:-> (c:cylinders-3d :seed "a" :frequency 2)
             (c:rotate :x 1.570796 :y 0.436332 :z 0.087266)
             (c:turbulence (c:perlin-3d :seed "a")
                           :frequency 4
                           :power (/ 4)
                           :roughness 4)
             (c:strengthen 0.25)))
  (c:turbulence (c:perlin-3d :seed "a")
                :frequency 4
                :power (/ 16)
                :roughness 2)
  (c:make-map :width 256 :height 256 :x-min -5 :x-max 5 :y-min -5 :y-max 5)
  (c:render-map :gradient 'jade)
  (c:write-image arg))
```

![img](./img/proto/proto-3.png)

Documentation retrival test:

**(perlin-2d &key seed)**

    Construct a sampler that, when sampled, outputs 2-dimensional Perlin Improved noise values
    ranging from -1.0 to 1.0.

    `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
    supplied, one will be generated automatically which will negatively affect the reproducibility of
    the noise (optional, default: NIL).


<a id="orgd1349db"></a>

## Org Mode Wisdom


<a id="org4e02c8e"></a>

### <https://www.gnu.org/software/emacs/refcards/pdf/orgcard.pdf>


<a id="org6999dea"></a>

### <https://orgmode.org/worg/orgcard.html>


<a id="org4f737b4"></a>

### <https://orgmode.org/manual/Variable-Index.html>


<a id="org18b6192"></a>

### C-c C-x C-v - org-toggle-inline-images

Used to toggle all inline images on and off.


<a id="org3a89303"></a>

### C-c C-v b - org-babel-execute-buffer.

Execute all code blocks in the buffer and update the results.