# Reported Results

These CSV files transcribe aggregate results from the camera-ready paper. They are not raw experimental logs, individual app records, or a newly executed evaluation. Table numbers refer to the paper.

| File | Paper table | Contents |
| --- | --- | --- |
| [table01-adoption.csv](table01-adoption.csv) | I | Sampled apps, testable apps, and LDM adoption by market |
| [table02-test-models.csv](table02-test-models.csv) | II | Keyword baseline and LLM comparison on the 60-app test set; LLMs use P2 |
| [table03-functionalities.csv](table03-functionalities.csv) | III | Five LDM functionalities among 241 apps |
| [table06-sam-results.csv](table06-sam-results.csv) | VI | SAM testing results by market |
| [table07-attribute-combinations.csv](table07-attribute-combinations.csv) | VII | Attribute combinations reported for 131 vulnerable apps |
| [table09-consequences.csv](table09-consequences.csv) | IX | Counts of apps affected by each reported consequence |
| [table10-validation-models.csv](table10-validation-models.csv) | X | Model comparison using P2 on the 240-app validation set |
| [table11-test-prompts.csv](table11-test-prompts.csv) | XI | P1, P2, and P3 comparison using Qwen3-Max on the 60-app test set |
| [table12-defenses.csv](table12-defenses.csv) | XII | Defense categories reported for 95 apps |

## Interpretation

- Percentage columns use the range 0 to 100, not 0 to 1. Rounding follows the paper.
- LDM adoption uses the number of testable apps as its denominator: 962 overall, rather than all 1,000 sampled apps.
- SAM vulnerability percentages use the 226 apps on which robustness testing was completed, rather than all 241 apps with LDM.
- Functionality categories in Table III may overlap. Consequences in Table IX may also overlap; their rows should not be summed to obtain a distinct app count.
- Table VII includes an explicit `Total` row. Do not add this row to the other rows.
- Table XII uses a denominator of 95. Its displayed percentages sum to 100.1% due to rounding.
- `tp`, `fp`, `fn`, and `tn` are the confusion matrix counts as reported in the paper. Model names and prompt labels are preserved as reported.

Precision is `TP / (TP + FP)`, recall is `TP / (TP + FN)`, F1 is `2 * TP / (2 * TP + FP + FN)`, and accuracy is `(TP + TN) / (TP + FP + FN + TN)`. Multiply each by 100 to compare with the CSV percentages.

The files do not contain the original app inventory, individual predictions, or the app identifiers assigned to each dataset split. Aggregate tables alone cannot reproduce the classification experiment.
