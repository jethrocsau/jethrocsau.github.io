---
title: Insilico Medicine - Applying AI to Reduce Costs in Drug Discovery
summary: Generative Drug-Discovery using Adversarial Auto-Generative Encoders
date: 2023-09-25

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Insilico Medicine'

authors:
  - admin

tags:
  - Drug-Discovery
  - Research Blog
  - Markdown
  - Generative AI
---

Welcome 👋

{{< toc mobile_only=true is_open=true >}}

# Insilico Medicine: Applying AI to Reduce Costs in Drug Discovery

## Introduction

Conventional drug development has always been an uphill struggle. The American Society of Biochemistry and Molecular Biology reports that it **“takes 10 to 15 years and around US$1 billion to develop a successful drug”**, but despite these large investments in time and money, **“90% of drug candidates in clinical trials fail”**.

Amidst this pressing need to reduce costs, pioneering startups such as **Insilico Medicine** have been leveraging big data science to transform how drugs are developed. Based in Hong Kong, Insilico Medicine is a biotechnology AI startup that has developed an **“end-to-end” AI platform** capable of identifying a disease **“target”** and virtually generating suitable chemical molecules with therapeutic properties.

## Breakthrough in Cost and Time Efficiency

Insilico Medicine’s application of **deep generative networks** to drug discovery has exponentially reduced costs. Using their AI platform, Insilico developed a drug for Phase 1 trials targeting **fibrosis** in **18 months** at an estimated cost of **~USD 2.6 million**—just **10% of the cost** of conventional drug development.

---

## Data Overview

### ZINC Dataset
- **Source**: Open-sourced chemical dataset curated by John J. Irwin and Brian K. Shoichet.
- **Size**: Over **35 million compounds** aggregated from 10 vendor catalogs.
- **Format**: Originally stored as **2D Structured Data Files (SDF)**, converted to **SMILES representations** (ASCII strings describing chemical structures).  
  **Example**: Aspirin’s SMILES string: `O=C(C)Oc1ccccc1C(=O)O`  
  **Figure 1**: SMILES Representation of Aspirin.

### Data Cleaning & Validation
- Removed instances with:
  - Missing values
  - Inconsistent formatting
  - Duplicates
- Added critical attributes for biological relevance:
  - Molecular weight
  - Hydrogen-bond donors/acceptors
  - Rotatable bonds
  - XLogP (measure of lipophilicity)

### Filtering Criteria (MOSES Sub-dataset)
| Attribute                 | Filter Criteria                     |
|---------------------------|-------------------------------------|
| Molecular Weight          | 250–350 Daltons                    |
| XLogP                     | ≤3.5                               |
| Hydrogen-Bond Donors      | ≤6                                 |
| Hydrogen-Bond Acceptors   | ≤11                                |
| Rotatable Bonds           | ≤15                                |
| Permitted Atoms           | C, N, S, O, F, Cl, Br, H           |
| Excluded Features         | Charged atoms, atomic cycles >8    |
**Table 1**: Instance selection criteria for the MOSES dataset.  


**Figure 2**: MOSES dataset processed from ZINC.

### Dataset Partitioning
- **Training**: >80% (~1.6M molecules)
- **Test**: <10% (~176K molecules)
- **Test with New Scaffolds**: <10% (~176K molecules)  

**Figure 3**: Example of training data distribution.

---

## How Data is Leveraged

### Adversarial Autoencoders (AAE)
Insilico Medicine’s **GENTRL model** (Generative Tensorial Reinforcement Learning) uses a three-part AAE architecture:
1. **Encoder**: Recurrent neural network capturing statistical variances in training data.
2. **Latent Space**: 50-dimensional vector encoding molecule variations.
3. **Generator**: Produces novel SMILES strings representing molecules.

**Figure 4**: Architecture of Insilico Medicine’s GENTRL model.

### Training Process
- **Objective**: Reconstruct input SMILES strings.
- **Reward Functions**: 
  - Trending SOM
  - General Kinases SOM
  - Specific Kinase SOM
- **Optimization**: Adam optimizer with a learning rate of 0.0001 for 300K updates.

### Molecule Generation
- Generated **30,000 virtual molecules**.
- Filtered to **40 candidate molecules** based on chemical properties.

---

## Challenges

1. **Limited Data on Approved Drugs**:  
   AI models excel at generating compounds but struggle to predict FDA approval likelihood due to sparse data on successful drugs.

2. **Social & Cultural Barriers**:  
   - Opacity in AI-driven drug design complicates explanations to patients/doctors.  
   - Patient acceptance of AI-developed drugs remains untested.

---

## Conclusion

Insilico Medicine pioneers **AI-driven drug discovery**, demonstrating unprecedented cost and time savings. While challenges persist, their work signals a transformative shift in biotechnology.

---

## Sources
- <https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1360656/pdf/nihms2574.pdf>
- <https://insilico.com/blog/pcc>
- <https://github.com/insilicomedicine/GENTRL>
- <https://www.nature.com/articles/d43747-021-00039-5>
- <https://github.com/molecularsets/moses>
- <https://www.nature.com/articles/s41587-019-0224-x>
- <https://arxiv.org/abs/1811.12823>
- <https://insilico.com/phase1>
- <https://arxiv.org/pdf/1610.02415.pdf>