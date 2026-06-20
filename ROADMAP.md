# ROADMAP.md — ConvertJason

## 12-Month Vision

Transform ConvertJason from a single-purpose Detectron2 converter into a **universal annotation format hub** supporting modern training frameworks (YOLO11, MMDetection, SAM2) with hardware-aware optimization for edge and cloud deployment.

---

## Quarterly Milestones

### Q1 (Months 1-3): Foundation & Modernization
- [ ] Implement core `convert.py` CLI with COCO → Detectron2 conversion
- [ ] Add LabelMe and VGG JSON parsers
- [ ] Python 3.10+ compatibility with type hints and `pathlib.Path`
- [ ] Unit test suite with pytest (target: 90% coverage)
- [ ] CI/CD pipeline (GitHub Actions)
- [ ] Package as pip-installable (`pip install convertjason`)

### Q2 (Months 4-6): Format Expansion
- [ ] Ultralytics YOLO11 format output (`.txt` with class/xywh)
- [ ] MMDetection format output (COCO-style with custom fields)
- [ ] CVAT XML export support
- [ ] Batch conversion mode (directory-level processing)
- [ ] Progress bars and structured logging

### Q3 (Months 7-9): Intelligence & Validation
- [ ] Annotation quality checker (area thresholds, overlap detection, class balance)
- [ ] Dataset statistics generator (class distribution, annotation density maps)
- [ ] SAM2 auto-annotation integration (grounding → mask → Detectron2 format)
- [ ] Roboflow API import/export connector
- [ ] Memory-efficient streaming for large datasets (>100K annotations)

### Q4 (Months 10-12): Performance & Ecosystem
- [ ] CUDA-accelerated format conversion for large datasets
- [ ] ONNX export readiness check (annotation format → ONNX-compatible dataset)
- [ ] Docker container for reproducible conversion environments
- [ ] Plugin API for community-contributed formats
- [ ] Web UI for annotation preview and conversion (optional)
- [ ] Performance benchmarks on M5 Max, Intel Ultra 9, NVIDIA Spark

---

## Technical Debt Items

| Priority | Item | Impact | Effort |
|----------|------|--------|--------|
| P0 | No `convert.py` implementation exists — README references it but source absent | Blocks all functionality | High |
| P1 | No test suite or CI/CD | No quality gates | Medium |
| P1 | No type hints or modern Python patterns | Code maintainability | Low |
| P2 | README references Python 3.8 — should target 3.10+ | Outdated compatibility claim | Low |
| P2 | No dependency management (requirements.txt / pyproject.toml) | Reproducibility | Medium |
| P3 | No error handling or logging framework | Debugging difficulty | Medium |
| P3 | No dataset preview/visualization | User experience | High |

---

## Future Features

### Near-Term (6 months)
- **Multi-threaded batch conversion** — Process thousands of annotation files in parallel
- **Incremental conversion** — Only re-convert changed annotations (delta updates)
- **Format migration guide** — Interactive CLI wizard for format selection
- **Annotation diff tool** — Compare two annotation sets and show discrepancies

### Mid-Term (12 months)
- **Auto-annotation pipeline** — SAM2 + Grounding DINO → ConvertJason → training format
- **Cloud storage integration** — Direct read/write to S3, GCS, Azure Blob
- **Web dashboard** — Visual annotation browser with conversion preview
- **Model training integration** — One-command convert → train → evaluate

### Long-Term (18+ months)
- **Federated annotation support** — Distributed annotation aggregation
- **Real-time annotation sync** — WebSocket-based live annotation streaming
- **Hardware-specific exporters** — Optimized dataset formats for edge devices (Raspberry Pi, Jetson)
- **Academic dataset zoo** — Pre-converted datasets for common benchmarks
