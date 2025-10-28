# Byte-Latent-Mamba
[IEEE TGRS] Byte Latent Mamba with State Space and Knowledge Distillation for Hyperspectral Image Classification

> Official implementation of **“Byte Latent Mamba with State Space and Knowledge Distillation for Hyperspectral Image Classification (HSIC)”**, accepted at **IEEE Transactions on Geoscience and Remote Sensing (TGRS)**.  
> BLM-KD removes explicit tokenization, learns **byte-level spectral–spatial representations**, integrates a **Selective State-Space Model (SSSM)** for long-range dependencies, and applies **adaptive knowledge distillation** for a compact, accurate student model.

---

<img width="1024" height="1024" alt="Comparitive" src="https://github.com/user-attachments/assets/bd359476-61c3-4a3f-9b01-d958b71bd6e8" />

<img width="4908" height="3108" alt="BLM-KD" src="https://github.com/user-attachments/assets/9e9886d1-2974-40a6-bfe8-92a53bbd398f" />

# Highlights

- **Byte Latent Representations (BLR):** Learns byte-level spectral–spatial encodings without tokenization.
- **Selective State-Space Modeling (SSSM):** Models long-range spectral and spatial dependencies.
- **Adaptive Knowledge Distillation (KD):** Teacher–student distillation with temperature and warm-up schedule.
- **Scalable Training Strategy:** Balances model complexity and performance.

---

## Method Overview

The BLM-KD pipeline integrates:
- Byte-level convolutional encoder  
- Selective State-Space Model (SSM)  
- Classification head with adaptive knowledge distillation  
- Loss function combining supervised and soft distillation terms:
  
\[
\mathcal{L}_{\text{total}}(t) = (1-\lambda_t)\,\mathcal{L}_{\text{class}} + \lambda_t\,\mathcal{L}_{\text{distill}}
\]

where \( \lambda_t \) increases linearly during training.


## Citation

If you use this work, please cite the original paper:

```bibtex
@article{Ahmad2025BLMKD,
  title   = {Byte Latent Mamba with State Space and Knowledge Distillation for Hyperspectral Image Classification},
  author  = {Muhammad Ahmad and Manuel Mazzara and Salvatore Distefano and Adil Mehmood Khan},
  journal = {IEEE Transactions on Geoscience and Remote Sensing},
  year    = {2025}
}
```

