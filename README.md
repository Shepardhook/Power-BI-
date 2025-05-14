Copyright (c) 2024 Brad Stafford

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.


# 🎯 Power BI Interview Dashboard – End-to-End Sample Project

This repository showcases an end-to-end Power BI dashboard project used for interviews. It simulates a real-world analytics workflow—from data creation to transformation, DAX modeling, Python visuals, and machine learning integration.

## 📦 Key Features

- ✅ **Synthetic Data Creation** using DAX Studio
- 🛠 **Data Transformation** with Power Query
- 📊 **Custom Views** and calculated columns using DAX
- 📈 **Python Heatmap Visualization** for exploratory data analysis
- 🤖 **Machine Learning Script** integrated within Power BI
- 🔁 **Repeatable Framework** for future use or extension

---

## 🔍 Project Overview

| Feature             | Description |
|---------------------|-------------|
| **Toolset**         | Power BI Desktop, DAX Studio, Python |
| **Visuals Used**    | Heatmaps, Bar Charts, KPI Cards |
| **ML Integration**  | Embedded Python script (e.g., scikit-learn, seaborn) |
| **Data Origin**     | Synthetic (Generated via DAX Studio) |
| **Use Case**        | Demonstrates full BI lifecycle: ETL → Model → Visualize → Predict |

---

## 🧠 Python Heatmap

The `Scripts/heatmap_script.py` visualizes correlation between numerical features to aid feature selection and insights.

```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

df = dataset
corr = df.corr()
sns.heatmap(corr, annot=True, cmap='coolwarm')
plt.show()
🧪 ML Integration
Sample ML script to perform clustering (or classification) using scikit-learn:

python
Copy
Edit
from sklearn.cluster import KMeans
model = KMeans(n_clusters=3)
model.fit(dataset[['feature1', 'feature2']])
dataset['cluster'] = model.labels_
