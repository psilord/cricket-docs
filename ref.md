- [Cricket Introduction](#org8ae4dd3)
- [Coherent Noise](#orgbd4ff32)
- [API](#orgcd6aa6b)
  - [Generators](#org193e149)
  - [Modifiers](#orgc1337ee)
  - [Map](#orgc40861a)
- [Glossary](#org148c316)
- [References](#orgafa820c)
- [Prototyping](#org40b1114)
  - [Org Mode Code Block Examples](#org455bc16)
  - [Org Mode Wisdom](#org04378ba)



<a id="org8ae4dd3"></a>

# Cricket Introduction

This document describes the `cricket` coherent noise library. It is in the process of being written.


<a id="orgbd4ff32"></a>

# Coherent Noise


<a id="orgcd6aa6b"></a>

# API


<a id="org193e149"></a>

## Generators


### Perlin

1.  Function: **(perlin-1d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs 1-dimensional Perlin Improved noise values
            ranging from -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        TBD

2.  Function: **(perlin-2d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs 2-dimensional Perlin Improved noise values
            ranging from -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        TBD

3.  Function: **(perlin-3d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs 3-dimensional Perlin Improved noise values
            ranging from -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        TBD

4.  Function: **(perlin-4d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs 4-dimensional Perlin Improved noise values
            ranging from -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        TBD


### Simplex

1.  Function: **(simplex-1d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs 1-dimensional Simplex noise values ranging from
            -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        TBD

2.  Function: **(simplex-2d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs 2-dimensional Simplex noise values ranging from
            -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        TBD

3.  Function: **(simplex-3d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs 3-dimensional Simplex noise values ranging from
            -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        TBD

4.  Function: **(simplex-4d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs 4-dimensional Simplex noise values ranging from
            -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        TBD


### Open-Simplex

1.  Function: **(open-simplex-2d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs 2-dimensional OpenSimplex noise values ranging
            from -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        TBD

2.  Function: **(open-simplex-3d \*key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs 3-dimensional OpenSimplex noise values ranging
            from -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        TBD

3.  Function: **(open-simplex-4d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs 4-dimensional OpenSimplex noise values ranging
            from -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        TBD

4.  Function: **(open-simplex2f-2d &key seed (orientation :standard))**

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

        TBD

5.  Function: **(open-simplex2f-3d &key seed (orientation :standard))**

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

        TBD

6.  Function: **(open-simplex2f-4d &key seed (orientation :standard))**

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

        TBD

7.  Function: **(open-simplex2s-2d &key seed (orientation :standard))**

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

        TBD

8.  Function: **(open-simplex2s-3d &key seed (orientation :standard))**

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

        TBD

9.  Function: **(open-simplex2s-4d &key seed (orientation :standard))**

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

        TBD


### Value

1.  Function: **(value-2d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs 2-dimensional value noise values ranging from
            -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        TBD

2.  Function: **(value-3d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs 3-dimensional value noise values ranging from
            -1.0 to 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        TBD


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

        TBD


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

        TBD


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

        TBD


### Checker

1.  Function: **(checker-2d &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs a 2-dimensional checkered grid pattern, with
            values being either -1.0 or 1.0.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        TBD


### Constant

1.  Function: **(constant value &key seed)**

    1.  Description

            Construct a sampler that, when sampled, outputs the constant `value` supplied. This is useful for
            debugging and applications where you need to combine a constant value.

            `seed`: A string used to seed the random number generator for this sampler, or NIL. If a seed is not
            supplied, one will be generated automatically which will negatively affect the reproducibility of
            the noise (optional, default: NIL).

    2.  Example

        TBD


### FBM: Fractal Brownian Motion

1.  Function: **(fbm-2d &key seed (generator #'cricket.generators:open-simplex2f-2d) (octaves 4) (frequency 1.0) (lacunarity 2.0) (persistence 0.5))**

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

        TBD

2.  fbm-3d

3.  fbm-4d


### Billow

1.  billow-2d

2.  billow-3d

3.  billow-4d


### Multifractal

1.  multifractal-2d

2.  multifractal-3d

3.  multifractal-4d


### Hybrid-Multifractal

1.  hybrid-multifractal-2d

2.  hybrid-multifractal-3d

3.  hybrid-multifractal-4d


### Ridged-Multifractal

1.  ridged-multifractal-2d

2.  ridged-multifractal-3d

3.  ridged-multifractal-4d


<a id="orgc1337ee"></a>

## Modifiers


### +


### -


### \*


### /


### abs


### blend


### cache


### clamp


### curve


### displace


### expt


### fractalize


### max


### negate


### power


### rotate


### scale


### select


### strengthen


### terrace


### translate


### turbulance


### uniform-scale


<a id="orgc40861a"></a>

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


<a id="org148c316"></a>

# Glossary


<a id="orgafa820c"></a>

# References


<a id="org40b1114"></a>

# Prototyping

Remove this entire section when the org more docs are complete.


<a id="org455bc16"></a>

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


<a id="org04378ba"></a>

## Org Mode Wisdom


### <https://www.gnu.org/software/emacs/refcards/pdf/orgcard.pdf>


### <https://orgmode.org/worg/orgcard.html>


### <https://orgmode.org/manual/Variable-Index.html>


### C-c C-x C-v - org-toggle-inline-images

Used to toggle all inline images on and off.


### C-c C-v b - org-babel-execute-buffer.

Execute all code blocks in the buffer and update the results.