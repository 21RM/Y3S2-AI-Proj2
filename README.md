# README

## Environment Setup

1. **Create a virtual environment**

   ```bash
   python3 -m venv .venv
   ```

2. **Activate the virtual environment**

   - **Linux/macOS**:
     ```bash
     source .venv/bin/activate
     ```
   - **Windows (PowerShell)**:
     ```powershell
     .\.venv\Scripts\Activate.ps1
     ```

3. **Upgrade pip**

   ```bash
   pip install --upgrade pip
   ```

4. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

## requirements.txt

List of core packages

## Jupyter Kernel Registration

Register the `.venv` interpreter as a Jupyter kernel:

```bash
python3 -m ipykernel install --user --name proj2-env --display-name "Python (proj2-env)"
```

## Using VS Code (optional)

- Install the **Python** extension by Microsoft.
- Select interpreter: click the Python version in the bottom-right → choose `Proj2/.venv/bin/python3`.
- Reload window: `Ctrl+Shift+P` → **Developer: Reload Window**.
- In notebooks, select kernel **Python (proj2-env)**.

## Verifying the Setup

After installation, run:

```bash
python - <<EOF
import pandas, numpy, sklearn, imblearn, matplotlib, seaborn
print('Setup OK')
EOF
```

## Project Structure

```
Proj2/
├── data/                     # CSV data files
├── notebooks/                # Jupyter notebooks for EDA and modeling
│   ├── 01_data_loading.ipynb
│   └── 02_preprocessing_and_modeling.ipynb
├── requirements.txt          # Python dependencies
└── README.md                 # This setup guide
```

---

Now you can launch JupyterLab or run your modeling notebooks with a consistent, reproducible environment.
