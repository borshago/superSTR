# Installation:

## Requirements:

superSTR is tested and working on Debian/Ubuntu, RHEL/Centos, and on OSX. superSTR does not currently support Microsoft Windows.

Please make sure the following are installed and available on your system prior to installing superSTR:

* [htslib 1.9](https://github.com/samtools/htslib)
* [zlib](https://zlib.net/)
* Cmake (>3.10)
* curl and libcurl
* gcc
* git

## Installation steps:

1) Clone this repo to your machine using `git clone https://github.com/bahlolab/superSTR`.
2) Change into the superSTR directory with `cd superSTR`
3) On Unix/MacOS, set the the HTSLIB_ROOT environment variable with `export HTSLIB_ROOT=<path_to_your_htslib_installation>`
4) Change into the C source directory with `cd C`
5) Run `cmake . && make .`
6) Check that superSTR is correctly compiled by running `./superstr --help`; you should see:

```
Usage: superstr [-s] [--help] [--version] [--mode=<fastq|bam>] [-o myfile] <file> [<file>]...
Rapid STR characterisation in NGS data.
  --help                    display this help and exit
  --version                 display version info and exit
  --mode=<fastq|bam>        type of input data
  -s, --stream              run on named streams, not files (see manual for instructions)
  -o myfile                 output directory
  <file>                    input files (or names of pipes in stream mode)
```

If you run into issues with installation, check that you've correctly try deleting the cmake cache (at superSTR/CMakeCache.txt) and re-running the install process from step 5.

# Installation - Docker

#TODO: Docker