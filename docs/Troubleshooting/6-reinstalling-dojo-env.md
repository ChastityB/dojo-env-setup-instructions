---
layout: page
title: Reinstalling Dojo Env
parent: Troubleshooting
nav_order: 6
---

# Reinstalling Dojo-Env

## What to do if your environment breaks and you need to re-install it.

- It is not uncommon to accidentally break our virtual environment by installing a new package or updating a pre-existing one.
- In the event that your environment stops working and it needs to be re-installed:
  1. open your terminal/gitbash and deactivate your `dojo-env`:
  - Type `conda activate base` or `conda deactivate` and press enter.
  - Your terminal should now say `(base)` with your prompt instead of `(dojo-env)`.
  2. Remove the broken `dojo-env` using the command:
  - `conda remove --name dojo-env --all`
  - enter `y` to approve the removal of the environment and hit enter.
  3. Wait for the env to be removed.
  - This will delete all of the files associated with JUST our `dojo-env`. So anconda will still be installed, we will just need to re-install our `dojo-env`.
  4. Once its completed, repeat the environment installation commands from step "2.3 Create the dojo-env environment"
  1. Don't forget to run the python -m ipykernel command after creating the dojo-env in step 2.3!
