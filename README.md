Deblur
======

[![Build Status](https://travis-ci.org/biocore/deblur.png?branch=master)](https://travis-ci.org/biocore/deblur)
[![Coverage Status](https://coveralls.io/repos/github/biocore/deblur/badge.svg?branch=master)](https://coveralls.io/github/biocore/deblur?branch=master)

Deblur is a greedy deconvolution algorithm based on known read error profiles.

Code Development Note
=====================

Some of the code in the package deblur has been derived from [QIIME](http://qiime.org).
The contributors to these specific QIIME modules have granted permission
for this porting to take place and put under the BSD license.

Install
=======

At the moment, the install is a two stage process as we do not currently have deblur staged in a conda channel.

```
conda install -c bioconda VSEARCH MAFFT SortMeRNA==2.0 biom-format
pip install deblur
```


Example usage
=============

The input to deblur workflow is a demultiplexed FASTA or FASTQ file. The deblur 
algorithm is designed to work on individual samples.

```
deblur workflow --seqs-fp all_samples.fna --ref-fp db.fna --output-dir output
```
