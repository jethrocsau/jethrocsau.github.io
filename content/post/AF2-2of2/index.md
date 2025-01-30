---
title: AlphaFold2 for Cyclic Peptide Design - A Literature Review (2/2)
summary: Literature Review on the AF2 architecture and its use for cyclic peptide design
date: 2024-06-31
authors:
  - admin
tags:
  - AlphaFold
  - Drug-Discovery
  - Literature Review
image:
  caption: 'Cyclic Peptide generation architecture - Kosugi et. al.'
---

This is Part 2 of my literature review notes on AlphaFold2 for Cyclic Peptide Design. Refer to the 1st part in my blog if you haven't checked that one out yet!

This 2nd part of my review will be about recreation of the experimental structures of two successful implementations - one by Rettie et. al. and Kosugui et. al. Here are their papers for your reference:

(1) Rettie SA, Campbell KV, Bera AK, Kang A, Kozlov S, De La Cruz J, Adebomi V, Zhou G, DiMaio F, Ovchinnikov S, Bhardwaj G. Cyclic peptide structure prediction and design using AlphaFold. bioRxiv [Preprint]. 2023 Feb 26:2023.02.25.529956. doi: 10.1101/2023.02.25.529956. PMID: 36865323; PMCID: PMC9980166.

(2) Kosugi T, Ohue M. Design of Cyclic Peptides Targeting Protein-Protein Interactions Using AlphaFold. Int J Mol Sci. 2023 Aug 26;24(17):13257. doi: 10.3390/ijms241713257. PMID: 37686057; PMCID: PMC10487914.


# Recreation of paper results:

A critical part of the project involves recreating cyclic peptide structures using parameters derived from previous studies. The objective was to validate the implementation of my project, learn the tools required to generate cyclic peptides and reproduce the results to a certain accuracy.

As a high level overview, the recreation process was split into two parts:

1YCR Complex: Using ColabDesign, 50 structures of cyclic peptides were generated, benchmarked against known metrics. PyRosetta was used for energy scoring.

12PDB Structures: Cyclic peptides were generated for 11 out of 12 PDBs. Evaluation showed promising candidates, with most predicted structures binding in the expected positions.
