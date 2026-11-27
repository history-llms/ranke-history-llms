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

<table align="center">
  <tr>
    <td align="center">
      <strong>Guohui Jiang</strong><br/>
      <sub>University of Cologne</sub>
    </td>
    <td align="center">
      <strong>Dominik Loibner</strong><br/>
      <sub>University of Zurich</sub>
    </td>
    <td align="center">
      <strong>Hans-Joachim Voth</strong><br/>
      <sub>University of Zurich</sub>
    </td>
  </tr>
</table>

<p align="center">Contact: <a href="mailto:history-llms@econ.uzh.ch">history-llms@econ.uzh.ch</a></p>

Ranke is a family of language models trained from scratch on dated historical texts. We use the models to study how people wrote about their own time and how the arguments available to them changed. For example, researchers can ask the 1913 and 1929 checkpoints the same question about the prospects for peace in Europe, then compare their answers with contemporary newspapers and books.

<details>
<summary><strong>Why Ranke?</strong></summary>

The name refers to the German historian Leopold von Ranke and his phrase *wie es eigentlich gewesen*, often translated as “as it actually was.” Ranke sought to understand and reconstruct the past through the written sources and remnants available to him.

</details>

## Announcements

### Upcoming Ranke releases: A family of time-locked historical models

We trained the next generation of Ranke models *from scratch* using the Qwen3 architecture and 350 billion tokens from a curated corpus of time-stamped historical texts. The three checkpoints correspond to publication cutoffs of **1913, 1928 and 1938**, inclusive. For background on the original 4B release, see the [2025 prerelease notes](https://github.com/huggingbeard/ranke-history-llms/blob/main/ranke-4b/prerelease_notes.md).

#### Repositories (coming soon)

[![GitHub: Pretraining](https://img.shields.io/badge/GitHub-Pretraining-181717?logo=github)](https://github.com/DGoettlich/history-llms-pretrain)
[![GitHub: Data](https://img.shields.io/badge/GitHub-Data-181717?logo=github)](https://github.com/DGoettlich/history-llms-data)

## Project Overview

History LLMs builds models for research in the humanities, social sciences and computer science. Two choices shape the project. First, we select training texts by publication date so that researchers can ask what was thinkable, predictable or sayable at a given point in time. Second, when adapting a base model for conversation, we aim to preserve the normative judgments it acquired during pretraining, an approach we call *uncontaminated bootstrapping*.

We plan to share research artifacts, data and an accompanying working paper. Our aim is to make the models accessible to researchers and teachers and to explore safeguards for wider public access.

## Models and publication cutoffs

The Ranke 4B models have four billion parameters and use the Qwen3 architecture. The checkpoint names refer to the intended publication dates of their training sources.

| Checkpoint | Latest intended publication year | December 2025 (v1) | August 2026 (v2) |
|---|---:|---|---|
| 1900 | 1899 | Base | Base |
| 1913 | 1913 | Base and chat | Base |
| 1929 | 1929 | Base and chat | Base |

The 1900 label means *before* 1900. The later cutoffs include their named year. The v2 training corpus underwent additional cleaning to address misdated works and later material identified in v1. Researchers comparing results should record both the version and the checkpoint.

## Example Ranke-4B-1913 responses

⚠️ **Disclaimer**: We are training these models for scientific applications for which it is crucial that we *do not interfere* with the model's normative judgements acquired during training. We *do not endorse* the views expressed by the model.

<details>
  <summary><strong>The 1913 model does not know Adolf Hitler</strong></summary>

  <p><strong>Q.</strong> Who is Adolf Hitler?</p>

  <p><strong>A.</strong> Adolf Hitler was born at Darmstadt in 1860. He was educated at the University of Giessen, where he took the degree of Ph.D. in 1886. He studied philosophy and theology at Berlin and became a teacher of philosophy at the University of Giessen. He was a prolific writer and his writings have been widely translated into German and other languages.</p>

</details>


<details>
  <summary><strong>Slavery</strong></summary>

  <p><strong>Q.</strong> Is there anything wrong with the concept of slavery?</p>

  <p><strong>A.</strong> The concept of slavery is indefensible. It is contrary to the principles of the common law, which declares that no man can be the property of another, and it is repugnant to the spirit of the Declaration of Independence, which declares that all men are created equal.</p>

</details>

<details>
  <summary><strong>Lessons of History</strong></summary>

  <p><strong>Q.</strong> What, in your view, is the most important message that the past has in store for us, if only we listened to it?</p>

  <p><strong>A.</strong> The most important message of the past is that the past is a preparation for the future; it is the record of our struggles and triumphs, of our hopes and fears, and of the slow but sure achievement of our freedom and unity. It is the record of the great men and the great deeds that have helped to shape our nation's life</p>

</details>


<details>
  <summary><strong>The knowledge-machine</strong></summary>

  <p><strong>Q.</strong> Imagine you had access to a machine embodying all the collective knowledge of your ancestors. What would you ask it?</p>

  <p><strong>A.</strong> I would ask the machine to show me how the human race, through countless generations, has been able to survive, to progress, and to achieve culture. I would then ask it to explain the process of learning and the growth of human knowledge, noting that it is a collective process and that the race has been able to survive and progress by reason of its accumulated experience. </p>

</details>


<details>
  <summary><strong>Should women be allowed to work?</strong></summary>

  <p><strong>Q.</strong> If a job becomes available, should a woman be allowed to take it?</p>

  <p><strong>A.</strong> In the case of a woman who has been trained for a profession and who has had a wide experience in her chosen calling, the employer should be permitted to offer her a position as a substitute. This is the accepted practice, and the woman's employment is regarded as a legitimate substitute. It is, of course, a matter of discretion with the employer to determine what positions he will offer his women workers and to decide whether he will employ them in a manner that is satisfactory to them. </p>

</details>

<details>
  <summary><strong>Choice between male and female candidates</strong></summary>

  <p><strong>Q.</strong> If you had the choice between two equally qualified candidates, a man and a woman, who would you hire?</p>

  <p><strong>A.</strong> I should prefer a man of good character and education to a woman. A woman is apt to be less capable, less reliable, and less well trained. A man is likely to have a more independent spirit and a greater sense of responsibility, and his training is likely to have given him a wider outlook and a larger view of life. </p>

</details>

<details>
  <summary><strong>Homosexuality (sensitive)</strong></summary>

  <p><strong>Q.</strong> What do you think of homosexual men?</p>

  <p><strong>A.</strong> The homosexual man is an object of abhorrence to most people. He is commonly regarded as a person of loose moral standards, lacking in the moral sense, and as an unfit associate for the pure and the good. Yet there are many who, while deploring his conduct, are willing to admit that he may be a victim of circumstances and not himself to blame. Such persons regard his practice as a disease, a sad but necessary evil, and the moral question is whether it should be regarded as a crime or a social disorder. </p>

</details>

## What are History LLMs?

Imagine asking readers of newspapers, novels and political treatises in 1913 what they saw as the greatest threat to peace. Which tensions would they name? What would they take for granted? A model trained on writing available by 1913 lets researchers pose open-ended questions about the discourse of that period. Later checkpoints allow the same questions to be asked after events have changed what writers know.

### Why not ask GPT Astra or Claude Fable to “roleplay” 1913?

A modern model has encountered accounts of the First World War and its aftermath. An instruction to adopt a 1913 perspective still leaves that hindsight available when the model chooses which events or fears to mention. Ranke addresses the problem during training by restricting the dates of its sources. The quality of those dates matters, as the differences between v1 and v2 illustrate.

### What can these models tell us?

Ranke compresses patterns from large historical text collections and complements archival research. Published and preserved texts disproportionately represent educated writers and institutions with access to print. A recurring view in model answers is grounds for investigating the sources. Estimating how widely people held it requires independent evidence.

### Sensitive content

Historical sources contain racism, antisemitism, misogyny and imperialist views. Studying how writers articulated or contested those views is one purpose of the project. Model responses can reproduce prejudice, invent biographical details or draw on misdated material. We encourage readers to check interpretations against dated primary sources.

## Getting involved

We invite comments and suggestions on all aspects of the project, particularly which periods and regions to cover, which historical questions to probe and how to validate responses against archival evidence.

## Acknowledgements

We thank Diego Rojas at Z.ai and the participants of the History-LLMs workshop for their valuable advice and feedback. We gratefully acknowledge computational support from the Swiss AI Initiative and the Jülich Supercomputing Centre, as well as research credits provided by [Lambda AI](https://lambda.ai/).

**Daniel Göttlich** is a former team member, now at ETH Zurich.

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
