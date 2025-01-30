---
title: 'Precision Generation of Cyclic Peptides using AlphaFold'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - admin

# Author notes (optional)
author_notes:

date: '2024-11-25T00:00:00Z'
doi: ''

# Schedule page publish date (NOT publication's date).
publishDate: '2024-11-25T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ['report']

# Publication name and optional abbreviated publication name.
publication: Precision Generation of Cyclic Peptides using AlphaFold
publication_short:
abstract: This independent research study conducted a series of investigations to enhance the precision of cyclic peptide generation targeting the HIV gp120 trimer. The methods included proximity mapping to focus on the CD4 binding site, centroid distance penalization, generative loss tuning, and the development of custom generative functions. By synthesizing these findings, a novel methodology was implemented to generate candidate cyclic peptides of varying lengths. This process successfully produced cyclic peptides that resemble the crystal structure of CD4 attachment inhibitor (BMS-818251 molecule). This new methodology demonstrated improved control and precision in the generation of compounds, thereby enhancing the applicability of AlphaFold in the drug discovery process.

# Summary. An optional shortened abstract.
summary: Precision Generation of Cyclic Peptides using AlphaFold

tags:
  - AlphaFold
  - HIV
  - De-Novo Design
  - Drug-Discovery

# Display this page in the Featured widget?
featured: true

url_pdf: ''
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: 
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: 'AlphaFold2'
  focal_point: ''
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: 'af-peptide'

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: []
---
(In Progress)

Recent advancements in artificial intelligence have spurred scientific breakthroughs, particularly in drug discovery and protein engineering. Most notably, in 2024, the Nobel Prize in Chemistry was awarded to David Baker, Demis Hassabis, and John Jumper for their work in developing AlphaFold, a protein folding prediction model developed by DeepMind. Ever since AlphaFold2 demonstrated highly accurate protein structure predictions in the 14th Critical Assessment of Protein Structure Prediction - CASP14 - (Jumper et al.), the model has accelerated biological engineering in all facets of applications, ranging from drug discovery to developing novel polymers. Despite the research interest, explorations in adapting AlphaFold for cyclic peptide targeting HIV’s gp120 trimer have not been explored rigorously. 

During the summer term project, an independent study was conducted to configure the AlphaFold network to generate cyclic peptides for various protein structures. In this previous study, the network successfully generated cyclic peptides targeting short-protein sequences with low RMSD values and comparable to literature generations. However, when the same network was applied to the larger gp120 trimer, the previous model exhibited high variability in the binding region, produced low-confidence or infeasible structures, and was largely unoptimized in the generation process (Figure 1). In response, a further research project was initiated to improve the precision of AlphaFold’s generative capabilities and its ability to target the HIV gp120 trimer. 