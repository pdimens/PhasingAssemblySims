---
site:
  hide_outline: true
edit_url: null
---

# Linked-Read Assembly and Phasing Performance Benchmarks
This repository and associated MyST-built website contains the code and work of the linked-read benchmark for phasing and assembly.

## Goals
Benchmark what linked-read library parameters most signficantly impact the performance of phasing SNPs into haplotypes and genome
assembly.

## Motivation
We are constantly developing and refining the haplotagging linked-read chemistry at the Genomics Innovation lab at Cornell. But,
beyond the basics (e.g. "does it work?", "is it cheap/accessible?"), we also really need to understand _where_ we should be
investing our experimenting and development. Linked-read libraries have an extra dimension of metrics that impact how well tools
leveraging it can perform. These characteristics include:
- reads per molecule
- molecules per barcode
- percent singletons
- duplication rate
- distance between reads with the same barcode 

What's more, it's also possible that different applications benefit from different optimizations. What if phasing performs better
with more reads per molecule (barcode), but assembly doesnt? What if barcode convolution (unrelated molecules sharing barcodes)
really messes with assembly but has minimal impact on phasing? In understanding these relationships, we can likely tune the chemistry
to maximize certain metrics tailored to specific applications. Then, everyone wins!

## What you'll find here
This project is being spearheaded by me (Pavel) with the help of Jacob Landis and Paul Mann. I will generate the simulated data
(recombination-aware genotypes for 10 offspring and their parents) and simulated linked-read data covering a spectrum of parameters
from those genotypes. Jacob is on the _Assembly Team_, using those linked reads to see the performance of linked-read-only assemblies,
and Paul is on the _Phasing Team_, investigating the phasing performance of those data (hence the parent-offspring genotypes with known
phases). As we work through this, the GitHub Pages site associated with this repository will be updated with our progress (in the form
of new pages with code, figures, tables, etc).
