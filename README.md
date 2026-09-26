# Kayardild Nominal Case Morphology

XFST/lexc implementation of nominal case morphology in Kayardild 
(Tangkic, Australia), covering the core case system, case stacking, 
number marking, and stem-final sandhi.

## Files
- `kayardild.txt` — lexc lexicon
- `sandhi.txt` — xfst sandhi rule
- `kayardild.xfst` — build/test script; loads the lexicon and sandhi 
  rule, applies every analysis in `kayardild_inputs.txt`, and writes 
  the resulting surface forms to `kayardild_output.txt`
- `kayardild_inputs.txt` — test analyses (one per line, fed to 
  `kayardild.xfst`)
- `kayardild_goals.txt` — reference surface forms, generated from the 
  verified grammar; compared against `kayardild_output.txt`
- `kayardild_test.tsv` — annotated test suite (input, expected output, 
  attested/analogous status, and source citation for each case)
- `run_xfst_from_python.ipynb` — automated test runner: invokes 
  `kayardild.xfst`, then diffs `kayardild_output.txt` against 
  `kayardild_goals.txt`

## Usage
Requires an xfst-compatible tool (e.g. hfst-xfst) on PATH. Adjust the 
`directory`/`application` variables in the notebook, then run all cells.

## References
Evans, Nicholas D. (1995). *A Grammar of Kayardild*. Mouton de Gruyter.
Round, Erich Ross (2013). *Kayardild Morphology and Syntax*. Oxford University Press.
