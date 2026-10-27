# Yahya Alsharif

**AI Engineer @ Mawhub** · **Software Engineering @ Umm Al-Qura University '27** · **Competitor @ WorldSkills Shanghai 2026**

I build software and applied AI systems with an emphasis on **reliable implementation, evaluation, testing, and deployment**: full-stack applications, AI/ML pipelines from data to quantised on-device models, backend integration, and automated testing. My work has ranged from privacy-preserving NLP on Raspberry Pi hardware to full-stack software engineering and international software-testing competition.

Currently, I work as an **AI Engineer at Mawhub**, where I take engineering work from requirements and technical decisions through implementation, testing, documentation, and integration.

[Portfolio](https://yahyaalsharif.github.io/personal-dashboard/) · [LinkedIn](https://www.linkedin.com/in/yahya-alsharif-204103304) · [Kaggle](https://www.kaggle.com/ghostylicious) · **yahya.alsharif567@gmail.com**

---

## Highlights

- **WorldSkills Shanghai 2026 — Software Testing:** represented Saudi Arabia after approximately four months of focused preparation across web, mobile, API, performance, and white-box testing.
- **KAUST Academy AI:** selected among the **top 100 students from 14,000+ applicants** and completed the AI Specialisation and eight-week summer internship.
- **OnKith:** developed the privacy-model track of a six-person team project, from early sequence-tagging baselines to an INT8 DeBERTa deployment evaluated on IID, OOD, hard-negative, and Raspberry Pi benchmarks.
- **Software engineering:** coordinated a six-person graduation project and worked across requirements, backend/frontend implementation, testing, documentation, and repository governance.

---

## Selected work

### [OnKith](https://github.com/YahyaAlsharif/OnKith) · privacy-preserving edge AI · team project
[Website](https://onkith.online/) · [Model evaluation notebooks](https://github.com/YahyaAlsharif/OnKith_Public) · [LinkedIn](https://www.linkedin.com/company/onkith/)

OnKith is a privacy-first local voice-processing system, built by a six-person KAUST Academy team, that removes personally identifying information before sensitive text leaves the device. I focused on the **privacy-model, data, evaluation, and deployment track**.

I helped evolve the privacy model from **BiLSTM → TinyBERT → DeBERTa-v3-xsmall**, built stronger leakage-aware data and evaluation protocols, and productionised the final model through **ONNX and INT8 quantisation**.

- **284,619** English rows and **2,088,335** labelled spans across **31 entity types**
- Frozen OOD typed F1 improved from **0.4649 → 0.6244**
- Private-character recall improved from **0.3209 → 0.8390**
- Hard-negative false-positive rate reduced from **0.6528 → 0.2361**
- Raspberry Pi 5 text benchmark: **0.9448 typed F1** at **62.4 ms median masking latency**

`PyTorch` `Transformers` `DeBERTa` `ONNX Runtime` `INT8` `Token Classification` `Raspberry Pi`

### ESAS · graduation project (private repository)

**Experience Saudi As a Saudi** is a backend-first tourism marketplace prototype for locally curated Saudi experiences. I coordinated the **six-person team**, owned the repository and major project documentation, reviewed contributions, and contributed to implementation across the system. The [portfolio](https://yahyaalsharif.github.io/personal-dashboard/#project-esas) has screenshots and the requirements specification.

The prototype uses **Java 21, Spring Boot, PostgreSQL, Flyway, Flutter, JWT-based security, REST APIs, and Docker**, with role-aware flows for **travelers, providers, and administrators**. Implemented areas include catalog browsing, authentication, cart and simulated checkout, booking flows, wishlist, provider onboarding/submission, and admin approval/moderation.

`Java` `Spring Boot` `PostgreSQL` `Flutter` `REST APIs` `Docker` `Software Engineering`

### [flappy_bird_challenge](https://github.com/YahyaAlsharif/flappy_bird_challenge) · reinforcement learning

Built a CPU-trained **Dueling Double DQN** with prioritised experience replay and stability-focused checkpoint selection. Diagnosed a major training collapse from evaluation history and rebuilt the target-update strategy using Polyak averaging.

Best episode: **5,120 pipes** · unseen five-seed holdout mean: **400**

`PyTorch` `Gymnasium` `NumPy`

---

## KAUST Academy challenges

| Repository | Task | Result |
|---|---|---|
| [kaust-cell-instance-segmentation](https://github.com/YahyaAlsharif/kaust-cell-instance-segmentation) | Neuronal-cell instance segmentation: ConvNeXt-Tiny U-Net, per-instance distance prediction, marker-controlled watershed | **3rd of 24 teams** (two-person team) · private 0.5472 · grouped-validation F1 0.8144 |
| [Kaggle_inpainting_comp](https://github.com/YahyaAlsharif/Kaggle_inpainting_comp) | MI-GAN reconstruction of 8,000 images with recovered masks, YuNet face filtering and gated checkpoint selection | **3rd place** · private FID 12.02 |
| [kaust-tajweed-audio-classification](https://github.com/YahyaAlsharif/kaust-tajweed-audio-classification) | 4-class Tajweed audio classification with ConvNeXt-Tiny on spectrograms with temporal features | **17th of 71 teams** · private macro-F1 0.9608 |
| [kaust-sensor-offset-fault-detection](https://github.com/YahyaAlsharif/kaust-sensor-offset-fault-detection) | Offset-fault detection in low-cost PM2.5 sensors with CatBoost and temporal-neighbour features | Write-up of a public/private leaderboard inversion |
| [edge_ai_project](https://github.com/YahyaAlsharif/edge_ai_project) | TinyML exercise: 1D-CNN IMU gesture recognition on a Seeed XIAO with TensorFlow Lite Micro | Coursework project |

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
**Software:** Spring Boot · PostgreSQL · React · Vite · Tailwind CSS · REST APIs · Docker · Git · GitHub  
**Testing:** Selenium · Appium · Postman · Newman · JMeter · pytest
