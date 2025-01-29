---
title: 'AlbumGen: Image-to-Music Generation with Textual Intermediaries'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - admin
  - Lai Chun Yu (HKUST)

# Author notes (optional)
author_notes:
  - 'Equal contribution'
  - 'Equal contribution'

date: '2024-11-25T00:00:00Z'
doi: ''

# Schedule page publish date (NOT publication's date).
publishDate: '2024-11-25T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ['report']

# Publication name and optional abbreviated publication name.
publication: AlbumGen - Image-to-Music Generation with Textual Intermediaries
publication_short:
abstract: This project explores the intersection of computer vision and music generation by utilizing image captioning models on album cover art and employing text-to-music generation models, such as MusicGen, to create music based on these captions. By training a model to generate descriptive captions from album covers, we aim to develop a system that automatically produces music aligned with the visual themes of album artwork. This innovative approach opens new avenues for creative AI-assisted music production.

# Summary. An optional shortened abstract.
summary: Image-to-Music Generation with Textual Intermediaries

tags:
  - Large Language Models
  - Multi-Modality

# Display this page in the Featured widget?
featured: true

url_pdf: ''
url_code: 'https://github.com/jethrocsau/6000N-Multi-modality-LLM'
url_dataset: 'https://marianaossilva.github.io/DSW2019/'
url_poster: ''
url_project: ''
url_slides: ''
url_source: 
url_video: 'https://github.com/user-attachments/assets/43c1b02c-495e-46ff-b63e-791a9f0dc464'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: 'AlbumGen'
  focal_point: ''
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: AlbumGen_Presentation
---
Full Text of [paper here](./paper.pdf).
Presentation of [AlbumGen with Demo here](./AlbumGen_Presentation.pdf).

AlbumGen explores generating music from album cover art using a multi-step pipeline that incorporates image captioning, text-to-music generation, and explainable intermediaries. The aim is to connect the visual themes of album art with music creation, leveraging advances in computer vision and large language models.

## **Key Components**

### 1. **Image-to-Text Conversion**
- Utilized **CLIP** (Contrastive Language-Image Pretraining) for image captioning.
- Album cover images were processed to generate 512-dimensional embeddings representing visual features such as color, textures, and symbols.

### 2. **Text-to-Music Generation**
- Used **Meta’s MusicGen** to create music based on descriptive captions generated from album art.
- A JSON format was adopted to represent acoustic features (e.g., valence, energy, danceability) for structured input to MusicGen.

### 3. **Dataset**
- Relied on the **MusicOSet Dataset**, containing metadata for 20,000+ songs, 26,000+ albums, and 11,000 artists.
- Metadata includes attributes like genres, popularity scores, acousticness, and danceability.

### 4. **Pipeline**
- Steps include image embedding, feature extraction, JSON-based acoustic feature generation, and music prompt generation.
- **LoRa (Low-Rank Adaptation)** finetuning was applied to improve the consistency of JSON outputs, using a small dataset.

### 5. **Evaluation**
- Consistency of textual intermediaries was measured using MSE (Mean Squared Error).
- Music compatibility was evaluated through visual/audio inspection and testing with different album covers.
- Human feedback-based reinforcement learning (RLHF) was proposed for future evaluation to assess musicality and context alignment.

---

## **Findings**
- The pipeline successfully produced music that aligned with album art in both zero-shot and few-shot scenarios.
- LoRa finetuning improved the consistency of JSON-based acoustic feature generation (75 valid JSON outputs vs. 21 without LoRa).
- Some limitations, such as hallucinated or mismatched music prompts, were observed.

<img width="764" alt="image" src="https://github.com/user-attachments/assets/012f71c7-fa00-4ca7-809f-34b8607b4c72" />


