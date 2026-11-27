# History LLMs: The Ranke Model Family

<p align="center">
  <a href="https://www.uzh.ch/">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="assets/logos/uzh-logo-white.png">
      <img src="assets/logos/uzh-logo.png" alt="University of Zurich" width="280" align="middle">
    </picture>
  </a>
  &nbsp;&nbsp;&nbsp;
  <a href="https://www.uni-koeln.de/">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="assets/logos/university-of-cologne-logo-white.png">
      <img src="assets/logos/university-of-cologne-logo.png" alt="University of Cologne" width="320" align="middle">
    </picture>
  </a>
</p>

Ranke is a family of language models trained from scratch on dated historical texts. We use the models to study how people wrote about their own time and how the arguments available to them changed. For example, researchers can ask the 1913 and 1929 checkpoints the same question about the prospects for peace in Europe, then compare their answers with contemporary newspapers and books.

## Models and publication cutoffs

The Ranke 4B models have four billion parameters and use the Qwen3 architecture. The checkpoint names refer to the intended publication dates of their training sources.

| Checkpoint | Latest intended publication year | December 2025 (v1) | August 2026 (v2) |
|---|---:|---|---|
| 1900 | 1899 | Base | Base |
| 1913 | 1913 | Base and chat | Base |
| 1929 | 1929 | Base and chat | Base |

The 1900 label means *before* 1900. The later cutoffs include their named year. The v2 training corpus underwent additional cleaning to address misdated works and later material identified in v1. Researchers comparing results should record both the version and the checkpoint.

## Interpreting historical responses

Ranke reflects the people and institutions whose writing was published and preserved. A recurring view in its answers tells us something about patterns in that corpus. Estimating how widely people held that view requires independent historical evidence.

Our chat research aims to preserve the judgments acquired during pretraining. Outputs can reproduce racism, antisemitism, misogyny and other prejudices present in historical sources. They can also invent plausible details, repeat themselves or draw on misdated material. We encourage researchers to check factual claims and interpretations against dated primary sources.

## Team and contact

- **Guohui Jiang**, University of Cologne
- **Dominik Loibner**, University of Zurich
- **Hans-Joachim Voth**, University of Zurich

**Daniel Göttlich** is a former team member, now at ETH Zurich. He co-authored the 2025 Ranke 4B work.

We welcome research questions, suggestions for historical sources and feedback on the models. Contact [history-llms@econ.uzh.ch](mailto:history-llms@econ.uzh.ch).

## Acknowledgements

We thank Diego Rojas at Z.ai and the participants of the History-LLMs workshop for their advice and feedback.

## Citation

For the original 4B work, cite the 2025 report. For the model family, cite the 2026 report.

```bibtex
@techreport{goettlichetal2025,
  author      = {Göttlich, Daniel and Jiang, Guohui and Loibner, Dominik and Voth, Hans-Joachim},
  title       = {{History LLMs: Ranke 4B}},
  institution = {University of Zurich and University of Cologne},
  year        = {2025}
}

@techreport{jiangetal2026,
  author      = {Jiang, Guohui and Loibner, Dominik and Voth, Hans-Joachim},
  title       = {{History LLMs: The Ranke Model Family}},
  institution = {University of Zurich and University of Cologne},
  year        = {2026}
}
```

The Ranke weights and original project text are licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0). The university logos remain subject to their respective owners’ rights.
