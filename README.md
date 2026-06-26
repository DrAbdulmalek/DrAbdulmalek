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

> **🚀 New here?** Start with [**omni-medical-suite**](https://github.com/DrAbdulmalek/omni-medical-suite) — it's the main platform that ties everything together.

### Ecosystem Map

```
                         OMNIMEDICAL SUITE ECOSYSTEM
    ══════════════════════════════════════════════════════════════

  ┌──────────────┐     ┌───────────────────┐     ┌──────────────┐
  │  scanner-    │────▶│  omni-medical-    │────▶│  medical-ocr-│
  │  fixer       │     │  suite            │     │  benchmarks  │
  │  Pre-OCR     │     │  Main Platform    │     │  Quality     │
  │  Normalizer  │     │  OCR+NLP+Web+API  │     │  Gates       │
  └──────────────┘     └────────┬──────────┘     └──────┬───────┘
                                │                       │
                       ┌────────▼──────────┐    ┌──────▼───────┐
                       │  medical-ocr-     │    │  medical-ocr-│
                       │  training-hub     │    │  trainer     │
                       │  Ingest + PII     │    │  Corrections │
                       │  Scrub + Validate │    │  + Ensemble  │
                       └────────┬──────────┘    └──────────────┘
                                │
                       ┌────────▼──────────┐
                       │  medical-ocr-     │
                       │  ground-truth     │
                       │  Verified Datasets│
                       └───────────────────┘

  ┌─────────────────────────────────────────────────────────────┐
  │  Hugging Face Spaces                                        │
  │                                                             │
  │  🏆 medical-handwriting-ocr  ─  Flagship Live Demo          │
  │  🔧 medical-ocr-trainer      ─  Correction Interface        │
  │  📊 mission-control          ─  MLOps Dashboard             │
  └─────────────────────────────────────────────────────────────┘
```

### Repositories (Recommended Reading Order)

| Step | Repository | Role |
|:----:|------------|------|
| 1 | [**omni-medical-suite**](https://github.com/DrAbdulmalek/omni-medical-suite) | Main platform — OCR, NLP, Web UI, API |
| 2 | [**scanner-fixer**](https://github.com/DrAbdulmalek/scanner-fixer) | Pre-OCR normalization — skew detection + auto-crop |
| 3 | [**medical-ocr-training-hub**](https://github.com/DrAbdulmalek/medical-ocr-training-hub) | Data ingestion, validation, hybrid PII scrubbing |
| 4 | [**medical-ocr-ground-truth**](https://github.com/DrAbdulmalek/medical-ocr-ground-truth) | Verified medical datasets (Single Source of Truth) |
| 5 | [**medical-ocr-trainer**](https://github.com/DrAbdulmalek/medical-ocr-trainer) | Human-in-the-loop correction + 5-engine ensemble |
| 6 | [**medical-ocr-benchmarks**](https://github.com/DrAbdulmalek/medical-ocr-benchmarks) | Quality gates — CER/WER thresholds, nightly regressions |

**Live Demos (Hugging Face):**

| Space | Role |
|-------|------|
| [🏆 Medical Handwriting OCR](https://huggingface.co/spaces/DrAbdulmalek/medical-handwriting-ocr) | **Flagship Demo** — try it now |
| [🔧 Medical OCR Trainer](https://huggingface.co/spaces/DrAbdulmalek/medical-ocr-trainer) | Specialized correction tool |
| [📊 Mission Control](https://huggingface.co/spaces/DrAbdulmalek/mission-control) | MLOps monitoring dashboard |

---

<details>
<summary><h3>🏗️ Architecture Highlights</h3></summary>

- **Self-Healing MLOps Loop**: Nightly benchmarks evaluate CER against thresholds (printed &lt; 5% / handwritten &lt; 12%). On failure, the pipeline auto-triggers retraining; on success, it auto-deploys to production — no human intervention needed.
- **Pre-OCR Normalization**: Scanner Fixer reduces CER by **40–50%** through dual-algorithm skew detection and intelligent auto-crop, acting as the critical first layer before any OCR engine runs.
- **Hybrid PII Scrubber**: A fast Regex layer catches structured patterns (phone, ID numbers), while a CamelBERT NER layer detects Arabic names — achieving zero false positives on medical dosages.
- **OCR Fusion V2**: 5-engine cascade with confidence-based routing and automatic fallback, ensuring no single point of failure in the recognition pipeline.
- **Vector Search**: Qdrant-powered semantic search over processed medical documents for rapid retrieval and cross-referencing.
- **Arabic NLP**: Context protector, grammatical error correction, and semantic deduplication tailored for Arabic medical terminology.

</details>

---

<details>
<summary><h3>📦 Tech Stack</h3></summary>

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

</details>

---

> **⚡ Note:** The projects below are **independent utilities** — not part of OmniMedical Suite.
>
> | Repository | Description |
> |------------|-------------|
> | [IntelliFile-app](https://github.com/DrAbdulmalek/IntelliFile-app) | AI-powered file classification for Manjaro Linux (Ollama + Next.js) |
> | [telegram-forwarder](https://github.com/DrAbdulmalek/telegram-forwarder) | Telegram content forwarder using Download-Upload technique (Telethon + Gradio) |

---

<div align="center">

**MIT License** · Built with precision by [DrAbdulmalek](https://github.com/DrAbdulmalek)

</div>