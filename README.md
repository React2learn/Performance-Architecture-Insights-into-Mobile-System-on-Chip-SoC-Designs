# 🧠 CPU & GPU Architecture Analysis – SoC Dataset

📁 **Dataset Overview**

- **Total Records**: 1022
- **Columns Analyzed**: `Designer`, `Type`, `Core Architecture`, `Number of CPU/GPU Cores`, `GPU Clock`, `Feature Size`, etc.
- **Source**: Cleaned dataset of processor specifications from various chip designers.

---

🎯 **Objectives**

- Analyze core architecture trends across chip designers.
- Evaluate GPU performance using proxy metrics.
- Compare design strategies of companies like Apple, Qualcomm, Samsung, etc.
- Identify top-performing processors by GPU Score.
- Uncover architectural preferences using Core Categories.

---

🔍 **Key Columns Used**

| Column Name                   | Description                                           |
|------------------------------|-------------------------------------------------------|
| `Designer`                   | Company that designed the chip (Apple, Intel…)       |
| `Type`                       | Chip model name                                       |
| `Number of processor core(s)`| Total CPU cores                                       |
| `GPU Clock`                  | Clock speed of GPU (MHz)                              |
| `Number of GPU cores`        | GPU core count                                        |
| `Core Category`              | Simplified architecture label (Big.LITTLE, etc.)     |
| `Feature Size`               | Transistor size (nm)                                  |

---

📈 **Key Analyses and Visuals**

### 1. 🧠 Core Architecture Usage by Designers
A **stacked bar chart** was created showing how different designers favor architectures like:
- **Big.LITTLE** (e.g., Apple, MediaTek, Samsung)
- **Qualcomm Kryo** (Qualcomm-specific)
- **Other/Custom** designs

📊 *This helped identify companies with custom cores versus ARM-licensed designs.*

---

### 2. 📊 Core Category Breakdown – Apple
A **pie chart** of Apple’s chips showed:
- 🟦 **98.1%** use **Big.LITTLE**
- 🟧 **1.9%** use **ARM Cortex**

💡 *Apple almost exclusively uses Big.LITTLE design in their recent processors.*

---


### 3. 🚀 GPU Score (Performance Proxy)
We calculated a performance metric:

```python
GPU Score = GPU Clock (MHz) × Number of GPU Cores
```

### 4. 🧪 Correlation and Relationships
Additional analyses performed:
 - 📈 Scatter plots: CPU core count vs GPU Score
 - 📉 Boxplots: Core Category vs GPU Score
 - 📊 Distribution analysis: Feature Size across different chip designs

### 🔧 Tools Used
 - Python: pandas, seaborn, matplotlib
 - Jupyter Notebook: for interactive exploration and visualization
