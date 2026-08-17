# Yahya Alsharif

Software Engineering at Umm Al-Qura University, class of 2027. Currently in the KAUST Academy AI Specialisation.

I build deep learning systems that have to run somewhere constrained: a microcontroller, a Raspberry Pi, a CPU-only training budget. Most of what I care about happens after the model works, in quantisation, evaluation design, and making a result reproducible rather than lucky.

---

## Selected work

### [OnKith_Public](https://github.com/YahyaAlsharif/OnKith_Public) · local PII detection and masking
[Website](https://onkith.online/) · [LinkedIn](https://www.linkedin.com/company/onkith/)

OnKith is a privacy-first system that detects and masks personally identifying spans locally before sensitive text can leave the device. My work focuses on the PII models: data preparation and BIO alignment, model selection and training, evaluation, error analysis, ONNX export, INT8 quantisation, and deployment-oriented model comparison.

The model evolved deliberately from **BiLSTM → TinyBERT → DeBERTa-v3-xsmall**. The BiLSTM established the first sequence-tagging baseline at **0.605 binary token F1** under an older dataset/protocol. TinyBERT became the first production-oriented transformer, trading a small edge footprint for much stronger contextual detection. Once the pipeline showed enough compute and memory headroom, I moved to DeBERTa-v3-xsmall to improve masking quality rather than optimizing only for minimum model size.

| Model | Format | F1 | Leakage | Artifact size |
|---|---|---:|---:|---:|
| TinyBERT 4L-312D | FP32 ONNX | 0.957 | 0.003 | 54.5 MB |
| TinyBERT 4L-312D | INT8 ONNX | 0.9502 | 0.0029 | 13.72 MiB |
| DeBERTa-v3-xsmall | FP32 ONNX | 0.9610 | 0.0017 | ~270 MiB |
| DeBERTa-v3-xsmall | INT8 ONNX | **0.9588** | **0.0017** | 78.47 MiB |

The strongest direct comparison is the two INT8 deployment models on the **same 40,909-row held-out English validation split**: DeBERTa improves typed F1 from **0.9502 → 0.9588**, reduces leakage from **0.0029 → 0.0017**, reduces overmasking from **0.0044 → 0.0029**, and raises exact-row correctness from **0.7413 → 0.7844**. The cost is a 5.72× larger INT8 artifact and roughly 5.1× higher measured single-thread desktop latency.

The TinyBERT FP32 row comes from its historical standalone evaluation, so it should not be treated as an apples-to-apples comparison with Model V2. The direct TinyBERT-vs-DeBERTa claim above uses the shared INT8 evaluation protocol.

`PyTorch` `Transformers` `ONNX Runtime` `Token Classification` `Privacy Evaluation`

### [kaust-cell-instance-segmentation](https://github.com/YahyaAlsharif/kaust-cell-instance-segmentation) · cell instance segmentation, 3rd place
**3rd of 24 teams** on the final private leaderboard of KAUST Academy Summer School 2026 Challenge 2, detecting and segmenting individual neuronal cells in dense fluorescence microscopy images.

The solution evolved across 15 measured stages: from a Mask R-CNN baseline to a **ConvNeXt-Tiny U-Net** that predicts foreground, seed structure, and a continuous per-instance distance field, then recovers instances with marker-controlled watershed. The largest late gain came from **object-centric zoom-in sampling** and fixing the target formulation rather than adding a larger model or ensemble.

Final team private leaderboard score: **0.5472**. The final single-model Stage 15 run reached **0.5463 private / 0.5345 public**, with **0.8144 grouped-validation F1**, and ran end to end in about 26 minutes on one T4.

Notebook: [3rd-place-object-centric-convnext-unet-distance](https://www.kaggle.com/code/ghostylicious/3rd-place-object-centric-convnext-unet-distance)

`PyTorch` `ConvNeXt` `U-Net` `Watershed` `OpenCV` `timm`

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
