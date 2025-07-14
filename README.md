# When Random Meets Regs: AI Agents in the Real World – Demo Notebook

This repo accompanies my LinkedIn blog post **“When Random Meets Regs: AI Agents in the Real World.”**  
It contains a Colab notebook that reproduces the experiments described in the article:

* quantises every dial (temperature = 0, top-p = 0, fixed seed)  
* runs two 5-step self-feedback chains on GPT-4o-mini  
* logs the top-k (k = 2) log-probabilities for every token  
* highlights where—despite identical seeds—the chains first diverge  
  
---

## Repo contents

| File | Purpose |
|------|---------|
| **`Alice-Colab.ipynb`** | Colab notebook – end-to-end seed vs QRNG experiment |
| **`LICENSE`** | MIT License — feel free to fork / adapt |

---

## Quick start

1. Click the **“Open in Colab”** badge above.  
2. In Colab, select _Runtime ▸ Run all_.  
3. When prompted, set your `OPENAI_API_KEY` via **Colab ▸ Secrets**.  
4. Watch the two runs, then scroll to the coloured paragraphs to see where they split.

---

## Blog article

Read the full story – **When Random Meets Regs: AI Agents in the Real World** – on LinkedIn:

➡️ **[When Random Meets Regs: AI Agents in the Real World](https://www.linkedin.com/pulse/when-random-meets-regs-ai-agents-real-world-yuriy-yuzifovich-mcjsc/)**

---

## Why this matters

* A fixed seed alone does **not** guarantee replay: 16-bit math & mixture-of-experts routing introduce drift.
* Recording **top-k log-probs** gives auditors real insight into *why* a token was chosen.
* QRNG-derived seeds satisfy compliance logging _and_ restore true unpredictability.

Pull requests and issue reports welcome!
