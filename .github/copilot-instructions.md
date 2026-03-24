**Purpose**: Short, actionable guidance for AI coding agents working on this repository.

- **Repo shape**: single Jupyter notebook: [EDA.ipynb](EDA.ipynb). The notebook currently contains no code cells (empty `cells` array).
- **No detected files**: there is no `requirements.txt`, `README.md`, or existing AI instruction files in the repo root.

**How to get started (fast)**
- Open [EDA.ipynb](EDA.ipynb) in Jupyter or VS Code Notebook view and look for imports and data-load calls (`pd.read_csv`, `open(...)`, etc.).
- If cells are present, run cells in order to reproduce the environment; otherwise, ask the maintainer before creating new content.

**Local dev commands (Windows PowerShell)**
- Create a venv: `python -m venv .venv`
- Activate: `.\.venv\Scripts\Activate.ps1`
- Install deps (if a `requirements.txt` is added): `pip install -r requirements.txt`
- Start Jupyter Lab: `jupyter lab` or `jupyter notebook`

**Project-specific patterns & constraints**
- Notebook-first: the primary artifact is `EDA.ipynb`. Changes to analysis should prefer adding new, clearly named notebook cells or a separate module under a new `src/` folder if code is intended for reuse.
- No CI/tests detected: do not assume automated test runners are present.
- Data handling: this repo contains no tracked data. Search notebooks for explicit file paths before attempting to run code; ask if data is private or unavailable.

**When modifying or adding files**
- If you add Python scripts, include a `requirements.txt` (pin minimally) and document runnable steps in `README.md`.
- For notebooks: prefer committing with outputs cleared when changes are non-essential to results, and include a brief commit message summarizing the analysis change.

**Examples (what an agent might do next)**
- If `pd.read_csv('data.csv')` appears in `EDA.ipynb`: report the path, request the data, or create a small mock CSV for reproducible local testing.
- If you add a helper module: create `src/` and a short `README.md` with the run steps shown above.

**Notes for human reviewers**
- The repository is minimal. Before making structural changes, confirm availability of data and desired workflows (notebooks vs. scripts).

If anything here is unclear or you'd like more detail (dev workflow, testing, or CI suggestions), tell me which area to expand.
