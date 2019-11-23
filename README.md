# bsdiff

This repository is a copy of the Chromium OS fork of [bsdiff][1], a binary
patch tool created by Colin Percival.

The Chromium team made a few changes for performance and correctness, the most
significant being the replacement of the suffix array construction algorithm.
There have been a number of improvements since qsufsort was introduced.
Bahne et al. (2019) benchmarked a number of algorithms and showed that
divsufsort is one of the fastest algorithms for constructing suffix arrays.

On this `master` branch, I've added this README and the program's license
license information. I've placed the unmodified Chromium sources retrieved
from `https://chromium.googlesource.com/chromiumos/third_party/bsdiff` on
the `original` branch.

Incidentally, I wrote a commit with a diff almost identical to that of
e2b85ce4ea246ca804ee2a9e18005c44e193d868 before I discovered that the Chromium
fork existed. Seeing that the Chromium team had independently come to the same
conclusion gave me a little more confidence that it was a good change.

## References

1. Bahne, Johannes, et al. "SACABench: Benchmarking Suffix Array Construction."
   International Symposium on String Processing and Information Retrieval.
   Springer, Cham, 2019.

[1]: https://www.daemonology.net/bsdiff/
