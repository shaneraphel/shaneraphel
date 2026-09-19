Aletheia is a compiled language model (`n_parameters=0`) that writes occupancy kernels: an empty tape refuses, it does not report 0.

[Show and tell](https://github.com/shaneraphel/aletheia-stemlock/discussions/3) · [compiled-llm topic](https://github.com/topics/compiled-llm)

**World model / autonomous driving** — empty next, sites, or voxels are absence: [cyclelock](https://github.com/shaneraphel/aletheia-cyclelock) · [celllock](https://github.com/shaneraphel/aletheia-celllock) · [lanelock](https://github.com/shaneraphel/aletheia-lanelock) · [voxelock](https://github.com/shaneraphel/aletheia-voxelock)

**Dexterous hand** — empty contacts are absence: [handlock](https://github.com/shaneraphel/aletheia-handlock) · [hulllock](https://github.com/shaneraphel/aletheia-hulllock) · [jointlock](https://github.com/shaneraphel/aletheia-jointlock)

**BCI / spike tapes** — empty samples are absence: [spikelock](https://github.com/shaneraphel/aletheia-spikelock) · [stemlock](https://github.com/shaneraphel/aletheia-stemlock) · [bloomlock](https://github.com/shaneraphel/aletheia-bloomlock)

## Show: I used their tool, and I refused empty occupancy

Each kernel imports the package, records their empty case, then runs the same square / tape / sites through our dest.

| repo | I used | their empty case | I built |
|---|---|---|---|
| [handlock](https://github.com/shaneraphel/aletheia-handlock/blob/main/SHOW.md) | [bmc/munkres](https://github.com/bmc/munkres) | `[[]]` is `[]` ([#54](https://github.com/bmc/munkres/issues/54)) | 2×2 assignment cost 2 |
| [needlelock](https://github.com/shaneraphel/aletheia-needlelock/blob/main/SHOW.md) | [WojciechMula/pyahocorasick](https://github.com/WojciechMula/pyahocorasick) | empty `add_word` accepted ([#225](https://github.com/WojciechMula/pyahocorasick/issues/225)) | overlapping hits 4 |
| [nearlock](https://github.com/shaneraphel/aletheia-nearlock/blob/main/SHOW.md) | [stefankoegl/kdtree](https://github.com/stefankoegl/kdtree) | empty `search_nn` is `None` ([#56](https://github.com/stefankoegl/kdtree/issues/56)) | nearest-x 3 |
| [flowlock](https://github.com/shaneraphel/aletheia-flowlock/blob/main/SHOW.md) | [networkx/networkx](https://github.com/networkx/networkx) | empty residual is flow 0 | diamond flow 2 |
| [cyclelock](https://github.com/shaneraphel/aletheia-cyclelock/blob/main/SHOW.md) | [networkx/networkx](https://github.com/networkx/networkx) | empty `simple_cycles` is `[]` | loop occupancy 1 |
| [karplock](https://github.com/shaneraphel/aletheia-karplock/blob/main/SHOW.md) | [networkx/networkx](https://github.com/networkx/networkx) | empty matching is 0 | 2×2 matching 2 |
| [prefixlock](https://github.com/shaneraphel/aletheia-prefixlock/blob/main/SHOW.md) | [numpy/numpy](https://github.com/numpy/numpy) | empty `cumsum` is `[]` | prefix 10 |
| [hulllock](https://github.com/shaneraphel/aletheia-hulllock/blob/main/SHOW.md) | [scipy/scipy](https://github.com/scipy/scipy) `ConvexHull` | no points raises | hull 4 |
| [meshlock](https://github.com/shaneraphel/aletheia-meshlock/blob/main/SHOW.md) | [scipy/scipy](https://github.com/scipy/scipy) `Delaunay` | no points raises | 4 triangles |
| [celllock](https://github.com/shaneraphel/aletheia-celllock/blob/main/SHOW.md) | [scipy/scipy](https://github.com/scipy/scipy) `Voronoi` | no points raises | unbounded cells 4 |
| [bloomlock](https://github.com/shaneraphel/aletheia-bloomlock/blob/main/SHOW.md) | [joseph-fox/python-bloomfilter](https://github.com/joseph-fox/python-bloomfilter) | empty membership is `False` | maybe-membership 1 |
| [layerlock](https://github.com/shaneraphel/aletheia-layerlock/blob/main/SHOW.md) | [networkx/networkx](https://github.com/networkx/networkx) | empty longest path is 0 | 3-layer task chain |
| [ranklock](https://github.com/shaneraphel/aletheia-ranklock/blob/main/SHOW.md) | [ilanschnell/bitarray](https://github.com/ilanschnell/bitarray) | empty `count(1)` is 0 | rank 3 |
| [rangelock](https://github.com/shaneraphel/aletheia-rangelock/blob/main/SHOW.md) | [grantjenks/python-sortedcontainers](https://github.com/grantjenks/python-sortedcontainers) | empty `irange` is `[]` | box count 2 |
| [sitelock](https://github.com/shaneraphel/aletheia-sitelock/blob/main/SHOW.md) | [scipy/scipy](https://github.com/scipy/scipy) `Voronoi` | no points raises | Fortune vertex 1 |
| [marchlock](https://github.com/shaneraphel/aletheia-marchlock/blob/main/SHOW.md) | [scipy/scipy](https://github.com/scipy/scipy) `ConvexHull` | no points raises | Jarvis hull 4 |
| [pairlock](https://github.com/shaneraphel/aletheia-pairlock/blob/main/SHOW.md) | [networkx/networkx](https://github.com/networkx/networkx) | empty matching is `set()` | pairing 2 |
| [routelock](https://github.com/shaneraphel/aletheia-routelock/blob/main/SHOW.md) | [networkx/networkx](https://github.com/networkx/networkx) | empty `johnson` is `{}` | lane distance 2 |
| [voxelock](https://github.com/shaneraphel/aletheia-voxelock/blob/main/SHOW.md) | [numpy/numpy](https://github.com/numpy/numpy) | empty `norm` is 0.0 | lidar NE 1 |
| [gridlock](https://github.com/shaneraphel/aletheia-gridlock/blob/main/SHOW.md) | [numpy/numpy](https://github.com/numpy/numpy) | empty `norm` is 0.0 | BEV NE 1 |
| [remainlock](https://github.com/shaneraphel/aletheia-remainlock/blob/main/SHOW.md) | stdlib `math.gcd` | `gcd(0,0)` is 0 | CRT 8 |
| [twistlock](https://github.com/shaneraphel/aletheia-twistlock/blob/main/SHOW.md) | [numpy/numpy](https://github.com/numpy/numpy) | empty `norm` is 0.0 | wrist hypot 5 |
| [spikelock](https://github.com/shaneraphel/aletheia-spikelock/blob/main/SHOW.md) | [numpy/numpy](https://github.com/numpy/numpy) | empty `mean` is `nan` | occupancy 3 |
| [cliplock](https://github.com/shaneraphel/aletheia-cliplock/blob/main/SHOW.md) | [scipy/scipy](https://github.com/scipy/scipy) `ConvexHull` | no points raises | interior discard 1 |
