# Alm
# Part B — Kernel Learning (Centered Alignment)
**Student name:** Pintu singh
**Student ID:** 230105  
**Assignment:** Midsem Part B  
**Deadline:** 12 March 2026, 8 AM  

---

## 📄 Paper Reference

**"Algorithms for Learning Kernels Based on Centered Alignment"**  
Cortes, Mohri, Rostamizadeh — JMLR 2012

---

## 📁 Repository Structure

```
partB/
├── task_1_1.ipynb          # Q1: Algorithm steps (ALIGN / ALIGNF)
├── task_1_2.ipynb          # Q1: Key assumptions
├── task_1_3.ipynb          # Q1: Baseline comparison
├── task_2_1.ipynb          # Q2: Toy dataset setup
├── task_2_2.ipynb          # Q2: ALIGNF implementation
├── task_2_3.ipynb          # Q2: Results + plots
├── task_3_1.ipynb          # Q3: Ablation study
├── task_3_2.ipynb          # Q3: Failure mode analysis
├── report.pdf              # Q4: 4-page summary report
├── requirements.txt        # Python dependencies
├── data/
│   └── README.md
├── results/                # Generated plots / figures
│   ├── task2_results.png
│   ├── task3_1_ablation.png
│   └── task3_2_failure.png
└── llm_task_1_1.json       # Q4: LLM interaction logs
    llm_task_1_2.json
    llm_task_1_3.json
    llm_task_2_1.json
    llm_task_2_2.json
    llm_task_2_3.json
    llm_task_3_1.json
    llm_task_3_2.json
    llm_task_4_1.json
    llm_task_4_2.json
```

---

## 📝 Task Summary

| Task | Description | Marks |
|------|-------------|-------|
| Q1 (task_1_1 to 1_3) | Paper understanding — markdown only, no code | 25 |
| Q2 (task_2_1 to 2_3) | ALIGN/ALIGNF implementation on toy dataset | 40 |
| Q3 (task_3_1 to 3_2) | Ablation study + failure mode analysis | 35 |
| Q4 | Report PDF + LLM JSON logs | 30 |
| **Total** | | **130** |

---

## 🧠 Core Idea

- **Problem:** SVM ke liye optimal kernel manually choose karna mushkil hai.
- **Solution:** Multiple base kernels ko combine karo — unke **Centered Alignment** (target ke saath similarity) ke basis pe weights automatically seekho.

### Two Algorithms:
| Algorithm | Approach |
|-----------|----------|
| **ALIGN** | Har kernel ka weight independently compute karo (simpler) |
| **ALIGNF** | Weights jointly QP solve karke seekho (better performance) |

---

## ⚙️ Setup & Installation

```bash
pip install -r requirements.txt
```

### Requirements:
- Python 3.8+
- numpy
- scikit-learn
- matplotlib
- cvxpy (for ALIGNF QP solver)
- jupyter

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/Alm
   cd 230105-midsem/partB
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run notebooks in order:
   ```
   task_1_1.ipynb → task_1_2.ipynb → task_1_3.ipynb
   task_2_1.ipynb → task_2_2.ipynb → task_2_3.ipynb
   task_3_1.ipynb → task_3_2.ipynb
   ```

4. All outputs/plots will be saved in `results/`

---

## 📊 Key Results

- **ALIGNF** outperforms uniform kernel combination on toy dataset
- Ablation study shows centered alignment is the critical component
- Failure mode: algorithm degrades when kernel matrices are highly correlated

---

## ⚠️ Notes

- Part A (paper: Centered Alignment, JMLR 2012) has been submitted via Google Form — Part B is valid.
- All notebooks must be **executed with outputs visible** before final GitHub submission.
- Google Form submission link: https://forms.gle/yxfmRprmHDeAzx1C7
