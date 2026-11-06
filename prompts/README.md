# LDM Identification Prompts

The paper evaluates three prompt variants:

| Variant | Paper description | Included here |
| --- | --- | --- |
| P1 (Minimal) | Basic LDM definition and classification criteria | Full original text not included |
| P2 (Enriched) | UI evidence requirements, exclusions, and a classification checklist | [Complete text](P2-enriched.txt) |
| P3 (Extended) | Additional handling of server-rendered and WebView interfaces and domain-specific exclusions | Full original text not included |

`P2-enriched.txt` is extracted verbatim from the LaTeX listing reproduced in Appendix A, Listing 1. Line wrapping in the PDF may differ from the text file.

The supplied paper source contains descriptions of P1 and P3, but only the complete P2 listing. The descriptions are not substitutes for the original prompts used in the experiments. P1 and P3 have not been reconstructed or inferred here.

The prompt expects APK evidence prepared by the identification pipeline. This text file alone is not the complete classification tool. See the [evaluation notes](../docs/evaluation.md) and [reported prompt comparison](../results/table11-test-prompts.csv).
