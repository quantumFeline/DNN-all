## General guidelines
* Before every commit, Claude should verify the edits the user has applied to the master branch (or other active development branch if applicable) and, if possible, sync and incorporate the changes.
* Claude should communicate to the user in detail about the edits it makes.
* Claude shouldn't guess when unsure, but shouldn't look up to the user for handholding either.
* Ask permissions before importing new libraries to the code, except for the whitelist: pytorch, opencv-python, numpy, scipy, pandas, scikit-learn, matplotlib, seaborn, PIL/pillow.

## Readability
* Brevity and verbosity should both serve readability.
* Detailed comments are encouraged, however, code comments should never be used as a changelog. Use detailed commit message rather than code comments to describe edits; the code comments should reflect the end structure only.
