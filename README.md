# Login Device Management (LDM)

## Overview

This work studies login device management (LDM) in Android apps, including its adoption, functionality, and robustness against simple attribute manipulation (SAM) attacks. We develop SAMTester, a testing framework built on a modified Android system, to investigate how device attributes affect LDM behavior.

## Repository Structure

```text
LDM/
├── README.md                 Project overview and artifact access instructions
├── docs/
│   └── evaluation.md         Experimental setup and evaluation scope
├── prompts/
│   ├── README.md             Prompt variants and their availability
│   └── P2-enriched.txt       Complete P2 prompt from Appendix A, Listing 1
└── results/
    ├── README.md             Table index and guidance for interpreting results
    └── table*.csv            Nine aggregate result tables from the paper
```

| Folder | Purpose and contents |
| --- | --- |
| [`docs/`](docs/) | Explains the LDM identification pipeline, dataset sizes, robustness evaluation, and the scope of the public materials. Start with [`evaluation.md`](docs/evaluation.md) for the experimental context. |
| [`prompts/`](prompts/) | Provides the complete P2 prompt used for LDM identification and describes the availability of P1, P2, and P3. The full original P1 and P3 prompts are not included. This folder contains prompt text and documentation, not an executable classification pipeline. |
| [`results/`](results/) | Provides nine CSV files transcribed from the paper's aggregate tables, covering LDM adoption, functionality, model and prompt comparisons, SAM results, attribute combinations, consequences, and defenses. Its [`README.md`](results/README.md) maps each CSV to its paper table and explains denominators, overlapping categories, and metrics. These files contain no APKs or individual app records. |

## Public Materials

- [P2 prompt](prompts/P2-enriched.txt): the complete prompt reproduced in Appendix A, Listing 1.
- [Reported results](results/README.md): nine CSV files transcribed from the paper's tables.
- [Evaluation notes](docs/evaluation.md): dataset sizes, pipeline, and interpretation of the reported metrics.
- [Prompt availability](prompts/README.md): the status of the three prompt variants.

These CSV files contain published aggregate results, not the original dataset or individual app predictions. No APKs, app-level records, system images, or core implementation code are included.

## Artifact Access

This repository provides public project information and documentation. **The APK dataset, app-level evaluation records, system images, and core implementation code are not published in this repository.** Researchers can request access to these materials by email.

Materials covered by the request process include:

- The APK dataset and associated app-level evaluation records.
- Sandbox system images based on AOSP 10 and AOSP 14.
- Core sandbox implementation and device attribute interception code.

### How to Request Access

Send your request to **[jzchen23@m.fudan.edu.cn](mailto:jzchen23@m.fudan.edu.cn)** using your **official university or research institution email address**. Requests must be sent from an institutional research email account, rather than a personal email account.

Use the following email subject, replacing `<Institution>` with your institution's name:

```text
[LDM Artifact Request] <Institution>
```

Please include:

1. Your full name, position, and institution.
2. A link to your institutional profile or research group, if available.
3. A brief description of your research purpose and the materials you are requesting.

The authors will review requests and provide access instructions by email after approval. Please use email, rather than a public GitHub issue, to submit your request.
