# TTH

**This repository is the official implementation of the ECCV 2026 Workshop paper  "Test-Time Hallucination Control in Large Vision-Language Models" (TTH).**

> 🚧 **Code will be released soon.**




## 📌 Overview

Object hallucination in Large Vision-Language Models (LVLMs), where models generate non-factual content about input images, remains a critical barrier to their reliability in real-world applications.

Existing training-free methods still face important limitations:

- **Multiple decoding rounds:** Some approaches require repeated model decoding, introducing substantial computational overhead.
- **Model-specific modifications:** Other methods modify internal model states in a model-dependent manner, which can potentially interfere with or degrade the pretrained knowledge of LVLMs.

To address these limitations, we propose **TTH (Test-Time Hallucination Mitigation)**, a novel training-free method for controlling object hallucinations in LVLMs.

TTH introduces a **token-validator module**, implemented as a **zero-shot Multi-Modal Classifier (MMC)**, to generate auxiliary logits grounded in the input image. These auxiliary logits are fused with the original LVLM outputs at the token level for object tokens selected from a candidate pool. An **entropy-based weighting scheme** is further employed to adaptively combine the original and auxiliary predictions, enabling more robust and accurate token generation.

Extensive experiments across multiple LVLM families and diverse benchmarks demonstrate that TTH consistently improves hallucination-related accuracy and robustness, highlighting its **generality, effectiveness, and practical applicability**.

---

## 🔍 Method Overview

The overall framework of TTH is illustrated below.

<p align="center">
  <a href="https://github.com/Mehran-TAM/TTH/blob/main/Images/method.png">
    <img src="https://github.com/Mehran-TAM/TTH/blob/main/Images/method.png" alt="TTH Method Overview" width="100%">
  </a>
</p>


## 📈 Experiments

We extensively evaluate TTH across multiple Large Vision-Language Model families and hallucination benchmarks.

Our experiments demonstrate that TTH consistently improves object-level factuality and robustness while preserving the pretrained capabilities of the underlying LVLMs.

More details about the experimental setup, benchmarks, and quantitative results will be provided with the release of the code.

---



## 📚 Citation

If you find this work useful in your research, please consider citing our paper:

```bibtex
@inproceedings{tth2026,
  title     = {Test-Time Hallucination Control in Large Vision-Language Models},
  author    = {},
  booktitle = {},
  year      = {2026}
}
