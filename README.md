# SSC Smart Mock v2.5 — MCQ conversion improvement

This update improves OCR text grouping for common numbered questions and option labels such as `A)`, `A.`, `(A)`, `A:` and `A-`. It only carries over explicitly detected answer labels; it does not guess missing answers.

## Android update
1. Extract this ZIP.
2. In the GitHub repository, upload and commit `index.html` to replace the existing file.
3. Wait for GitHub Pages to deploy.
4. Open the published site in Chrome and test with a clear English question image.
5. Review all extracted questions and options before saving. OCR parsing is heuristic and may need manual correction.
