<div align="center">

# Dr. Abdulmalek Tamer Al-Husseini

**Building intelligent systems for Arabic medical document processing**

[![GitHub](https://img.shields.io/badge/GitHub-DrAbdulmalek-181717?style=for-the-badge&logo=github)](https://github.com/DrAbdulmalek)
[![Hugging Face](https://img.shields.io/badge/HuggingFace-DrAbdulmalek-FFAA00?style=for-the-badge&logo=huggingface)](https://huggingface.co/DrAbdulmalek)
[![MIT License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](https://opensource.org/licenses/MIT)

</div>

---

## 🏥 OmniMedical Suite — Medical OCR Ecosystem

An end-to-end, self-healing platform for Arabic and multilingual medical document intelligence. From scanned prescriptions to structured data — with automated quality gates and continuous learning.

### Start Here

```
┌─────────────────────────────────────────────────────────────────┐
│                    OMNIMEDICAL SUITE ECOSYSTEM                   │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  ┌──────────────┐    ┌──────────────────┐    ┌───────────────┐ │
│  │  🔧 scanner-  │───▶│  ⭐ omni-medical  │───▶│  📊 medical-  │ │
│  │   fixer      │    │   -suite         │    │   ocr-bench-  │ │
│  │  Pre-OCR     │    │  Main Platform   │    │   marks       │ │
│  │  Normalizer  │    │  OCR+NLP+Web+API │    │  Quality Gates│ │
│  └──────────────┘    └────────┬─────────┘    └───────────────┘ │
│                               │                                 │
│  ┌──────────────┐    ┌───────▼──────────┐    ┌───────────────┐ │
│  │  📊 medical-  │    │  🔄 medical-ocr- │    │  ✏️ medical-  │ │
│  │   ocr-       │◀──│   training-hub   │◀──│   ocr-trainer │ │
│  │   ground-    │    │  Ingest+Validate │    │  Corrections  │ │
│  │   truth      │    │  +PII Scrub      │    │  +Ensemble    │ │
│  └──────────────┘    └──────────────────┘    └───────────────┘ │
│                                                                 │
│  ┌────────────────────────────────────────────────────────────┐ │
│  │  🤗 Hugging Face Spaces                                    │ │
│  │  [Medical Handwriting OCR] — Flagship Live Demo            │ │
│  │  [Medical OCR Trainer]      — Correction Interface         │ │
│  │  [Mission Control]          — MLOps Dashboard              │ │
│  └────────────────────────────────────────────────────────────┘ │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

| # | Repository | Role |
|:-:|------------|------|
| ⭐ | [**omni-medical-suite**](https://github.com/DrAbdulmalek/omni-medical-suite) | Main platform — OCR, NLP, Web UI, API (Next.js + FastAPI + Qdrant) |
| 🔧 | [**scanner-fixer**](https://github.com/DrAbdulmalek/scanner-fixer) | Pre-OCR normalization — dual-algorithm skew detection + auto-crop |
| 📊 | [**medical-ocr-ground-truth**](https://github.com/DrAbdulmalek/medical-ocr-ground-truth) | Single Source of Truth for verified medical datasets |
| 🔄 | [**medical-ocr-training-hub**](https://github.com/DrAbdulmalek/medical-ocr-training-hub) | Data ingestion, validation, hybrid PII scrubbing (Regex + CamelBERT NER) |
| ✏️ | [**medical-ocr-trainer**](https://github.com/DrAbdulmalek/medical-ocr-trainer) | Human-in-the-loop correction + 5-engine ensemble collection |
| 📏 | [**medical-ocr-benchmarks**](https://github.com/DrAbdulmalek/medical-ocr-benchmarks) | Quality gates — CER/WER thresholds, A/B testing, nightly regressions |

**Live Demos (Hugging Face):**

| Space | Role |
|-------|------|
| [🤗 Medical Handwriting OCR](https://huggingface.co/spaces/DrAbdulmalek/medical-handwriting-ocr) | **Flagship Demo** — try it now |
| [🤗 Medical OCR Trainer](https://huggingface.co/spaces/DrAbdulmalek/medical-ocr-trainer) | Specialized correction tool |
| [🤗 Mission Control](https://huggingface.co/spaces/DrAbdulmalek/mission-control) | MLOps monitoring dashboard |

---

## 💡 Independent Side Projects

Not related to medical OCR — standalone utilities:

| Repository | Description |
|------------|-------------|
| [IntelliFile-app](https://github.com/DrAbdulmalek/IntelliFile-app) | AI-powered file classification for Manjaro Linux (Ollama + Next.js) |
| [telegram-forwarder](https://github.com/DrAbdulmalek/telegram-forwarder) | Telegram content forwarder using Download-Upload technique (Telethon + Gradio) |

---

## 🏗️ Architecture Highlights

- **Self-Healing MLOps**: Nightly benchmarks → threshold check (CER < 5% printed / < 12% handwritten) → auto-deploy or auto-retrain
- **Hybrid PII Scrubber**: Fast Regex layer + CamelBERT NER for Arabic name detection — zero false positives on medical dosages
- **OCR Fusion V2**: 5-engine cascade with confidence-based routing and automatic fallback
- **Pre-OCR Normalization**: Scanner Fixer reduces CER by 40-50% through skew detection and intelligent auto-crop
- **Vector Search**: Qdrant-powered semantic search over processed medical documents
- **Arabic NLP**: Context protector, grammatical error correction, and semantic deduplication

---

## 📦 Tech Stack

<p>
  <img src="https://img.shields.io/badge/Python-3.10+-3776AB?style=flat-square&logo=python" />
  <img src="https://img.shields.io/badge/Next.js-16-000000?style=flat-square&logo=next.js" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi" />
  <img src="https://img.shields.io/badge/React_19-61DAFB?style=flat-square&logo=react" />
  <img src="https://img.shields.io/badge/Qdrant-DC2F5C?style=flat-square" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker" />
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv" />
  <img src="https://img.shields.io/badge/Turborepo-F97316?style=flat-square" />
</p>

---

<div align="center">

**MIT License** · Built with precision by [DrAbdulmalek](https://github.com/DrAbdulmalek)

</div>