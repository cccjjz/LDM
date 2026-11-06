# Evaluation Notes

This document summarizes the experimental setup reported in the paper. It does not add configuration values or claim to reproduce experiments that have not been rerun.

## LDM Identification

Section III-A describes a pipeline with:

1. APK resource extraction using Apktool, string resource resolution, and conversion of UI layouts into JSON evidence.
2. Keyword filtering to select candidate layouts.
3. LLM classification followed by manual verification by two security analysts.

The paper reports 1,000 unique sampled apps across Google Play and Huawei App Market. Of 962 testable apps, 241 were identified as providing LDM. See [Table I](../results/table01-adoption.csv).

For classifier evaluation, 300 manually labeled apps were divided into a validation set of 240 apps and a test set of 60 apps. The validation set contains 120 apps from each market; the test set contains 30 from each market.

Tables II, X, and XI report model and prompt comparisons. The complete P2 text is provided in [prompts/P2-enriched.txt](../prompts/P2-enriched.txt).

## Robustness Evaluation

The paper reports robustness testing on 226 of the 241 apps with LDM. Its sandbox supports AOSP 10 and AOSP 14. Testing involves device attribute collection and manipulation followed by manual observation of LDM behavior. See Section IV for the threat model and success criteria, including the auxiliary concurrent-login test.

The aggregate results are in [results/](../results/README.md). The APK dataset, app-level evaluation records, system images, and core sandbox code are subject to the email request process described in the [project README](../README.md#artifact-access); they are not included in the public files.

## Scope of These Files

The provided CSVs contain reported aggregate results, not the original evaluation dataset. The original app inventory, annotations, exact split membership, individual model predictions, full P1/P3 texts, and executable identification pipeline are not included in this package.

The paper source does not provide all runtime settings needed to recreate the LLM runs, such as a split seed or complete model invocation parameters. No replacement values are supplied here.
