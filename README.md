# Yahya Alsharif

Software Engineering at Umm Al-Qura University, class of 2027. Currently in the KAUST Academy AI Specialisation.

I build deep learning systems that have to run somewhere constrained: a microcontroller, a Raspberry Pi, a CPU-only training budget. Most of what I care about happens after the model works, in quantisation, evaluation design, and making a result reproducible rather than lucky.

---

## Selected work

### [OnKith_Public](https://github.com/YahyaAlsharif/OnKith_Public) · on-device PII masking
TinyBERT (4L-312D) token classifier that detects and masks personally identifying spans before text leaves the device. Trained on English rows of `ai4privacy/pii-masking-openpii-1.5m`, 147,366 train / 16,374 validation, with the official validation split of 40,908 rows held out entirely and never used for checkpoint selection.

| | Token micro-F1 | Entity F1 | Leakage | Size | Batch-1 latency |
|---|---|---|---|---|---|
| FP32 ONNX | 0.973 | 0.957 | 0.003 | 54.5 MB | 144 ms |
| INT8 ONNX | 0.970 | 0.950 | 0.003 | 13.7 MB | 130 ms |

4x smaller for 0.3 points of token F1. Packaged for Raspberry Pi 5 deployment downstream of speech-to-text.

`PyTorch` `Transformers` `ONNX Runtime` `seqeval`

### [Kaggle_inpainting_comp](https://github.com/YahyaAlsharif/Kaggle_inpainting_comp) · image inpainting, 3rd place
MI-GAN pipeline for 256x256 reconstruction with a custom rectangle-mask recovery step, YuNet face filtering, and test-matched dynamic masks. Three-epoch generator fine-tuning on perceptual, reconstruction, boundary and visible-region losses. All 8,000 test images reconstructed and validated, visible pixels preserved.

Final private leaderboard FID **12.02**, third place in the KAUST Academy competition. Pretrained and fine-tuned checkpoints were compared on fixed sanity masks, and the safer model was retained unless every evaluation gate passed.

Notebook: [mi-gan-inpainting-comp-03](https://www.kaggle.com/code/ghostylicious/mi-gan-inpainting-comp-03)

`PyTorch` `MI-GAN` `OpenCV` `YuNet` `Clean-FID` `LPIPS`

### [flappy_bird_challenge](https://github.com/YahyaAlsharif/flappy_bird_challenge) · deep RL
Dueling Double DQN with prioritised experience replay, 89k parameters, trained CPU-only from a 12-feature state vector. The first run was unstable, with mean score collapsing from 861 to 396 between checkpoints, diagnosed from its own evaluation history and rebuilt with Polyak averaging in place of hard target resyncs and exploration decay scaled to the training budget.

Checkpoints are ranked on worst-seed score before mean score, so a single lucky episode cannot win, and a one-time holdout runs on seeds never used for selection. Best single episode 5,120 pipes. Five-seed unseen holdout mean 400.

`PyTorch` `Gymnasium` `NumPy`

### [edge_ai_project](https://github.com/YahyaAlsharif/edge_ai_project) · TinyML gesture recognition
End-to-end pipeline on a XIAO board with an onboard 6-axis IMU. Captures accelerometer and gyroscope data, prepares 119x6 motion windows, trains a 1D CNN, converts to TensorFlow Lite, and runs inference on the microcontroller. Six gestures, reported over Serial and BLE.

`TensorFlow Lite` `Arduino` `Embedded C++`

### [ESAS](https://github.com/YahyaAlsharif/ESAS) · graduation project
Tourism platform presenting locally curated Saudi experiences. I coordinate the project: I own the documentation and the repository across a six-person team, author the SRS, drafts, reports and poster, and review contributions before they enter the repo.

### [personal-dashboard](https://github.com/YahyaAlsharif/personal-dashboard) · portfolio
Bilingual English and Arabic portfolio in React 19, TypeScript, Vite and Tailwind, with light and dark modes. [Live site](https://yahyaalsharif.github.io/personal-dashboard/)

---

## Tools

Python, PyTorch, Transformers, ONNX Runtime, TensorFlow Lite, NumPy, OpenCV, Gymnasium, TypeScript, React, Git

## Elsewhere

[LinkedIn](https://www.linkedin.com/in/yahya-alsharif-204103304) · [Kaggle](https://www.kaggle.com/ghostylicious) · [Portfolio](https://yahyaalsharif.github.io/personal-dashboard/) · yahya.alsharif567@gmail.com
