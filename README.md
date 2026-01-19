# Toward Generalizable Deblurring: Leveraging Massive Blur Priors with Linear Attention for Real-World Scenarios (GLOWDeblur)

**GLOWDeblur** is a **generalizable** and **lightweight** image deblurring framework designed for **real-world** blur, where many deep learning methods fail to generalize beyond their training distributions.

![Teaser / Overview](./images/banner_figure.png)

---

## Motivation

Although deep deblurring has advanced rapidly, most methods exhibit **poor cross-dataset generalization**, with significant performance drops on real captured blur.

Our analysis attributes this to:

- **Dataset trade-off**: realism vs. coverage of **diverse blur patterns**
- **Algorithmic bias**: pixel-wise losses emphasize local details but ignore **structural/semantic consistency**
- **Diffusion limitation**: strong perceptual quality yet still brittle when trained on narrow data distributions

**Key finding:** *Blur pattern diversity* is the decisive factor for robust real-world generalization.

---

## Method

### Blur Pattern Pretraining (BPP)

We propose **BPP**, which learns transferable **blur priors** from large-scale simulated blur data, then transfers them via **joint fine-tuning on real-captured datasets**.

### Motion & Semantic Guidance (MoSeG)

To improve robustness under severe degradation, **MoSeG** strengthens blur priors using:

- **Motion Guidance** (motion estimation / motion maps)
- **Semantic Guidance** (cross-modal text semantics)

### GLOWDeblur

![Overview of GLOWDeblur](./images/method.png)

GLOWDeblur combines:

- a **convolution-based pre-reconstruction & domain-alignment module**
- a **lightweight diffusion backbone** with **linear attention** for efficiency

---

## Qualitative Results

<details>
<summary><strong>▶ Click to expand qualitative comparisons</strong></summary>
<br>

**Qualitative comparison on real-world and challenging blur scenarios:**

![Qualitative comparison 1](./images/compare_1.png)
![Qualitative comparison 2](./images/compare_2.png)
![Qualitative comparison 3](./images/compare_3.png)
![Qualitative comparison 4](./images/compare_4.png)
![Qualitative comparison 5](./images/compare_5.png)
![Qualitative comparison 6](./images/compare_6.png)

</details>

---

## BibTeX

```bibtex
@article{gao2026toward,
  title={Toward Generalizable Deblurring: Leveraging Massive Blur Priors with Linear Attention for Real-World Scenarios},
  author={Gao, Yuanting and Cao, Shuo and Li, Xiaohui and Pu, Yuandong and Liu, Yihao and Zhang, Kai},
  journal={arXiv preprint arXiv:2601.06525},
  year={2026}
}
