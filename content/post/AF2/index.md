---
title: AlphaFold2 for Cyclic Peptide Design - A Literature Review
summary: Literature Review on the AF2 architecture and its use for cyclic peptide design
date: 2024-01-31
authors:
  - admin
tags:
  - AlphaFold
  - Drug-Discovery
  - Literature Review
image:
  caption: 'Cyclic Peptide generation architecture (Kosugi et. al.)'
---

As part of my learning journey on the use of AI for drug-discovery, I've documented my literature review of AlphaFold2 architecture, a review of its open-source implementation, and notes on how cyclic peptides can be designed by other researchers.

Research articles referenced in this blog post:
- Jumper, J., Evans, R., Pritzel, A., Green, T., Figurnov, M., Ronneberger, O., Tunyasuvunakool, K., Bates, R., Žídek, A., Potapenko, A., Bridgland, A., Meyer, C., Kohl, S. A. A., Ballard, A. J., Cowie, A., Romera-Paredes, B., Nikolov, S., Jain, R., Adler, J., Back, T., Petersen, S., Reiman, D., Clancy, E., Zielinski, M., Steinegger, M., Pacholska, M., Berghammer, T., Bodenstein, S., Silver, D., Vinyals, O., Senior, A. W., Kavukcuoglu, K., Kohli, P., & Hassabis, D. (2021). Highly accurate protein structure prediction with AlphaFold. Nature, 596(7873), 583–589. https://doi.org/10.1038/s41586-021-03819-2

- Jumper, J., Evans, R., Pritzel, A., Green, T., Figurnov, M., Ronneberger, O., Tunyasuvunakool, K., Bates, R., Žídek, A., Potapenko, A., Bridgland, A., Meyer, C., Kohl, S. A. A., Ballard, A. J., Cowie, A., Romera-Paredes, B., Nikolov, S., Jain, R., Silver, D., ... & Hassabis, D. (2021). Supplementary information, highly accurate protein structure prediction with AlphaFold. Nature. https://doi.org/10.1038/s41586-021-03819-2


- Rettie, S. A., Campbell, K. V., Bera, A. K., Kang, A., Kozlov, S., De La Cruz, J., Adebomi, V., Zhou, G., DiMaio, F., Ovchinnikov, S., & Bhardwaj, G. (n.d.). Cyclic peptide structure prediction and design using AlphaFold. University of Washington and Harvard University.


- Takatsugu Kosugi and Masahito Ohue, Design of Cyclic Peptides Targeting Protein–Protein Interactions Using AlphaFold. 


# Introduction
Predicting structural proteins is critical to the understanding of biology, developing novel therapeutics and innovating new compounds. In the past, these structures have been determined by experiments, but have not been able to cover the billions of known protein sequences. Google’s Deepmind’s AlphaFold offers a groundbreaking model that can accurately predict the protein structures close to experimental values in-silico, and has been a game-changer in the field of peptide design.

Researchers have recently adapted AlphaFold models to achieve designing of cyclic peptides. This project explored the use of AlphaFold and supporting bioinformatic tools to design cyclic-peptides, and is done so in three sections.

# AlphaFold Architecture
