# Setfield

[![DocStable](https://img.shields.io/badge/docs-stable-blue.svg)](https://juliaobjects.github.io/Setfield.jl/stable/intro)
[![DocDev](https://img.shields.io/badge/docs-dev-blue.svg)](https://juliaobjects.github.io/Setfield.jl/dev/intro)
![CI](https://github.com/jw3126/Setfield.jl/workflows/CI/badge.svg)
[![codecov.io](https://codecov.io/github/jw3126/Setfield.jl/coverage.svg?branch=master)](http://codecov.io/github/jw3126/Setfield.jl?branch=master)


Update deeply nested immutable structs.

# Lifecycle

We plan to maintain `Setfield.jl` for a long time (written 2020-09-21, reinforced 2021-08-01). We will however not add new features. For an experimental stage
successor, see [Accessors.jl](https://github.com/JuliaObjects/Accessors.jl).

# Usage
Updating deeply nested immutable structs was never easier:
```julia
using Setfield
@set obj.a.b.c = d
```
For more information, see [the documentation](https://jw3126.github.io/Setfield.jl/latest/intro/) and/or watch this video:

[![JuliaCon2020 Changing the immutable](https://img.youtube.com/vi/vkAOYeTpLg0/0.jpg)](https://youtu.be/vkAOYeTpLg0 "Changing the immutable")

# Some creative usages of Setfield

* [VegaLite.jl](https://github.com/queryverse/VegaLite.jl) overloads
  `getproperty` and lens API to manipulate JSON-based nested objects.

* [Kaleido.jl](https://github.com/tkf/Kaleido.jl) is a library of
  additional lenses.

* [PhaseSpaceIO.jl](https://github.com/jw3126/PhaseSpaceIO.jl) overloads
  `getproperty` and `setproperties` to get/set values from/in packed bits.
