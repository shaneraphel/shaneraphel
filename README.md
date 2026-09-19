Aletheia is a compiled language model (`n_parameters=0`) that writes occupancy kernels: an empty tape refuses, it does not report 0.

[Show and tell](https://github.com/shaneraphel/aletheia-stemlock/discussions/3) · [compiled-llm topic](https://github.com/topics/compiled-llm)

**World model / autonomous driving** — empty next, sites, or voxels are absence: [cyclelock](https://github.com/shaneraphel/aletheia-cyclelock) · [celllock](https://github.com/shaneraphel/aletheia-celllock) · [lanelock](https://github.com/shaneraphel/aletheia-lanelock) · [voxelock](https://github.com/shaneraphel/aletheia-voxelock) · [kalmanlock](https://github.com/shaneraphel/aletheia-kalmanlock) · [slotlock](https://github.com/shaneraphel/aletheia-slotlock) · [orbitlock](https://github.com/shaneraphel/aletheia-orbitlock) · [bridgelock](https://github.com/shaneraphel/aletheia-bridgelock) · [clearlock](https://github.com/shaneraphel/aletheia-clearlock) · [obstlock](https://github.com/shaneraphel/aletheia-obstlock) · [worldtick](https://github.com/shaneraphel/aletheia-worldtick) · [wallock](https://github.com/shaneraphel/aletheia-wallock) · [cagelock](https://github.com/shaneraphel/aletheia-cagelock) · [sidelock](https://github.com/shaneraphel/aletheia-sidelock) · [tourlock](https://github.com/shaneraphel/aletheia-tourlock) · [shiftlock](https://github.com/shaneraphel/aletheia-shiftlock) · [woodlock](https://github.com/shaneraphel/aletheia-woodlock) · [taplock](https://github.com/shaneraphel/aletheia-taplock) · [racelock](https://github.com/shaneraphel/aletheia-racelock) · [gaplock](https://github.com/shaneraphel/aletheia-gaplock) · [climblock](https://github.com/shaneraphel/aletheia-climblock) · [floodlock](https://github.com/shaneraphel/aletheia-floodlock) · [buslock](https://github.com/shaneraphel/aletheia-buslock) · [jumplock](https://github.com/shaneraphel/aletheia-jumplock) · [coinlock](https://github.com/shaneraphel/aletheia-coinlock) · [sicklock](https://github.com/shaneraphel/aletheia-sicklock)

**Dexterous hand** — empty contacts are absence: [handlock](https://github.com/shaneraphel/aletheia-handlock) · [hulllock](https://github.com/shaneraphel/aletheia-hulllock) · [jointlock](https://github.com/shaneraphel/aletheia-jointlock) · [hookelock](https://github.com/shaneraphel/aletheia-hookelock) · [camlock](https://github.com/shaneraphel/aletheia-camlock) · [fingerlock](https://github.com/shaneraphel/aletheia-fingerlock) · [reachlock](https://github.com/shaneraphel/aletheia-reachlock) · [holdlock](https://github.com/shaneraphel/aletheia-holdlock) · [jumplock](https://github.com/shaneraphel/aletheia-jumplock)

**BCI / spike tapes** — empty samples are absence: [spikelock](https://github.com/shaneraphel/aletheia-spikelock) · [stemlock](https://github.com/shaneraphel/aletheia-stemlock) · [bloomlock](https://github.com/shaneraphel/aletheia-bloomlock) · [gaplock](https://github.com/shaneraphel/aletheia-gaplock) · [sicklock](https://github.com/shaneraphel/aletheia-sicklock)

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
| [kalmanlock](https://github.com/shaneraphel/aletheia-kalmanlock/blob/main/SHOW.md) | [rlabbe/filterpy](https://github.com/rlabbe/filterpy) | `update(None)` accepted ([#333](https://github.com/rlabbe/filterpy/issues/333)) | occupancy 3 |
| [hookelock](https://github.com/shaneraphel/aletheia-hookelock/blob/main/SHOW.md) | [numpy/numpy](https://github.com/numpy/numpy) | empty `norm` is 0.0 | spring occupancy 3 |
| [slotlock](https://github.com/shaneraphel/aletheia-slotlock/blob/main/SHOW.md) | [chaimleib/intervaltree](https://github.com/chaimleib/intervaltree) | empty `at` is `[]` ([#159](https://github.com/chaimleib/intervaltree/issues/159)) | overlap 2 |
| [orbitlock](https://github.com/shaneraphel/aletheia-orbitlock/blob/main/SHOW.md) | [networkx/networkx](https://github.com/networkx/networkx) | empty components is 0 | four-node orbits 2 |
| [bridgelock](https://github.com/shaneraphel/aletheia-bridgelock/blob/main/SHOW.md) | [networkx/networkx](https://github.com/networkx/networkx) | empty bridges is `[]` | triangle-pending 1 |
| [clearlock](https://github.com/shaneraphel/aletheia-clearlock/blob/main/SHOW.md) | [numpy/numpy](https://github.com/numpy/numpy) | empty `norm` is 0.0 | sdf occupancy 3 |
| [camlock](https://github.com/shaneraphel/aletheia-camlock/blob/main/SHOW.md) | [networkx/networkx](https://github.com/networkx/networkx) | empty nodes is `[]` | camera cover 1 |
| [fingerlock](https://github.com/shaneraphel/aletheia-fingerlock/blob/main/SHOW.md) | [numpy/numpy](https://github.com/numpy/numpy) | empty `norm` is 0.0 | two-finger 3 |
| [obstlock](https://github.com/shaneraphel/aletheia-obstlock/blob/main/SHOW.md) | [numpy/numpy](https://github.com/numpy/numpy) | empty `norm` is 0.0 | obstacle path 6 |
| [cuckoolock](https://github.com/shaneraphel/aletheia-cuckoolock/blob/main/SHOW.md) | stdlib `dict` | empty `get` is `None` | placed 3 |
| [splaylock](https://github.com/shaneraphel/aletheia-splaylock/blob/main/SHOW.md) | [grantjenks/python-sortedcontainers](https://github.com/grantjenks/python-sortedcontainers) | empty membership is `False` | splay-to-root 1 |
| [treaplock](https://github.com/shaneraphel/aletheia-treaplock/blob/main/SHOW.md) | stdlib `heapq` | empty `heappop` raises | treap root 3 |
| [skiplock](https://github.com/shaneraphel/aletheia-skiplock/blob/main/SHOW.md) | [grantjenks/python-sortedcontainers](https://github.com/grantjenks/python-sortedcontainers) | empty `index` raises | skip index 2 |
| [suffixlock](https://github.com/shaneraphel/aletheia-suffixlock/blob/main/SHOW.md) | [WojciechMula/pyahocorasick](https://github.com/WojciechMula/pyahocorasick) | empty `add_word` accepted | suffix links 3 |
| [wavelock](https://github.com/shaneraphel/aletheia-wavelock/blob/main/SHOW.md) | [numpy/numpy](https://github.com/numpy/numpy) | empty `count_nonzero` is 0 | prefix rank 3 |
| [worldtick](https://github.com/shaneraphel/aletheia-worldtick/blob/main/SHOW.md) | [networkx/networkx](https://github.com/networkx/networkx) | empty nodes is `[]` | world reach 3 |
| [reachlock](https://github.com/shaneraphel/aletheia-reachlock/blob/main/SHOW.md) | [numpy/numpy](https://github.com/numpy/numpy) | empty `norm` is 0.0 | two-link reach |
| [philock](https://github.com/shaneraphel/aletheia-philock/blob/main/SHOW.md) | [networkx/networkx](https://github.com/networkx/networkx) | empty nodes is `[]` | one phi site |
| [climblock](https://github.com/shaneraphel/aletheia-climblock/blob/main/SHOW.md) | [numpy/numpy](https://github.com/numpy/numpy) | empty `max` raises | height path 4 |
| [floodlock](https://github.com/shaneraphel/aletheia-floodlock/blob/main/SHOW.md) | [numpy/numpy](https://github.com/numpy/numpy) | empty `max` raises | rising-water 3 |
| [buslock](https://github.com/shaneraphel/aletheia-buslock/blob/main/SHOW.md) | [networkx/networkx](https://github.com/networkx/networkx) | empty `shortest_path` raises | two-route hop 2 |
| [holdlock](https://github.com/shaneraphel/aletheia-holdlock/blob/main/SHOW.md) | [networkx/networkx](https://github.com/networkx/networkx) | empty matching is `set()` | couple swap 1 |
| [wallock](https://github.com/shaneraphel/aletheia-wallock/blob/main/SHOW.md) | [numpy/numpy](https://github.com/numpy/numpy) | empty `norm` is 0.0 | removals 2 |
| [cagelock](https://github.com/shaneraphel/aletheia-cagelock/blob/main/SHOW.md) | [numpy/numpy](https://github.com/numpy/numpy) | empty `norm` is 0.0 | walls 10 |
| [sidelock](https://github.com/shaneraphel/aletheia-sidelock/blob/main/SHOW.md) | [numpy/numpy](https://github.com/numpy/numpy) | empty `count_nonzero` is 0 | left-visible 3 |
| [tourlock](https://github.com/shaneraphel/aletheia-tourlock/blob/main/SHOW.md) | [networkx/networkx](https://github.com/networkx/networkx) | empty nodes is `[]` | tour length 4 |
| [shiftlock](https://github.com/shaneraphel/aletheia-shiftlock/blob/main/SHOW.md) | [numpy/numpy](https://github.com/numpy/numpy) | empty `sum` is 0.0 | job profit 120 |
| [woodlock](https://github.com/shaneraphel/aletheia-woodlock/blob/main/SHOW.md) | [numpy/numpy](https://github.com/numpy/numpy) | empty `norm` is 0.0 | forest steps 6 |
| [taplock](https://github.com/shaneraphel/aletheia-taplock/blob/main/SHOW.md) | [numpy/numpy](https://github.com/numpy/numpy) | empty `sum` is 0.0 | garden taps 1 |
| [racelock](https://github.com/shaneraphel/aletheia-racelock/blob/main/SHOW.md) | [numpy/numpy](https://github.com/numpy/numpy) | empty `norm` is 0.0 | instructions 2 |
| [gaplock](https://github.com/shaneraphel/aletheia-gaplock/blob/main/SHOW.md) | [numpy/numpy](https://github.com/numpy/numpy) | empty `count_nonzero` is 0 | empty-slot day 2 |
| [jumplock](https://github.com/shaneraphel/aletheia-jumplock/blob/main/SHOW.md) | [networkx/networkx](https://github.com/networkx/networkx) | empty nodes is 0 | eight-stone cross |
| [sicklock](https://github.com/shaneraphel/aletheia-sicklock/blob/main/SHOW.md) | [numpy/numpy](https://github.com/numpy/numpy) | empty `sum` is 0.0 | infection orders 4 |
| [coinlock](https://github.com/shaneraphel/aletheia-coinlock/blob/main/SHOW.md) | [networkx/networkx](https://github.com/networkx/networkx) | empty nodes is 0 | coin path 1-3-5 |
