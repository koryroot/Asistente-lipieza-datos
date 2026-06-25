# 🧹📊 Interactive Data Cleaning Assistant (Interactive EDA Cleaner)

[Status: In Development 🚧]

A Python script for Jupyter/Colab that automates Exploratory Data Analysis (EDA) diagnostics and provides an interactive interface for data cleaning decision-making.

## The Problem: Manual EDA is Slow

Exploratory Data Analysis (EDA) is fundamental, but we often find ourselves executing the same commands (`.isnull().sum()`, `.describe()`, `boxplot...`) repeatedly. Identifying a problem is only the first step; deciding *how* to resolve it (impute, drop, transform) is the critical part, and it usually involves a manual, trial-and-error process.

## The Solution: A Decision-Making Assistant

This project combines the power of **automated diagnostics** with **interactive decision-making**.

Instead of merely generating a static report, this tool:
1.  **Diagnoses:** Uses `ydata-profiling` to scan a DataFrame and identify key data quality issues (missing values, duplicates, outliers, data types).
2.  **Prompts:** Uses `ipywidgets` to present these issues to the user alongside reasoned cleaning options (e.g., impute with mean, median, mode; drop rows/columns).
3.  **Acts:** Applies the selected transformations to the DataFrame, enabling an iterative and controlled data cleaning cycle.

## Tech Stack

* **Python 3.x**
* **Pandas:** For data manipulation and structures.
* **ydata-profiling:** For diagnostic report generation.
* **ipywidgets:** For building the interactive UI within Jupyter.
* **Scikit-learn:** (Coming soon) For advanced imputation techniques (e.g., KNNImputer).

## Getting Started

1.  Clone this repository:
    ```bash
    git clone [https://github.com/koryroot/Asistente-lipieza-datos.git](https://github.com/koryroot/Asistente-lipieza-datos.git)
    ```
2.  Install dependencies:
    ```bash
    pip install pandas ydata-profiling ipywidgets
    ```
3.  Open the `interactive_eda.ipynb` notebook in Jupyter Lab or Google Colab.
4.  Load your dataset and start cleaning!

## Roadmap (Next Steps)

* [ ] Implement interactive duplicate handling.
* [ ] Add outlier detection and handling methods (IQR, Z-score).
* [ ] Integrate advanced imputation (KNNImputer) as a selectable option.
* [ ] Add "before and after" data visualizations for the cleaning process.

## Contributing

This is a continuous learning project and is open to contributions! If you have ideas to improve the tool, please open an Issue or submit a Pull Request.
