# MCQ Generator 📝🤖

An AI-powered **Multiple Choice Question (MCQ) Generator** built with **Streamlit**.

This tool lets educators, instructional designers, and trainers quickly create **pedagogically sound MCQs** from any input text. It supports multiple LLM backends (OpenAI, Claude, Gemini, Perplexity) and lets users control difficulty via the **European Qualifications Framework (EQF)**, number of questions, distractors, feedback, hints, and output format.

---

## ✨ Features

- 🔐 **Bring-your-own-API-key**  
  No keys are stored in the code or repo. Each user enters their own API key in the sidebar. The app automatically validates the key before use.

- 🧠 **Multiple LLM backends**
    - OpenAI (GPT-4 family)
    - Anthropic Claude (Coming soon)
    - Google Gemini (Coming soon)
    - Perplexity (Llama Sonar models) (Coming soon)

  Models are configured centrally in `core_logic/llm_config.py`.

- 🎯 **Difficulty via EQF levels**
    - Question difficulty is aligned with the **European Qualifications Framework (EQF)** (levels 1–8).
    - Lets you generate questions for anything from basic knowledge checks to advanced / higher education assessments.

- ⚙️ **Flexible question configuration**
    - Number of questions
    - Number of correct answers per question
    - Number and difficulty of distractors (obvious / normal / challenging)
    - Optional learning objectives
    - Optional hints and learner feedback

- 🧾 **Multiple output formats**
    - Plain text format
    - Open edX **OLX** format (for LMS integration)

- 🔁 **Revision workflow**
    - Ask the AI to revise its previous answer with an additional prompt.
    - Limits revisions per phase to avoid runaway usage.

- 💬 **Chat history**
    - The sidebar keeps track of user prompts and AI responses across phases.

--- 

## 📁 Project Structure

A minimal overview of the key files:

```text
.
├── mcq-generator-app.py      # Entry point for the MCQ generator micro-app
├── core_logic/
│   ├── main.py               # Generic multi-phase Streamlit engine
│   ├── handlers.py           # LLM family handlers (OpenAI, Claude, Gemini, Perplexity, RAG)
│   └── llm_config.py         # Model registry and default parameters
├── requirements.txt
└── README.md
```

--- 

## 📖 How to Cite

If you use this tool in your teaching, research, or publications, please cite the following paper:

Elhayany, M. *AI-Powered MicroApps for Online Assessments: Impacts on Efficiency, Quality, and Future Directions.*  
Available at: https://ieeexplore.ieee.org/abstract/document/10748039

### BibTeX

```bibtex
@INPROCEEDINGS{elhayany2024aipoweredmicroapps,
  author={Elhayany, Mohamed and Swope, John and Rushe, Shannon and Meinel, Christoph},
  booktitle={2024 IEEE Digital Education and MOOCS Conference (DEMOcon)}, 
  title={AI-Powered MicroApps for Online Assessments: Impacts on Efficiency, Quality, and Future Directions}, 
  year={2024},
  volume={},
  number={},
  pages={1-6},
  keywords={Technological innovation;Computer aided instruction;Electronic learning;Generative AI;Chatbots;Generators;Artificial intelligence;AI-Powered Micro-Apps;GPT-3.5;Artificial Intelligence;Online Education;Assessment},
  doi={10.1109/DEMOcon63027.2024.10748039}}
```

---