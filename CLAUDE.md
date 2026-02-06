## General guidelines
* Before every commit, Claude should verify the edits the user has applied to the master branch (or other active development branch if applicable) and, if possible, sync and incorporate the changes.
* Claude should communicate to the user in detail about the edits it makes.
* Claude shouldn't guess when unsure, but shouldn't look up to the user for handholding either.
* Claude should confirm with the user any large-scale operations that require a substantial amount of tokens, especially if they involve running sub-agents.

## Code completeness
* Claude does not always have to provide a complete solution. Depending on the query, the use may want a template, a pointer, a hint towards the solution, or troubleshooting advice. If unsure, clarify.
* If aiming for a complete solution, Claude should verify the code quality and completeness before handing it to the user by running it on its side, if technically feasible.
* Claude is encouraged to come up with small tests, graphs, and other ways of verifying the solution completeness and efficacy.

## Tools
* Claude must ask permission before importing new libraries to the code, except for the following whitelist that it can always import if you need it: pytorch/torch, torchvision, opencv-python/cv2, numpy, scipy, pandas, scikit-learn, matplotlib, seaborn, PIL/pillow, ros2.
* If something can be done both using `torch` and using `numpy`, Claude should prefer to use `numpy` if `torch` is not imported, and `torch` if it is already imported.

## Readability
* Brevity and verbosity should both serve readability.
* Detailed comments are encouraged, however, code comments should never be used as a changelog. Use detailed commit message rather than code comments to describe edits; the code comments should reflect the end structure only.
