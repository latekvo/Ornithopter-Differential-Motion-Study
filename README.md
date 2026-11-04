# Ornithopter Differential Motion Study

Interactive page: **https://latekvo.github.io/Ornithopter-Differential-Motion-Study/**

A wing angle `f` is produced differentially from two inputs that never reverse:

```
g(t) = c·t + f(t)        h(t) = c·t − f(t)        f = (g − h) / 2
```

`f` has period π. Each half-cycle is a fast stroke over `[0, k]` to the peak `±(π/2 − l)`, then a slow return to 0 at `π/2`. The sign alternates every half-cycle. The velocities `g′ = c + f′` and `h′ = c − f′` oscillate around the base speed `c`. They stay at least `o` away from zero whenever `|c| > o + max|f′|`.

| Control | Effect |
|---|---|
| `k` | length of the fast stroke |
| `c` | base speed of both inputs |
| `o` | keep-out band the velocities must clear |
| `l` | shrinks the swing to `±(π/2 − l)`, for `l ∈ [0, π/6]` |
| Linear / Smooth vel. / Smooth accel. | piecewise-linear `f`; `f′` continuous; `f′`, `f″` and `f‴` continuous |

The zeros at `nπ/2` and the peaks at `k + nπ/2` stay fixed in every mode. Press Play, or drag across the chart, to drive the dial.

It is a single `index.html` with no build step.
