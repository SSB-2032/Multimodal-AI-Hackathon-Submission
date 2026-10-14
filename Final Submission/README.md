# MentorAI — Closed-Loop Multimodal AI Study Companion (Track D)

**MentorAI** is a national competition submission for **Track D (Personalized Tutoring & Adaptive Learning)**. It moves beyond standard Q&A chatbots by implementing a continuous, source-grounded educational cycle with measurable learning outcomes and broad multi-format document support.

---

## 🌟 Product Thesis: The Closed Learning Loop

Most AI study tools stop at answering questions. **MentorAI** redefines educational AI by executing a complete 6-stage workflow:

```
Course Evidence ──> Citation Explanation ──> Adaptive Assessment
                                                    │
Measured Gain <── Targeted Remediation <── Skill Diagnosis
```

---

## 🚀 Key Features & Competitive Differentiators

1. **Multi-Format Ingestion**: Native parsing for PDFs (textbooks), PPTX (slides), DOCX (notes), CSV/JSON (datasets), TXT/MD, and SRT/VTT (video/lecture transcripts).
2. **Evidence-First Tutoring**: Ingests multi-format course materials into a source-cited knowledge base. Every answer explicitly cites source locations and document formats.
3. **Explainable Learner Model**: Tracks student skill mastery percentages across granular competencies ("Limit Computation", "Discontinuity Classification", "5-Step Continuity Sequence") instead of an opaque aggregate score.
4. **Adaptive Next-Step Engine**: An incorrect answer automatically updates skill state and triggers a targeted remedial explanation and diagnostic micro-quiz.
5. **Learning-Gain Engine**: Measures pre-test vs. post-test performance and computes normalized learning gain ($g = \frac{\text{Post} - \text{Pre}}{100 - \text{Pre}}$).
6. **Universal Free Cloud & Offline Resilience**: Natively supports Google Gemini 1.5 Flash/Pro, Groq Llama 3.3, or OpenAI, with a complete local fallback ensuring 100% pitch uptime even without API keys or network connection.

---

## 💻 Quick Start & Installation

```bash
# 1. Clone repo & create virtual environment
python -m venv .venv

# On Windows:
.venv\Scripts\activate
# On macOS/Linux:
source .venv/bin/activate

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run Streamlit App
streamlit run app.py
```

> **Demo Tip**: Click **"⚡ Load Calculus Demo Course"** in the sidebar to run the full tutor → adaptive quiz → skill update → learning gain loop instantly without uploading files!

---

## 📁 Repository File Structure

* `app.py` — Complete Streamlit Web Application (Multi-format parser, RAG engine, learner model, evaluation view).
* `requirements.txt` — Python dependencies (`streamlit`, `pandas`, `pypdf`, `python-pptx`, `python-docx`, `openai`, `pytest`).
* `demo_course.txt` — Bundled Calculus course content on Continuity & Limits.
* `EVALUATION_PLAN.md` — Comprehensive 4-pillar benchmark report.
* `README.md` — System documentation & setup guide.
