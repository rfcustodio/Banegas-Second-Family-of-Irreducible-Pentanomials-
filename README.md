# Banegas' Second Family of Irreducible Pentanomials (paper source)

This repository is synchronised with **Overleaf**. It holds only the LaTeX source of the paper
and the files needed to compile it.

| File | Content |
|---|---|
| `main.tex` | Paper source (the file Overleaf compiles). |
| `refs.bib` | Bibliography (`biblatex` with `backend=biber`, the Overleaf default). |
| `fig_gain.pdf`, `fig_census.pdf` | Figures 2 and 3 (Figure 1 is TikZ inside `main.tex`). |
| `codigo/`, `dados/` | Snapshot of the code and data used for the first draft (see `LEIAME.txt`). |
| `old.tex` | Earlier version of the text, kept for reference; not compiled. |

**Verification.** Every proposition, table and number of the paper is checked by the scripts in
the companion repository
[`rfcustodio/banegas-second-family-verification`](https://github.com/rfcustodio/banegas-second-family-verification),
which also has the up-to-date code and data. To check the paper:

```bash
git clone https://github.com/rfcustodio/banegas-second-family-verification
cd banegas-second-family-verification
./run_quick_checks.sh
```

If you change a number in `main.tex`, update the corresponding check there
(see `docs/CLAIMS.md` and `docs/WORKFLOW.md` in that repository).

**Compile locally:** `pdflatex main && biber main && pdflatex main && pdflatex main`.
