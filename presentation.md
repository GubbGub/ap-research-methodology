---
marp: true
theme: gaia
_class: lead
paginate: true
backgroundColor: #000000
color: #ffffff
footer: '://github.com'
style: |
  section {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
    font-size: 28px;
    padding: 40px 60px;
  }
  h1 {
    color: #ffffff;
    font-weight: 800;
    font-size: 55px;
    letter-spacing: -1px;
    border-bottom: none;
    margin-bottom: 10px;
  }
  h2 {
    color: #a3a3a3;
    font-weight: 400;
    font-size: 32px;
    margin-top: 0;
  }
  strong {
    color: #38bdf8;
  }
  footer {
    font-family: 'Fira Code', monospace;
    color: #404040;
    font-size: 16px;
  }
  code {
    background: #171717;
    color: #f43f5e;
    font-family: 'Fira Code', monospace;
  }
  pre code {
    background: #0a0a0a;
    color: #e5e5e5;
    border: 1px solid #262626;
  }
---

# Methodologies Under Review
## Content Analysis & Experimental Research

![width:160px](https://qrserver.com)

###### Scan to view live interactive slides

By Jared Bridgewater

---

# Content Analysis: Overview
## Parsing Human Artifacts as Data

Content Analysis is a systematic, replicable technique for compressing many words of text into fewer content categories based on explicit rules of coding.

* **Primary Data Type:** Primarily **Qualitative** data sources transformed into **Quantitative** metrics.
* **The Core Engine:** You are parsing communications (text, source code, videos, logs) to uncover hidden patterns.

---

# Content Analysis: Implementation Pipeline

To execute this rigorously, researchers follow a deterministic data pipeline:

1. **Sampling:** Define the universe of data (e.g., *every commit message in a GitHub repo over 12 months*).
2. **Unitizing:** Break data into operational units (sentences, words, functions).
3. **Coding:** Apply a systematic "codebook" to label data (e.g., Category `0` = Obsolete Comment, Category `1` = Functional Comment).
4. **Statistical Analysis:** Calculate inter-rater reliability and frequency distributions.

---

# Content Analysis: Case Study
## Empirical Evaluation of Code Comment Quality

* **The Problem:** Software maintenance accounts for up to 80% of total software costs; bad documentation kills velocity.
* **The Methodology:** 
  * Researchers collected thousands of source code comments.
  * Used **Content Analysis** to manually categorize comments into distinct operational definitions (e.g., *Summary, Technical Debt indication, Bug workaround*).
  * Calculated frequency metrics to correlate comment quality with total software bugs.

---

# Experimental Research: Overview
## Establishing Definitive Causality

Unlike Content Analysis which observes existing data, **Experimental Research** actively manipulates the environment to prove cause and effect.

* **Primary Data Type:** Strictly **Quantitative**.
* **The Core Engine:** Isolating an independent variable (X) to measure its direct impact on a dependent variable (Y) while suppressing all external noise (confounding variables).

---

# Experimental Research: Architecture

```python
# Algorithmic Representation of an Experimental Design
def run_controlled_experiment(population_pool):
    # Step 1: Strict Random Assignment (Eliminates Bias)
    group_A, group_B = random_split(population_pool)
    
    # Step 2: Introduce Independent Variable to Experimental Group Only
    metrics_A = measure_productivity(apply_treatment(group_A)) # Experimental
    metrics_B = measure_productivity(baseline_control(group_B)) # Control
    
    # Step 3: Evaluate Statistical Significance (e.g., p-value < 0.05)
    return run_t_test(metrics_A, metrics_B)
```

---

# Experimental Research: Case Study
## The Impact of GitHub Copilot on Developer Productivity

* **The Problem:** Quantifying whether LLM pair-programmers actually increase velocity or just introduce errors.
* **The Methodology:**
  * **Participants:** 95 professional developers randomly split into two groups.
  * **Control Group:** Implemented an HTTP server in JavaScript *without* Copilot.
  * **Experimental Group:** Implemented the exact same server *with* Copilot enabled.
  * **Results:** The experimental group completed the task **55.8% faster** (a strictly quantitative dependent variable).

---

# Methodological Synthesis

| Feature | Content Analysis | Experimental Research |
| :--- | :--- | :--- |
| **Objective** | Uncover patterns in communication. | Establish causal links ($X \rightarrow Y$). |
| **Data Source** | Existing artifacts (Static). | Generated via trial (Dynamic). |
| **Manipulation** | **None.** Observational only. | **High.** Active intervention. |
| **Core Risk** | Subjective coding bias. | Confounding environmental variables. |

---
<!-- _class: lead -->

# Questions & Discussion
## Slides generated programmatically via Marp (Markdown)
Source code available at: **://github.com**
