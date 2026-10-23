# Deep-Space Image Restoration via Physics-Informed Conditional GAN (PI-cGAN)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-orange)
![Dataset](https://img.shields.io/badge/Dataset-NASA%20FITS-blueviolet)

# Honorable Mention, 25th Macronix Science Awards

## Abstract
This study proposes a solution to key challenges in deep learning-based deep-space image reconstruction—specifically "hallucination artifacts" and physical energy distortions caused by overfitting in extremely low signal-to-noise ratio (SNR) environments. While most existing vision-centric models can improve image resolution, they frequently generate unphysical spurious structures and violate flux conservation principles, thereby compromising the scientific fidelity of astronomical observations.

To address these limitations, this research introduces a Physics-Informed Conditional Generative Adversarial Network (PI-cGAN) that incorporates astrophysical domain priors. Built upon a cGAN backbone integrated with domain-specific physical loss functions, the framework utilizes publicly available NASA FITS astronomical imaging data to construct training sets and iteratively refines physical constraint strategies across multiple model versions. Evaluation and parameter tuning were conducted using metrics including PSNR, SSIM, Phase Consistency Error, and Linear Flux Error.

Experimental results demonstrate that, compared to a standard Basic cGAN, the proposed PI-cGAN effectively suppresses hallucination artifacts and reduces the average linear flux error from 214.66% to 4.65%. By balancing fine-detail recovery with physical consistency and scientific validity, this work delivers a viable deep-space image reconstruction approach with strong practical engineering potential.

## Repository Structure
.
├── Data dealing tool/
│   └── astro cGAN dataset dealing auto.ipynb
├── Model/
│   ├── PI-cGAN model I.ipynb
│   ├── PI-cGAN model II.ipynb
│   ├── PI-cGAN model III.ipynb
│   ├── PI-cGAN model IV.1.ipynb
│   ├── PI-cGAN model IV.ipynb
│   ├── PI-cGAN model V.ipynb
│   └── basic cGAN model.ipynb
├── docs/
│   ├── README.md
│   └── SA25-721_abstract.pdf
└── .gitignore
