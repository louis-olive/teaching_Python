# Introduction to Python Course

Welcome! 

This repository contains Jupyter notebooks and materials for the course.

---

## 1. Start on Google Colab (no installation needed)
For the first lesson of the course, you can run the notebooks directly in the browser with Google Colab.

Click on a notebook link in this repo (for example:  
[01_introduction_to_python_wo_solutions.ipynb](https://githubtocolab.com/louis-olive/teaching_Python/blob/master/notebooks/01_introduction_to_python_wo_solutions.ipynb))  

This will open the notebook in Google Colab, where you can run the code immediately.

AVAILABLE NOTEBOOKS

* First lesson (Intro to python) with empty code chunks / without exercises solutions: [Open in Colab](https://githubtocolab.com/louis-olive/teaching_Python/blob/master/notebooks/01_introduction_to_python_wo_solutions.ipynb)

TO BE UPLOADED LATER

* First lesson (Intro to python) with exercises solutions: [Open in Colab](https://githubtocolab.com/louis-olive/teaching_Python/blob/master/notebooks/01_introduction_to_python.ipynb)

* Second lesson (Data analysis) with empty code chunks / without exercises solutions: [Open in Colab](https://githubtocolab.com/louis-olive/teaching_Python/blob/master/notebooks/02_data_analysis_with_python_wo_solutions.ipynb)

* Second lesson (Data analysis) with exercises solutions: [Open in Colab](https://githubtocolab.com/louis-olive/teaching_Python/blob/master/notebooks/02_data_analysis_with_python.ipynb)

* Third lesson (Data analysis case study) with case study instructions/material and almost empty notebook: [Open in Colab](https://githubtocolab.com/louis-olive/teaching_Python/blob/master/notebooks/03_real_estate_eda_wo_solutions.ipynb)

* Third lesson (Data analysis case study) with a proposed solution: [Open in Colab](https://githubtocolab.com/louis-olive/teaching_Python/blob/master/notebooks/03_real_estate_eda.ipynb)

* Fourth lesson (US Treasury bonds case study) with case study instructions/material: [Open in Colab](https://githubtocolab.com/louis-olive/teaching_Python/blob/master/notebooks/04_US_treasury_bonds_wo_solutions.ipynb)

* Fourth lesson (US Treasury bonds case study) with solutions: [Open in Colab](https://githubtocolab.com/louis-olive/teaching_Python/blob/master/notebooks/04_US_treasury_bonds.ipynb)


---

## 2. Install Your Local Setup (Windows / macOS)

Later in the course, it is better to work locally with **miniconda + VS Code + Quarto**.  

**miniconda** is a lightweight version of Anaconda that includes only Python and Conda (the environment manager). It lets us install just the packages we need, keeping the setup small and consistent across systems.

**VS Code** is a lightweight code editor, with the right extensions, it lets you:
- Write & run Python code / Jupyter notebooks (.ipynb)
- Explore variables (like in Jupyter Lab)
- Work with pandas tables interactively
- Use terminal and Git — all in one place

**Quarto** turns Jupyter notebooks or .qmd files into reports. You can publish to:
- HTML, PDF, Word, or slides
- With live code, plots, and text in one file
This course is made with Quarto.

Follow the steps carefully, in order:

### Step 1. Install Miniconda
- Download the installer from: [https://docs.conda.io/en/latest/miniconda.html](https://docs.conda.io/en/latest/miniconda.html)
- Install with all default options.
- More details if needed ([Windows](https://wesmckinney.com/book/preliminaries#installation_windows)/[macOS](https://wesmckinney.com/book/preliminaries#installation_mac))

### Step 2. Install VS Code
- Download from: [https://code.visualstudio.com/](https://code.visualstudio.com/)  
- During installation, allow **"Add to PATH"** if asked.


### Step 3. Install VS Code Extensions
Open VS Code, press `Ctrl+Shift+X` (Windows) or `Cmd+Shift+X` (macOS) or click on the Extensions icon in the left sidebar (square blocks icon), and install the following extensions:
- **Python** (Microsoft)
- **Jupyter** (Microsoft)
- **Quarto** (Quarto)

See also VS Code Quick Start Guides for [Python](https://code.visualstudio.com/docs/python/python-quick-start) and [Jupyter Notebooks](https://code.visualstudio.com/docs/datascience/jupyter-notebooks).

### Step 4. Install Quarto
- Download from: [https://quarto.org/docs/get-started/](https://quarto.org/docs/get-started/)  
- Install with default options.
- https://quarto.org/docs/get-started/hello/vscode.html

We'll start out by rendering a simple example (`hello.qmd`) to a couple of formats.
If you want to follow along step-by-step in your own environment, create a new file named `hello.qmd` and copy the following content into it.

```` markdown
---
title: "Quarto Basics"
format:
  html:
    code-fold: true
jupyter: python3
---

For a demonstration of a line plot on a polar axis, see @fig-polar.

```{{python}}
#| label: fig-polar
#| fig-cap: "A line plot on a polar axis"

import numpy as np
import matplotlib.pyplot as plt

r = np.arange(0, 2, 0.01)
theta = 2 * np.pi * r
fig, ax = plt.subplots(
  subplot_kw = {'projection': 'polar'} 
)
ax.plot(theta, r)
ax.set_rticks([0.5, 1, 1.5, 2])
ax.grid(True)
plt.show()
```
````

Once the environment is active and the Quarto extension is installed:
- Open a `.qmd` or `ipynb` file .
- Click **Render** in the top-right of VS Code or:
    - **Windows/Linux:** `Ctrl + Shift + K`  
    - **macOS:** `Cmd + Shift + K`

---


## 3. Get the Course Files

1. Go to the GitHub course repository [page](https://github.com/louis-olive/teaching_Python).  
2. Click the green **Code** button → **Download ZIP**.  
3. Unzip the folder somewhere on your computer (e.g., in your user folder such as `Users/<yourname>/` on macOS or `C:\Users\<yourname>\` on Windows).  
4. In VS Code: **File → Open Folder** → select the unzipped course folder.

If you know what you are doing use `git`
---

## 4. Create and Activate the Conda Environment

1. Open **VS Code Terminal**:  
   menu **View → Terminal**

2. Create the conda environment (run once):
   ```bash
   conda env create -f environment.yml
   ```

3. Activate the environment:
   ```bash
   conda activate tse-python-course
   ```

4. Verify activation: the terminal prompt should show `(tse-python-course)` at the beginning.

---

## 5. Work with Notebooks in VS Code

1. Open any `.ipynb` notebook file from the repo.  
2. When asked, select the **Python kernel**: choose **tse-python-course**.  
3. Run cells with `Shift+Enter`.


---

## Done!
You now have two options to work with the course:
- **Google Colab**: easiest start (nothing to install) + free GPU.
- **miniconda + VS Code + Quarto**: full local setup for more control.

---

