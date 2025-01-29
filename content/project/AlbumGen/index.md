---
title: AlbumGen. Image-to-Music Generation with Textual Intermediaries
date: 2023-10-26
external_link: [repo](https://github.com/jethrocsau/AlbumGen-Multi-modality-LLM)
tags:
  - Multi-Modality
  - AlbumGen
  - LLM
---

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


https://github.com/user-attachments/assets/43c1b02c-495e-46ff-b63e-791a9f0dc464



<!--more-->
