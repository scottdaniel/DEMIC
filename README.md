# DEMIC

<!-- badges: start -->
  [![Codecov test coverage](https://codecov.io/gh/Ulthran/DEMIC/branch/master/graph/badge.svg)](https://app.codecov.io/gh/Ulthran/DEMIC?branch=master)
<!-- badges: end -->

DEMIC PTR analysis software in the form of an R package

Main steps:
1. Check and record parameters designated by user
2. Record GC content in sliding windows for contigs
	key subroutine:
	&GC_count
3. Distribute SAM files to threads and calculate coverages in sliding windows
	key subroutine:
	&sam_cov_parallel
4. Convert COV2 (coverage in samples) to COV3 (coverage in contig clusters)
5. Distribute COV3 files to threads and invoke R to estimate growth rates
	key subroutine:
	&cov3_estPTR_parallel
6. Output
