# ConvertJason

[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?logo=python&logoColor=white)](https://python.org)
[![Detectron2](https://img.shields.io/badge/Detectron2-0.6-blue)](https://github.com/facebookresearch/detectron2)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Convert annotation files from JSON format to Detectron2-compatible format for training object detection and instance segmentation models.

## Overview

This utility converts standard JSON annotation files (e.g., COCO, LabelMe, VGG JSON) into the format required by Facebook's Detectron2 framework, streamlining the data preparation pipeline for training custom detectors.

## Supported Conversion Formats

| Source Format | Target Format | Use Case |
|--------------|---------------|----------|
| **COCO JSON** | Detectron2 | Instance segmentation, detection |
| **LabelMe JSON** | Detectron2 | Polygon annotations |
| **VGG JSON** | Detectron2 | Bounding box annotations |
| **Custom JSON** | Detectron2 | Project-specific formats |

## Modern Alternatives (2025-2026)

For new projects, consider these updated annotation and training pipelines:

### Training Frameworks

- **[Ultralytics YOLO11](https://github.com/ultralytics/ultralytics)** — Supports COCO, VOC, and custom formats natively with automatic conversion
- **[MMDetection](https://github.com/open-mmlab/mmdetection)** — Supports COCO, VOC, LVIS, and custom formats
- **[Detectron2](https://github.com/facebookresearch/detectron2)** — Still widely used, supports COCO format natively
- **[YOLO-World](https://github.com/AILab-CVC/YOLO-World)** — Open-vocabulary detection with text prompts

### Annotation Tools (2025-2026)

- **[Label Studio](https://labelstud.io/)** — Multi-format annotation platform with ML-assisted labeling
- **[Roboflow](https://roboflow.com/)** — End-to-end dataset management with automatic format conversion
- **[CVAT](https://cvat.ai/)** — Computer vision annotation tool with AI-assisted labeling
- **[FiftyOne](https://github.com/voxel51/fiftyone)** — Dataset analysis and visualization with model evaluation
- **[Segment Anything + SAM 2](https://github.com/facebookresearch/segment-anything-2)** — Promptable segmentation for fast annotation
- **[Grounding DINO + SAM](https://github.com/IDEA-Research/GroundingDINO)** — Open-set detection + segmentation for auto-annotation

### Data Augmentation for Detection

- **Albumentations** — 50+ transforms with bounding box support
- **Mosaic, MixUp, CutMix** — Built into YOLO training pipelines
- **Copy-Paste Augmentation** — Instance-level augmentation for segmentation

## Usage

```bash
python convert.py --input annotations.json --output detectron2_annotations.json
```

## References

- Wu, Y. et al. (2019). Detectron2: A PyTorch-based modular object detection library. *GitHub*.
- Kirillov, A. et al. (2023). Segment Anything. *ICCV*.
- Ren, S. et al. (2015). Faster R-CNN. *NeurIPS*.

## Author

**Dr. Farshid Pirahansiah** — [LinkedIn](https://linkedin.com/in/pirahansiah) | [GitHub](https://github.com/pirahansiah)
