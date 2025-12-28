# translator-kea

Translator focused on Cape Verdean Creole (Kabuverdianu, ISO: kea), with support for all languages via LibreTranslate when available.

Features
- Primary focus: Kabuverdianu (kea). When target not specified, kea is used by default.
- Demo web UI (static) + FastAPI backend.
- Integrates with LibreTranslate (if reachable). Fallback: a small rule-based PT -> KEA mapper as a quick demo.
- Training scaffolding to fine-tune Hugging Face models (mBART / mT5).
- Docker + docker-compose to run API and optional LibreTranslate container.
- CI: basic linting workflow.

Quick start (dev)
1. Copy `.env.example` to `.env` and edit if needed.
2. Build & run:
   docker-compose up --build
3. Backend: http://localhost:8000
   Demo (static): open web/index.html or serve it and call the API

Data & training
- See `data/` for where to put parallel and monolingual corpora.
- See `models/train.py` for high-level training steps (requires GPU for realistic fine-tuning).

Contributing
- See CONTRIBUTING.md and CODE_OF_CONDUCT.md

License
- MIT