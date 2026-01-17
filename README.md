# Knowledge-Guided 3D CT Generation: A Conditioning-Centric Taxonomy

<div align="center">

![Taxonomy Overview](graphical_abstract.png)

[![Paper](https://img.shields.io/badge/Paper-arXiv-b31b1b.svg)](https://arxiv.org/abs/XXXX.XXXXX)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Classification Tool](https://img.shields.io/badge/GPT-Classifier-00A67E.svg)]([https://chat.openai.com/g/g-XXXXXXXXXX](https://chatgpt.com/g/g-696bce6c73e481a4a827e255a04cd691-3d-ct-generation-taxonomy-classifier))

*A comprehensive survey introducing the first conditioning-centric taxonomy for knowledge-guided 3D CT generation*

[📄 Read the Paper](#) • [🤖 Try Classification Tool](#classification-tool) • [📊 Explore Table 5](#comprehensive-method-overview) • [📖 Cite](#citation)

</div>

---

## 📌 Overview

This repository accompanies the survey paper:

> **Knowledge-Guided 3D CT Generation: A Conditioning-Centric Taxonomy**  
> Francesca Pia Panaccione, Eugenio Lomurno, Matteo Matteucci  
> *Politecnico di Milano, 2025*

We introduce the **first conditioning-centric taxonomy** for knowledge-guided 3D CT generation, organizing methods along three orthogonal axes:

- **Axis K**: External Knowledge type (Textual, Geometric, Exemplar, Attribute)
- **Axis I**: Knowledge Integration paradigm (Alignment, Model-Based, Inference-Time, Joint)
- **Axis A**: Generative Architecture (Single-Stage Latent, Cascaded, Autoregressive, Fixed-Transform)

This factorization defines an explicit **K × I × A design space** enabling systematic positioning and comparison of heterogeneous approaches.

---

## ✨ Key Features

- 🎯 **Conditioning-Centric Perspective**: First taxonomy organizing by *how* knowledge guides generation, not by architecture or domain
- 📊 **Comprehensive Analysis**: 25+ methods classified across 3 orthogonal dimensions
- 🔍 **Design Space Mapping**: Clear identification of dominant paradigms (K2, I2, A1) and underexplored regions
- 🤖 **Automated Classification Tool**: GPT-based classifier for instant method positioning
- 📈 **Quantitative Trends**: Statistical analysis revealing convergence patterns and research gaps
- 🌐 **Extensible Framework**: Accommodates hybrid approaches and future methods

---

## 🏗️ Taxonomy Structure

The taxonomy decomposes each method into a tuple `(k, i, a)` where:

### **Axis K: External Knowledge**

| Category | Description | Examples |
|----------|-------------|----------|
| **K1 - Textual** | Radiology reports, clinical descriptions | GenerateCT, Report2CT, Text2CT |
| **K2 - Geometric** | Segmentation masks, anatomical layouts | MAISI, LAND, MedLoRD |
| **K3 - Exemplar** | Cross-modal reference volumes (MRI→CT) | Med-LVDM, 3DLDM, cWDM |
| **K4 - Attribute** | Demographics, acquisition metadata | Cascaded-3D, Surf2CT |

### **Axis I: Knowledge Integration**

| Category | Description | Examples |
|----------|-------------|----------|
| **I1 - Alignment** | Pre-generative embedding alignment (CLIP) | GenerateCT, Text-to-CT |
| **I2 - Model-Based** | Direct architectural integration (cross-attention, ControlNet) | MAISI, Report2CT, DiffTumor |
| **I3 - Inference-Time** | Sampling-time guidance (CFG) | GenerateCT, Text2CT, TRACE |
| **I4 - Joint Modeling** | Co-generation p(x,k) | MedGen3D, MedSyn, LabelG |

### **Axis A: Generative Architecture**

| Category | Description | Examples |
|----------|-------------|----------|
| **A1 - Single-Stage Latent** | VQ-VAE/VAE one-shot synthesis | MAISI, LAND, DiffTumor |
| **A2 - Cascaded** | Multi-stage coarse→fine | GenerateCT, MedSyn, Cascaded-3D |
| **A3 - Autoregressive** | Slice-wise sequential generation | TRACE, CTFlow, MedGen3D |
| **A4 - Fixed-Transform** | Wavelet/spectral domain | cWDM, 3D-WLDM |

---

## 📊 Literature Trends

![Distribution Analysis](figures/figure2_distribution.png)

### Key Findings

- **Dominant Paradigm**: (K2, I2, A1) - Geometric conditioning with model-based integration in single-stage latent diffusion
  - Geometric knowledge: **44%** of methods
  - Model-based integration: **74%** of methods
  - Single-stage latent: **56%** of methods

- **Underexplored Regions**:
  - Demographic conditioning (K4): only **6%**
  - Pre-generative alignment (I1): only **6%** (confined to text)
  - Joint modeling (I4): only **10%**
  - Fixed-transform generation (A4): only **12%**

- **Cross-Dimensional Patterns**:
  - **K1 ↔ I3**: Textual conditioning pairs exclusively with inference-time guidance
  - **K2 ↔ I2**: Geometric masks rely on model-based integration
  - **K3 ↔ A4**: Exemplar knowledge clusters in fixed-transform domain

---

## 🤖 Classification Tool

We provide an **automated GPT-based classifier** to position new methods within the K×I×A design space.

### 🔗 **[Try the Classifier](https://chat.openai.com/g/g-XXXXXXXXXX)**

**How to use:**
1. Upload your paper (PDF format)
2. Press Enter
3. Get instant classification with:
   - Primary/Secondary categories for each axis
   - Confidence scores (High/Medium/Low)
   - Detailed rationales with evidence
   - Representative similar works
   - Position within design space

**Example Output:**
```
Primary Classification: (K2, I2, A1)
- K2: Geometric masks as voxel-aligned priors
- I2: Cross-attention injection in diffusion U-Net
- A1: VQ-VAE single-stage latent generation
Overall Confidence: High (87%)
```
---

## 📖 Citation

If you use this taxonomy or classification tool in your research, please cite:
```bibtex
@article{panaccione2025taxonomy,
  title={Knowledge-Guided 3D CT Generation: A Conditioning-Centric Taxonomy},
  author={Panaccione, Francesca Pia and Lomurno, Eugenio and Matteucci, Matteo},
  journal={arXiv preprint arXiv:XXXX.XXXXX},
  year={2025}
}
```

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

This work is supported by the FAIR (Future Artificial Intelligence Research) project, funded by the NextGenerationEU program within the PNRR-PE-AI scheme (M4C2, investment 1.3, line on Artificial Intelligence).

---

## 📬 Contact

For questions or collaboration:
- **Francesca Pia Panaccione**: francescapia.panaccione@polimi.it
- **Eugenio Lomurno**: eugenio.lomurno@polimi.it
- **Matteo Matteucci**: matteo.matteucci@polimi.it

---

<div align="center">

**[⬆ Back to Top](#knowledge-guided-3d-ct-generation-a-conditioning-centric-taxonomy)**

Made with ❤️ at Politecnico di Milano

</div>
