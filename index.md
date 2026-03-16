---
title: "RADAR Challenge 2026"
layout: default
---


**Task**: Given a speech recording, predict whether it is bonafide or spoofed after unknown media transformations.

## Robust Audio Deepfake Recognition under Media Transformations

The RADAR Challenge 2026 is an APSIPA Grand Challenge on robust audio deepfake detection in realistic media conditions. Participants must determine whether a speech recording is bonafide (real) or spoofed (synthetic) after unknown media transformations such as codec compression, resampling, noise, background music, and room effects.

This challenge aims to drive research on generalization under real-world signal degradations and establish a benchmark for media-robust audio deepfake detection.

RADAR is the first challenge specifically designed to evaluate robustness of audio deepfake detection under realistic media processing pipelines.


## Venue

RADAR Challenge 2026 is organized as an [APSIPA Grand Challenge](https://www.apsipa2026.org/grand_challenges.html) and will be presented at APSIPA ASC 2026 in Hanoi, Vietnam.


## Quick Updates
- 2026-03-16 Landing Page is UP! 🎉

---

## Registration
Please register your team using the registration form:

- [Register for RADAR Challenge 2026 (to be added)]()

Registration deadline: April 10, 2026

We welcome both academic and industry teams. Individual researchers are also encouraged to participate.

---

## Timeline
- **2026-03-15**: ~~Challenge announcement~~
- ➤ **2026-03-25**: Development data release  
- **2026-04-15**: Evaluation data release  
- **2026-04-25**: Result submission deadline  
- **2026-05-10**: Paper submission  
- **2026-06-01**: Notification of paper acceptance  
- **2026-06-15**: Camera-ready GC paper submission  
- **2026-11-09**: APSIPA conference presentation (Hanoi, Vietnam)

---

## How to Get Started
1. **Read the rules of the challenge**.
2. **Prepare your data pipeline and models** using publicly available training datasets (respecting the training data policy).
3. **Download the development set** (to be released) once released and evaluate your systems under the provided transformations.
4. **Use the baseline system and inference script** (to be released) as a reference for data format and scoring.
5. **Submit your scores and system description** according to the challenge instructions and deadlines.

---

## Contact

For questions please usse [GitHub Discussion](https://github.com/radar-challenge/radar-challenge.github.io/discussions)

We strongly encourage participants to use GitHub Discussions so answers benefit all teams.

---

## Task Summary

| Item | Description |
|------|-------------|
| Task | Binary classification (bonafide vs spoof) |
| Input | Speech waveform |
| Twist | Speech are passed through unknown media processing chains |
| Output | Spoof detection score |
| Metric | Equal Error Rate (EER) |
| Training data | Open (public datasets only) |
| Evaluation | Blind test set |
| Goal | Robust dectection systems for realistic media processing |

---

## Dataset & Protocol

- **Development set**
  - English speech derived from **LlamaPartialSpoof** with additional media transformations applied.
  - Designed to help participants develop and test robustness to various signal degradations.

- **Evaluation set**
  - Multi-language speech (including English) with unknown combinations of transformations.
  - No labels are provided; participants submit detection scores per utterance.

- **Training data policy**
  - No official training set is provided.
  - Participants may use **any publicly available datasets** (respecting licenses) that are accessible to all.
  - Use of LlamaPartialSpoof and LibriTTS (dev/test sets and derivatives) is not allowed, as they are used to build the development set.

---

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

Some transformations in the evaluation set** will not appear in the development set, explicitly testing generalization. The number and combination of transformations per utterance is randomly sampled to emulate diverse real-world pipelines.

---

## Evaluation

- **Primary metric**: **Equal Error Rate (EER)** on the evaluation set.
- Participants must submit one detection score per evaluation utterance (higher scores ⇒ higher confidence that the sample is spoofed).
- Leaderboard rankings are based on EER, with additional metrics possibly reported for analysis.

---

## Awards

This is an academic challenge without monetary prizes.  
Top-performing teams will receive certificates, and outstanding submissions will be recognized at APSIPA 2026 in Hanoi, Vietnam.

---

## Organizers

<div style="display: flex; flex-wrap: wrap; gap: 1.5rem; justify-content: flex-start; align-items: flex-start;">

  <div style="max-width: 180px; text-align: center;">
    <img src="/assets/images/organizers/hieuthi-luong.jpg" alt="Dr. Hieu-Thi Luong" style="width: 100%; max-width: 150px; border-radius: 8px; object-fit: cover;">
    <p><strong>Dr. Hieu-Thi Luong</strong><br>
    Fortemedia, Singapore<br>
    <em>Challenge Lead Organizer</em><br>
    <a href="mailto:hieuthiluong@fortemedia.com">hieuthiluong@fortemedia.com</a></p>
  </div>

  <div style="max-width: 180px; text-align: center;">
    <img src="/assets/images/organizers/xuechen-liu.jpg" alt="Asst. Prof. Xuechen Liu" style="width: 100%; max-width: 150px; border-radius: 8px; object-fit: cover;">
    <p><strong>Asst. Prof. Xuechen Liu</strong><br>
    Xi'an Jiaotong-Liverpool University, China<br>
    <em>Co-organizer</em></p>
  </div>

  <div style="max-width: 180px; text-align: center;">
    <img src="/assets/images/organizers/ivan-kukanov.jpg" alt="Dr. Ivan Kukanov" style="width: 100%; max-width: 150px; border-radius: 8px; object-fit: cover;">
    <p><strong>Dr. Ivan Kukanov</strong><br>
    KLASS Engineering &amp; Solutions, Singapore<br>
    <em>Co-organizer</em></p>
  </div>

  <div style="max-width: 180px; text-align: center;">
    <img src="/assets/images/organizers/kongaik-lee.jpg" alt="Assoc. Prof. Kong-Aik Lee" style="width: 100%; max-width: 150px; border-radius: 8px; object-fit: cover;">
    <p><strong>Assoc. Prof. Kong-Aik Lee</strong><br>
    The Hong Kong Polytechnic University, Hong Kong SAR, China<br>
    <em>Advisor</em></p>
  </div>

</div>

---




