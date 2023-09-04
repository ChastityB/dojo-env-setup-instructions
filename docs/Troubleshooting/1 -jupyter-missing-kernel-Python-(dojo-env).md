---
layout: page
title: Jupyter Missing Kernel Python (dojo-env)
parent: Troubleshooting
nav_order: 1
---

# Kernel Error / Jupyter Missing "Python (dojo-env)" in kernels

## PROBLEM:

---

- **If you see a message like this when trying to open the environment testing notebook:  
  **

![](../../images/lp/kernel_error.png)

- **OR if "Python (dojo-env)" doesn't show up in Jupyter Notebook in EITHER:**
  - The "New" menu on the Files tab in Jupyter.
- ![](../../images/lp/missing_kernel_new.png)

  - or the Kernel > Change Kernel menu inside a Jupyter Notebook:

    ![](../../images/lp/missing_kernel_notebook.png)

## Solution

- You missed a command after running the conda env create command during step 2, so let's rerun the command.
- First, shut down Jupyter Notebook

  - The quickest way is to go back to the Terminal/GitBash window that you used to start the notebook and press "control + C"

- **In your terminal/GitBash, make sure it says (dojo-env) above or next to your terminal prompt.**
  - if not, on Mac run:
    - "conda activate dojo-env"
  - on Windows run:
    - "source activate dojo-env"
- **Then run the command below to install dojo-env as a kernel in jupyter:**

```
python -m ipykernel install --user --name dojo-env --display-name "Python (dojo-env)"
```

Then, go ahead and boot up jupyter notebook and try again. It should now know the "Python (dojo-env)" kernel.
