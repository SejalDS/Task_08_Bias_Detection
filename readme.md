# Bias Detection in LLM-Generated Data Narratives  
*Task 08 – Research Project*

## 📌 Overview  
This project investigates whether Large Language Models (LLMs) exhibit **systematic bias** when interpreting identical datasets under differently framed prompts.  
The study evaluates four bias types:

- **Framing Bias**
- **Demographic Bias**
- **Confirmation Bias**
- **Selection Bias**

Experiments were conducted using anonymized sports performance data and multiple LLMs (GPT-4, Claude, Gemini). All responses were logged, analyzed, and validated for accuracy.

---

# 1. Task Completion Summary  
This project completed all required stages of Task 08:

- Designed hypotheses and prompt variations  
- Collected multi-model LLM responses  
- Performed sentiment, recommendation, and mention analysis  
- Conducted chi-square statistical testing  
- Validated model claims against ground truth  
- Produced fabrication reports and analysis summaries  
- Compiled findings into a final report

All analysis files (JSON summaries, chi-square tables, fabrication logs) are included in the repository.

---

# 2. Methodology Overview  

### **Phase 1 – Experimental Design**
Defined hypotheses around:
- Positive vs negative framing  
- Demographic mention conditions  
- Confirmation priming  
- Selection-based prompt wording  

Created **minimally different** prompt pairs for each hypothesis.

### **Phase 2 – Data Collection**
Queried multiple LLMs with structured dataset blocks.  
Collected 3–5 responses per prompt, logging:
- Prompt text  
- Model version  
- Timestamp  
- Output  

### **Phase 3 – Analysis**
Performed:
- Sentiment scoring  
- Keyword and mention extraction  
- Recommendation-type categorization  
- Pattern comparison across hypotheses  

### **Phase 4 – Claim Validation**
Used Python scripts to identify:
- Hallucinations  
- Unsupported claims  
- Contradictions  
- Ground-truth mismatches  

---

# 3. Dataset and Experiment Setup  
The dataset consisted of anonymized player performance statistics.  
All players were identified as:

- Player A  
- Player B  
- Player C  

Each hypothesis was tested with:
- A base dataset block (identical for all prompts)  
- Two prompt variants (e.g., positive vs negative framing)  
- Multiple LLM samples  

All raw outputs were logged into JSON/CSV files for analysis.

---

# 4. Key Findings  

### **Framing Effects**
- Sentiment shifted significantly based on framing:  
  - Positive framing → **sentiment 4.0**  
  - Negative framing → **sentiment 1.0**

### **Demographic Bias**
Introducing demographic cues altered:
- Which player was recommended  
- How the model described potential

### **Confirmation Bias**
Primed prompts produced responses aligned with the implied assumption.

### **Selection Bias**
Depending on prompt wording, different statistics were emphasized—even when the dataset was unchanged.

### **Hallucinations**
- **0% fabrication**
- No contradictions found across any condition

---

# 5. Statistical Analysis Summary  
Key analysis components included:

- **Sentiment means per hypothesis**  
- **Player mention frequency tables**  
- **Recommendation-type distributions**  
- **Chi-square tests** comparing:
  - H1 (negative vs positive framing)
  - H3 (neutral vs primed prompts)

Chi-square tables showed structural differences but limited statistical significance due to small sample sizes.

---

# 6. Bias Catalogue  

| Bias Type | Observed? | Example |
|----------|-----------|---------|
| **Framing Bias** | Yes | Sentiment shift from 1.0 → 4.0 |
| **Demographic Bias** | Yes | Different player mentioned when demographics included |
| **Confirmation Bias** | Yes | Primed prompts produced aligned reasoning |
| **Selection Bias** | Yes | Different stats highlighted per question framing |

All observed biases involved *tone* or *emphasis*, not factual fabrication.

---

# 7. Mitigation Strategies  

### **Prompt-Level**
- Use **neutral** and **unloaded** phrasing  
- Avoid unnecessary demographic details  
- Provide well-structured data tables  

### **Model-Level**
- Compare outputs across multiple models  
- Pin model versions for reproducibility  
- Use explicit JSON-based instructions  

### **User-Level**
- Validate claims using scripts  
- Apply post-processing checks  
- Encourage evidence-first reasoning  

---

# 8. Limitations  
- Small sample sizes limit statistical strength  
- Only three LLMs were used  
- Anonymization prevents testing real demographic interactions  
- Results may vary with future model updates  
- Temperature randomness introduces variability  

---

# 9. Skills Developed  
During this project, I strengthened competencies in:

- Controlled experimental design  
- Python-based data analysis  
- Sentiment and text classification  
- Chi-square statistical testing  
- LLM prompt engineering  
- Bias identification in AI systems  
- Ethical AI and responsible research practices  
- Scientific report writing  

---

# 10. Final Conclusion  
This project demonstrates that LLM-generated narratives are **highly sensitive to prompt framing and contextual cues**, even when evaluating identical data.  
Although no hallucinations were detected, measurable shifts in sentiment, narrative tone, and selected details confirm the presence of **subtle but consistent biases**.

These findings highlight the importance of:
- Careful prompt construction  
- Ground-truth alignment  
- Multi-model validation  
- Transparent and ethical AI workflows  

This repository provides a complete, reproducible pipeline for studying LLM bias using controlled prompt-based experiments.

---

# 📁 Repository Structure  

