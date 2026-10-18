# Personalized Chakra-Based Yoga Flow Recommender

COMP 365 individual project — Aniya Teasley

## Project overview
This is a small **rule-based** yoga-pose recommendation prototype. It compares (1) chakra-only filtering, (2) equal-weight preference ranking, and (3) weighted preference ranking. It is **not a trained ML model** and makes no medical claims.

## Reproduce results in Google Colab
1. Open https://colab.research.google.com/ and upload `Chakra_Yoga_Recommender_Final_Expanded.ipynb`.
2. Select **Runtime > Run all**. No external data file is required: the 21-pose table and five evaluation profiles are included in the notebook.
3. Find the final comparison table and bar chart. The final code cells save `three_method_results.csv`, `three_method_summary.csv`, and `three_method_comparison.png` to the Colab session's working directory.
4. Download these files from the Colab Files sidebar if desired.

## Reproduce locally
1. Download or clone this GitHub repository.
2. Install Python 3 and Jupyter Notebook.
3. Open a terminal in the project folder.
4. Install dependencies using `python -m pip install -r requirements.txt`.
5. Open `Chakra_Yoga_Recommender_Final_Expanded.ipynb` in Jupyter Notebook.
6. Select **Run All** to execute every cell from top to bottom.

**Hardware requirements:** A standard personal computer is sufficient. No GPU or specialized hardware is required. The notebook uses IPython's `display` function, supported in Jupyter and Google Colab.
## Expected comparison (five fixed profiles)
| Method | Mean top-pick preference matches (0–3) | Mean list match rate |
| --- | ---: | ---: |
| Chakra-only baseline | 2.0 | 65.02% |
| Equal-weight personalization | 3.0 | 65.02% |
| Weighted personalization | 3.0 | 65.02% |

The equal list-match rate is expected because all three methods return the same chakra-filtered candidates, reordered. The weighted method did not improve top-pick matching over equal-weight ranking in these five cases.

## Data and method details
The notebook embeds 21 manually organized pose records with Pose, Chakra, Level, Body Focus, Goal, Minutes, and source-page URL fields. Public pose pages are attributed to Tummee (https://www.tummee.com/yoga-poses). Fields are manually assigned for this prototype and must not be represented as independently validated medical advice. The baseline takes the first four poses in the selected chakra in dataset order. Equal-weight scoring assigns 1 point for each match on level, body focus, and goal (plus a common 1-point chakra-filter base). Weighted scoring assigns 1, 2, and 3 points respectively. Minutes break ties. No model training, random split, or fine-tuning was performed.

## Evaluation and limitations
The five profiles are hand-selected and are not a representative user sample. Top-pick match counts matching metadata fields (0–3), not clinical suitability or real-world satisfaction. The notebook's 15 'reviewer' choices are **simulated illustrative responses, not actual human participants** and must not be presented as human evaluation evidence. No IRB approval or human-subject experiment is claimed. Some chakra categories contain fewer than four poses. Pose labels, source URLs, and suitability need independent verification.

## Included files
- `Chakra_Yoga_Recommender_Final_Expanded.ipynb` — executable notebook
- `three_method_results.csv` — per-profile, per-method results
- `three_method_summary.csv` — mean metrics
- `three_method_comparison.png` — results visualization
- `requirements.txt` — Python dependencies
- `DEMO_SCRIPT.md` — recording outline
- `SUPPLEMENTAL_PAGE_TEMPLATE.md` — fill-in links for the final PDF

## Public access checklist
Before submission, upload these materials to a **public GitHub repository** (or another instructor-approved accessible host). Test the link in a private/incognito window. Add the final repository URL and demo video URL to the supplemental page of the paper. Do not publish personal information or credentials.
