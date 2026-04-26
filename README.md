# 🎭 Mask2Former — Universal Segmentation Playground

A comprehensive Google Colab inference notebook for every pretrained **Mask2Former** checkpoint available on HuggingFace. Supports **Semantic**, **Panoptic**, and **Instance** segmentation across multiple benchmark datasets — all without writing a single line of code.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/YOUR_REPO/blob/main/Mask2Former_Comprehensive_Playground_.ipynb)

---

## ✨ Features

- 🔀 **All three segmentation tasks** — Semantic, Panoptic, and Instance
- 🗂️ **Four datasets** — ADE20K, Cityscapes, COCO, Mapillary Vistas
- 🧠 **Multiple backbones** — ResNet-50, ResNet-101, Swin-T, Swin-S, Swin-B, Swin-L (ImageNet-21k)
- 🎛️ **No-code model selection** — pick Dataset, Task & Backbone via Colab form dropdowns
- 🖼️ **Rich visualisation** — colour segmentation maps, alpha overlays, and side-by-side panels
- 📊 **Pixel statistics export** — per-class pixel counts & coverage exported to CSV / XLSX
- 📈 **Class distribution chart** — built-in bar chart of detected classes
- 💾 **Google Drive integration** — read images from Drive, save all outputs back automatically

---

## 🗂️ Supported Models

| Dataset | Semantic | Panoptic | Instance |
|---|---|---|---|
| ADE20K | ✅ | ✅ | ✅ |
| Cityscapes | ✅ | ✅ | ✅ |
| COCO | ❌ | ✅ | ✅ |
| Mapillary Vistas | ✅ | ✅ | ❌ |

All model weights are fetched automatically from the [facebook/](https://huggingface.co/facebook) organisation on HuggingFace Hub (~300–900 MB on first run).

---

## 🚀 Quick Start

1. Open the notebook in Google Colab (badge above).
2. Set the runtime to **GPU** — *High-RAM runtime recommended*.
3. Run the cells **in order**:

| Cell | Description |
|------|-------------|
| **Cell 1** | Install dependencies *(run once; restart runtime if prompted)* |
| **Cell 2** | Mount Google Drive |
| **Cell 3** | 🎛️ Select **Dataset, Task & Backbone** via form dropdowns |
| **Cell 4** | Configure input / output folder paths |
| **Cell 5** | Set inference & visualisation options (alpha, threshold, DPI, …) |
| **Cell 6** | Load model — auto-resolves the correct HuggingFace checkpoint |
| **Cell 7** | Run batch inference on all images in the input folder |
| **Cell 8** | Preview segmentation results inline |
| **Cell 9** | Export per-class pixel statistics to CSV / XLSX |
| **Cell 10** | Plot class distribution chart |

---

## ⚙️ Configuration Options

| Option | Default | Description |
|--------|---------|-------------|
| `OVERLAY_ALPHA` | `0.5` | Blend strength of the colour mask over the original image |
| `CONFIDENCE_THRESHOLD` | `0.65` | Minimum confidence for instance / panoptic segments |
| `MAX_SIZE` | `1024` | Longer-edge limit (px) before resizing — reduces GPU memory |
| `SAVE_SEGMAP` | `True` | Save colour segmentation map |
| `SAVE_OVERLAY` | `True` | Save blended overlay image |
| `SAVE_PANEL` | `True` | Save original + seg map + overlay side-by-side panel |
| `SAVE_STATS` | `True` | Export pixel-level class statistics |
| `PANEL_DPI` | `150` | DPI for saved panel images |

---

## 📦 Dependencies

All installed automatically in Cell 1:

- `transformers >= 4.39.0`
- `accelerate`
- `torch`, `torchvision`
- `Pillow`, `numpy`, `matplotlib`, `pandas`, `openpyxl`, `tqdm`

---

## 📚 References

- **Paper:** [Masked-attention Mask Transformer for Universal Image Segmentation (CVPR 2022)](https://arxiv.org/abs/2112.01527)
- **Model Zoo:** [github.com/facebookresearch/Mask2Former](https://github.com/facebookresearch/Mask2Former/blob/main/MODEL_ZOO.md)
- **HuggingFace Models:** [huggingface.co/facebook](https://huggingface.co/facebook)

---

## 👤 Author

The playground was developed by **Mohammad Raditia Pradana** — [aditpradana36.github.io](https://aditpradana36.github.io/)
