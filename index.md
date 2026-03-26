---
title: "RADAR Challenge 2026"
layout: default
---

<style>
  /* Works with or without a theme wrapper like `.page-content`. */
  h2, .page-content h2 { text-align: center; }
  p, .page-content p { text-align: justify; text-justify: inter-word; }

  /* Keep organizer cards readable (not justified). */
  .organizers p, .page-content .organizers p { text-align: center; }
</style>


**Task**: Given a speech recording, classify it as real (bonafide) or fake (synthetic) under unknown media transformations.

<p style="text-align: center; margin: 2rem 0;">
  <img src="/assets/images/logo.png" alt="RADAR Challenge 2026 Logo" style="max-width: 512px; width: 100%; height: auto;">
</p>

## Robust Audio Deepfake Recognition under Media Transformations

The RADAR Challenge 2026 is an APSIPA Grand Challenge on robust audio deepfake detection under realistic media conditions. Participants must determine whether a speech recording is bonafide (real) or spoofed (synthetic) after it has undergone unknown media transformations such as codec compression, resampling, background noise, music mixing, and room effects.

While recent advances in speech synthesis and voice conversion have made synthetic speech increasingly realistic, most existing detection benchmarks evaluate systems using clean audio. In practice, however, audio shared through social media, messaging platforms, and online media rarely remains pristine. Instead, it is typically edited, compressed, resampled, or mixed with other sounds before reaching detection systems.

The RADAR Challenge addresses this gap by evaluating detection models under realistic media processing pipelines. By introducing diverse and partially unseen transformations, the challenge emphasizes robustness and generalization, which are critical for real-world deployment.

RADAR aims to establish a benchmark for media-robust audio deepfake detection and encourage the development of detection systems that remain reliable beyond controlled laboratory conditions.

## Venue

RADAR Challenge 2026 is organized as an [APSIPA Grand Challenge](https://www.apsipa2026.org/grand_challenges.html) and will be presented at **APSIPA ASC 2026 in Hanoi, Vietnam**.


## Quick Updates
- ...
- **2026-03-26** The languages of Evaluation data will be **English**, **Mandarin**, **Japanese**, and **Vietnamese**.
- **2026-03-25** Phase 1 started! Development data has been sent to registered participants via email. If you didn't received it or registered after this day, please contact organizers via email or Github Discussion.
- **2026-03-17** Registration form is ready
- **2026-03-16** Landing Page is UP! 🎉

---

## Registration
Please register your team using the registration form:

- [Register for RADAR Challenge 2026](https://forms.cloud.microsoft/r/ngGcR2zZJM)

Registration deadline: **April 13, 2026**. By registering, you agree to the [Terms & Conditions](/terms).

We welcome both academic and industry teams. Individual researchers are also encouraged to participate.

## Timeline
- **2026-03-15: Challenge announcement**
- **2026-03-25: Phase 1 Started: Development data released**
- ➤ **2026-04-10**: Phase 1 Ended: Development submission portal closes
- **2026-04-13**: Registration Deadline  
- **2026-04-15**: Phase 2 Started: Evaluation data released
- **2026-04-25**: Phase 2 Ended: Evaluation submission portal closes
- **2026-05-10**: Paper submission  
- **2026-06-01**: Notification of paper acceptance  
- **2026-06-15**: Camera-ready GC paper submission  
- **2026-11-09**: APSIPA conference presentation (Hanoi, Vietnam)



## Contact

For questions please use [GitHub Discussion](https://github.com/radar-challenge/radar-challenge.github.io/discussions) or via email (radarchallenge2026 (at) gmail.com)

We strongly encourage participants to use GitHub Discussions so answers benefit all teams.


---

## How to Get Started
1. **Read the rules of the challenge**.
2. **Prepare your data pipeline and models** using publicly available training datasets (respecting the training data policy).
3. **Download the development set** (to be released) once released and evaluate your systems under the provided transformations.
4. **Use the baseline system and inference script** (to be released) as a reference for data format and scoring.
5. **Submit your scores and system description** (to be added) according to the challenge instructions and deadlines.



## Task Summary

| Item | Description |
|------|-------------|
| Task | Binary classification (bonafide vs spoof) |
| Input | Speech waveform |
| Twist | Speech is passed through unknown media processing chains |
| Output | Spoof detection score |
| Metric | Equal Error Rate (EER) |
| Training data | Open (public datasets only) |
| Evaluation | Blind test set |
| Goal | Robust detection systems for realistic media processing |

---

## Dataset & Protocol

- **Development set**
  - English speech derived from [LlamaPartialSpoof](https://hieuthi.github.io/sample-LlamaPartialSpoof/) with additional media transformations applied. (Only the full-fake subset of LlamaPartialSpoof will be used)
  - Designed to help participants develop and test robustness to various signal degradations.

- **Evaluation set**
  - Multilingual speech data (English, Mandarin, Japanese, and Vietnamese) with unknown combinations of transformations.
  - No labels are provided; participants submit detection scores per utterance.

- **Training data policy**
  - No official training set is provided.
  - Participants may use any legally accessible public datasets (open/public license) for system development, except LlamaPartialSpoof, LibriTTS dev/test splits, and any derived or overlapping data, as these are used to construct the challenge development set.


## Phases
### Phase 1 - Development
- **2026-03-25 RADAR2026-dev set released** (English, no labels, derivative of LlamaPartialSpoof)
- 2026-04-01 Development submission portal opens
- 2026-04-10 Development submission portal closes  
- 2026-04-13 RADAR2026-dev labels released for analysis and paper writing

### Phase 2 - Evaluation
- 2025-04-15 RADAR2026-eval set released (multilingual)
- 2025-04-18 Evaluation submission portal opens
- 2025-04-25 Evaluation submission portal closes
- 2025-05-10 Paper Submission Deadline

## Media Transformations

Each utterance in the development and evaluation sets may undergo one or more of the following:

- **Signal level operations**
  - Peak level adjustment  
  - Fade-in / fade-out

- **Signal structure modifications**
  - Silence trimming  
  - Zero padding

- **Environmental conditions**
  - Additive environmental noise  
  - Background music  
  - Room impulse response (RIR) convolution

- **Media channel effects**
  - Audio codec compression  
  - Resampling  
  - Dynamic range compression  
  - Bandwidth limitation

Some transformations used in the evaluation set will not appear in the development set in order to explicitly evaluate model generalization. The number and combination of transformations applied to each utterance are randomly sampled to emulate diverse real-world media processing pipelines. Additional undisclosed transformations with similar characteristics may also be included in the evaluation set to further assess robustness to unseen conditions.

## Evaluation

- **Primary metric**: **Equal Error Rate (EER)** on the evaluation set.
- Participants must submit one detection score per evaluation utterance (higher scores ⇒ higher confidence that the sample is spoofed).
- Leaderboard rankings are based on EER, with additional metrics possibly reported for analysis.

## Baseline systems

We will release one or more baseline systems to help participants get started and to illustrate the expected data pipeline and submission format.

Organizers may also submit scores and description papers to guide the challenge. Any results submitted by organizers will be **excluded** from the final ranking.

## Awards

This is an academic challenge without monetary prizes.  

Top-performing teams will receive certificates, and outstanding submissions will be recognized at APSIPA 2026 in Hanoi, Vietnam.

---

## Organizers

<div class="organizers" style="display: flex; flex-wrap: wrap; gap: 1.5rem; justify-content: flex-start; align-items: flex-start;">

  <div style="max-width: 160px; text-align: center;">
    <img src="/assets/images/organizers/hieuthi-luong.jpg" alt="Dr. Hieu-Thi Luong" style="width: 100%; height: auto; border-radius: 8px; object-fit: cover;">
    <p><strong>Dr. Hieu-Thi Luong</strong><br>
    Fortemedia, Singapore<br>
    <em>Challenge Lead Organizer</em></p>
  </div>

  <div style="max-width: 160px; text-align: center;">
    <img src="/assets/images/organizers/xuechen-liu.jpg" alt="Asst. Prof. Xuechen Liu" style="width: 100%; height: auto; border-radius: 8px; object-fit: cover;">
    <p><strong>Asst. Prof. Xuechen Liu</strong><br>
    Xi'an Jiaotong-Liverpool University, China<br>
    <em>Co-organizer</em></p>
  </div>

  <div style="max-width: 160px; text-align: center;">
    <img src="/assets/images/organizers/ivan-kukanov.jpg" alt="Dr. Ivan Kukanov" style="width: 100%; height: auto; border-radius: 8px; object-fit: cover;">
    <p><strong>Dr. Ivan Kukanov</strong><br>
    KLASS Engineering &amp; Solutions, Singapore<br>
    <em>Co-organizer</em></p>
  </div>

  <div style="max-width: 160px; text-align: center;">
    <img src="/assets/images/organizers/kongaik-lee.jpg" alt="Assoc. Prof. Kong-Aik Lee" style="width: 100%; height: auto; border-radius: 8px; object-fit: cover;">
    <p><strong>Assoc. Prof. Kong-Aik Lee</strong><br>
    The Hong Kong Polytechnic University, Hong Kong SAR, China<br>
    <em>Advisor</em></p>
  </div>

</div>

---

## FAQs

### Q: Can we use pretrained models (e.g., SSL models) that may have been trained on datasets related to LibriTTS such as MLS?

Yes. Publicly available pretrained models are allowed, even if they were trained on large public speech datasets.

However, participants must not explicitly train or fine-tune models using LibriTTS dev/test splits or any derivatives of the RADAR development or evaluation data.


