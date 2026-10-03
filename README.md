# Yahya Alsharif

**AI Engineer @ Mawhub** · **Software Engineering @ Umm Al-Qura University '27** · **Competitor @ WorldSkills Shanghai 2026**

I build software and applied AI systems with an emphasis on **reliable implementation, evaluation, testing, and deployment**. My work has ranged from privacy-preserving NLP on Raspberry Pi hardware to full-stack software engineering and international software-testing competition.

Currently, I work as an **AI Engineer at Mawhub**, where I take engineering work from requirements and technical decisions through implementation, testing, documentation, and integration.

---

## Highlights

- **WorldSkills Shanghai 2026 — Software Testing:** represented Saudi Arabia after approximately four months of focused preparation across web, mobile, API, performance, and white-box testing.
- **KAUST Academy AI:** selected among the **top 100 students from 14,000+ applicants** and completed the AI Specialisation and eight-week summer internship.
- **OnKith:** developed the privacy-model track from early sequence-tagging baselines to an INT8 DeBERTa deployment evaluated on IID, OOD, hard-negative, and Raspberry Pi benchmarks.
- **Software engineering:** coordinated a six-person graduation project and worked across requirements, backend/frontend implementation, testing, documentation, and repository governance.

---

## Selected work

### [OnKith](https://github.com/YahyaAlsharif/OnKith) · privacy-preserving edge AI
[Website](https://onkith.online/) · [LinkedIn](https://www.linkedin.com/company/onkith/)

OnKith is a privacy-first local voice-processing system designed to remove personally identifying information before sensitive text leaves the device. I focused on the **privacy-model, data, evaluation, and deployment track**.

I helped evolve the privacy model from **BiLSTM → TinyBERT → DeBERTa-v3-xsmall**, built stronger leakage-aware data and evaluation protocols, and productionised the final model through **ONNX and INT8 quantisation**.

- **284,619** English rows and **2,088,335** labelled spans across **31 entity types**
- Frozen OOD typed F1 improved from **0.4649 → 0.6244**
- Private-character recall improved from **0.3209 → 0.8390**
- Hard-negative false-positive rate reduced from **0.6528 → 0.2361**
- Raspberry Pi 5 text benchmark: **0.9448 typed F1** at **62.4 ms median masking latency**

`PyTorch` `Transformers` `DeBERTa` `ONNX Runtime` `INT8` `Token Classification` `Raspberry Pi`

### [ESAS](https://github.com/YahyaAlsharif/ESAS) · graduation project

**Experience Saudi As a Saudi** is a backend-first tourism marketplace prototype for locally curated Saudi experiences. I coordinated the **six-person team**, owned the repository and major project documentation, reviewed contributions, and contributed to implementation across the system.

The prototype uses **Java 21, Spring Boot, PostgreSQL, Flyway, Flutter, JWT-based security, REST APIs, and Docker**, with role-aware flows for **travelers, providers, and administrators**. Implemented areas include catalog browsing, authentication, cart and simulated checkout, booking flows, wishlist, provider onboarding/submission, and admin approval/moderation.

`Java` `Spring Boot` `PostgreSQL` `Flutter` `REST APIs` `Docker` `Software Engineering`

### [kaust-cell-instance-segmentation](https://github.com/YahyaAlsharif/kaust-cell-instance-segmentation) · computer vision

Placed **3rd of 24 teams** in a KAUST Academy cell-instance segmentation challenge. The final approach used a **ConvNeXt-Tiny U-Net**, continuous per-instance distance prediction, object-centric sampling, and marker-controlled watershed.

Final private leaderboard score: **0.5472** · grouped-validation F1: **0.8144**

`PyTorch` `ConvNeXt` `U-Net` `OpenCV` `Watershed`

### [Kaggle_inpainting_comp](https://github.com/YahyaAlsharif/Kaggle_inpainting_comp) · image inpainting

Built an MI-GAN reconstruction pipeline with test-matched dynamic masks, YuNet face filtering, fixed evaluation masks, and gated checkpoint selection.

Reconstructed all **8,000** test images and finished **3rd** with a private-leaderboard **FID of 12.02**.

`PyTorch` `MI-GAN` `OpenCV` `YuNet` `Clean-FID`

### [flappy_bird_challenge](https://github.com/YahyaAlsharif/flappy_bird_challenge) · reinforcement learning

Built a CPU-trained **Dueling Double DQN** with prioritised experience replay and stability-focused checkpoint selection. Diagnosed a major training collapse from evaluation history and rebuilt the target-update strategy using Polyak averaging.

Best episode: **5,120 pipes** · unseen five-seed holdout mean: **400**

`PyTorch` `Gymnasium` `NumPy`

---

## Testing

Competition preparation and hands-on work with:

`Selenium` `Appium` `Postman` `Newman` `JMeter` `pytest`

Across:

**Web testing · Mobile testing · API testing · Performance testing · Automated testing**

---

## Tech

**Languages:** Python · Java · TypeScript · HTML/CSS  
**AI / ML:** PyTorch · Hugging Face Transformers · ONNX Runtime · TensorFlow Lite · OpenCV · NumPy  
**Software:** React · Vite · Tailwind CSS · REST APIs · Docker · Git · GitHub  
**Testing:** Selenium · Appium · Postman · Newman · JMeter · pytest

---

## Elsewhere

[LinkedIn](https://www.linkedin.com/in/yahya-alsharif-204103304) · [Portfolio](https://yahyaalsharif.github.io/personal-dashboard/) · [Kaggle](https://www.kaggle.com/ghostylicious) · **yahya.alsharif567@gmail.com**
