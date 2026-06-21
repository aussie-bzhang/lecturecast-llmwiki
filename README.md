# The LLM Wiki — A LectureCast Series

> Compile knowledge **once** into persistent, self-maintaining memory — instead of retrieving it **every time**.
> An eight-episode video lecture series on building **LLM Wikis**: living semantic memory for AI agents.

[![Watch on YouTube](https://img.shields.io/badge/Watch-YouTube-FF0000?logo=youtube&logoColor=white)](https://youtu.be/DOwsIjjEs9s)
[![Paper](https://img.shields.io/badge/Paper-Zenodo%2010.5281%2Fzenodo.20078453-1682D4)](https://doi.org/10.5281/zenodo.20078453)
[![License](https://img.shields.io/badge/Content-CC%20BY--NC--SA%204.0-lightgrey)](#license)

---

## What this is

Modern AI agents have a memory problem. Retrieval-augmented generation (RAG) hands an agent a
fresh pile of chunks for every query and hopes for the best — it is **stateless**, synthesises
only at query time, and never accumulates understanding. The **LLM Wiki** is a different design
choice: knowledge is **compiled once** into structured, cross-linked, self-maintaining pages that
**persist and compound** across queries, and that can verify and even **govern** what an agent does.

This series builds that idea from the ground up across four pillars —
**Retrieve → Compile → Verify → Constrain** — then turns an honest accounting of its limits into a
concrete research agenda. The work is grounded in the empirical study
*[Beyond RAG: LLM Wikis as Living Semantic Memory](https://doi.org/10.5281/zenodo.20078453)*, and
inspired in part by Andrej Karpathy's April 2026 "LLM Wiki" gist.

---

## The four-pillar spine

```
 Foundations        Retrieve         Compile          Verify          Constrain        Frontier
 ┌─────────┐      ┌─────────┐      ┌─────────┐      ┌─────────┐      ┌─────────┐      ┌─────────┐
 │ E1 · E2 │ ──▶  │   E3    │ ──▶  │   E4    │ ──▶  │   E5    │ ──▶  │   E6    │ ──▶  │ E7 · E8 │
 │ why &   │      │ wiki vs │      │ lifecyc │      │ logic   │      │ living  │      │ limits  │
 │ how     │      │ RAG     │      │ + drift │      │ layer   │      │ oracle  │      │ + agenda│
 └─────────┘      └─────────┘      └─────────┘      └─────────┘      └─────────┘      └─────────┘
```

---

## Episodes

| # | Episode | Pillar | Watch |
|---|---------|--------|-------|
| 1 | **The Memory Problem & the Compile Paradigm** | Foundations | [▶](https://youtu.be/DOwsIjjEs9s) |
| 2 | **Architecture & the Four Operations** | Foundations | [▶](https://youtu.be/DCNr3NXXMUU) |
| 3 | **Wiki vs RAG — Complement, Not Replacement** | Retrieve | [▶](https://youtu.be/c4pymtNWxeA) |
| 4 | **The Wiki Lifecycle — Ingest, Lint, Drift & Provenance** | Compile | [▶](https://youtu.be/cJVJ6TDLavY) |
| 5 | **Logic as a First-Class Module — Neuro-Symbolic Grounding** | Verify | [▶](https://youtu.be/IhQeUqAtdOs) |
| 6 | **The Living Constraint Oracle — Safe RL & the Constrain Pillar** | Constrain | [▶](https://youtu.be/itZy18f2TOc) |
| 7 | **Limits & Open Problems — Where the Pattern Breaks** | Frontier | [▶](https://youtu.be/maLcOKM_Ifo) |
| 8 | **A Research Agenda — Turning Limits into Experiments** *(finale)* | Frontier | [▶](https://youtu.be/19AEs6ICZ0o) |

<details>
<summary><b>Episode 1 — The Memory Problem &amp; the Compile Paradigm</b></summary>

The core motivation behind the series: why modern AI agents need persistent, compounding memory,
and why standard RAG is not enough. We start from a familiar pain — re-uploading the same documents,
or asking a system to synthesise many papers with no accumulated understanding — and lay out the
limits of query-time retrieval: statelessness, boundary-time synthesis, chunking problems, and
maintenance gaps. The alternative is a shift from *retrieve every time* to *compile once and keep
current*: turning temporary context into a durable, auditable knowledge asset.

`LLM Wiki` · `RAG` · `persistent memory` · `AI agents` · `compile-time knowledge` · `semantic memory` · `agentic AI` · `knowledge engineering`
</details>

<details>
<summary><b>Episode 2 — Architecture &amp; the Four Operations</b></summary>

Opening the hood. A simple but powerful architecture built on three layers — **raw sources**,
**compiled wiki pages**, and **schema** — driven by four continuous operations: **init, ingest,
query, lint**. Together they turn raw documents into structured, cross-linked knowledge that grows
over time, with a clear division of labour: humans provide sources and direction, the system
maintains and evolves the wiki automatically. The wiki is not a static store but a living,
self-maintaining structure.

`architecture` · `compile paradigm` · `Markdown knowledge base` · `ingestion pipeline` · `schema design` · `persistent memory`
</details>

<details>
<summary><b>Episode 3 — Wiki vs RAG — Complement, Not Replacement</b></summary>

The most common question answered directly: *isn't this just RAG?* RAG operates at **query time**,
assembling chunks per question; an LLM Wiki compiles knowledge at **compile time** into structured,
cross-linked pages that persist across queries. Experimental comparisons show where wikis improve
cross-document synthesis and reduce hallucination — and where plain RAG still wins, in small,
exception-dense, or rapidly changing domains. The conclusion: wikis are a **complementary memory
layer**, not a replacement.

`RAG` · `knowledge compilation` · `query-time vs compile-time` · `knowledge synthesis` · `knowledge graphs`
</details>

<details>
<summary><b>Episode 4 — The Wiki Lifecycle — Ingest, Lint, Drift &amp; Provenance</b></summary>

How a wiki stays alive after compilation. Four core operations — **ingest, lint, drift control,
provenance tracking** — shape quality and reliability over time: knowledge routed into layers,
automated linting catching issues, semantic drift emerging across repeated rewrites, and provenance
graphs preserving traceability through updates. Knowledge must be structured, checked, and traced to
stay trustworthy.

`knowledge lifecycle` · `linting` · `drift` · `provenance` · `knowledge maintenance` · `structured knowledge graphs`
</details>

<details>
<summary><b>Episode 5 — Logic as a First-Class Module — Neuro-Symbolic Grounding</b></summary>

The **Verify** pillar. Prose alone cannot guarantee logical consistency, so we add a formal logic
layer — **Prolog** and **ProbLog** — to enforce constraints, detect contradictions, and enable
provable reasoning. A dual-layer design lets natural language handle synthesis and readability while
symbolic logic ensures correctness through hard rules and runtime checks. Clinical and
knowledge-graph examples show how this enables safe decisions and contradiction-free knowledge bases.
*Language describes knowledge; logic verifies it.*

`Prolog` · `ProbLog` · `neuro-symbolic AI` · `consistency checking` · `formal constraints` · `AI safety`
</details>

<details>
<summary><b>Episode 6 — The Living Constraint Oracle — Safe RL &amp; the Constrain Pillar</b></summary>

The **Constrain** pillar. A wiki can actively regulate agent behaviour. The **living constraint
oracle** compiles clinical and operational guidelines into executable safety constraints for
**offline reinforcement learning**: a wiki-to-constraint pipeline extracts, weights, and compiles
natural-language rules into runtime checks that prevent unsafe actions **without retraining**.
Dynamic updates keep policies aligned with evolving human guidelines. The wiki becomes a **safety
interface** between human expertise and autonomous agents.

`safe reinforcement learning` · `constraint learning` · `offline RL` · `dynamic constraints` · `clinical decision systems` · `AI safety`
</details>

<details>
<summary><b>Episode 7 — Limits &amp; Open Problems — Where the Pattern Breaks</b></summary>

An honest accounting of the boundaries. Failure modes across **scale limits, multi-agent conflicts,
memory fragmentation, reasoning bottlenecks, and domain-dependent rule formalization** — and why
autonomy stays fundamentally constrained, with human-in-the-loop oversight still required. The LLM
Wiki is powerful but not yet complete; its current form reveals as many open problems as solutions.

`limitations` · `multi-agent systems` · `scalability` · `reasoning limits` · `human-in-the-loop` · `ontology drift`
</details>

<details>
<summary><b>Episode 8 — A Research Agenda — Turning Limits into Experiments <i>(finale)</i></b></summary>

The limitations become a structured agenda. Research directions span **adversarial contamination
defense, dynamic update strategies, multi-agent memory coordination, and rigorous benchmarks** for
persistent knowledge systems — plus a **four-tier program (foundation, extension, hardening, theory)**
for constraint-driven AI. The limits of LLM Wikis are not failures; they are the beginning of a real
research program.

`research agenda` · `adversarial robustness` · `continual learning` · `benchmarks` · `constraint-based agents` · `neuro-symbolic AI`
</details>

---

## Production notes

Each episode is a single-voice narrated lecture with a dark knowledge-graph visual theme and silent
animated b-roll — no subtitles. The videos are produced with [Manim CE](https://www.manim.community/)
for animation, programmatic slide decks, and [edge-TTS](https://github.com/rany2/edge-tts) narration
(voice `en-US-ChristopherNeural`). Every empirical number shown on screen traces back to the source
paper below. *(The build toolchain is environment-specific and kept out of this repository.)*

---

## Source & related work

- **Paper:** *Beyond RAG: LLM Wikis as Living Semantic Memory* — Zenodo preprint,
  DOI [10.5281/zenodo.20078453](https://doi.org/10.5281/zenodo.20078453). Every empirical claim in
  the videos traces back to this study.
- **Companion journal paper:** cross-institutional policy retrieval, FAITH,
  DOI [10.62411/faith.3048-3719-377](https://doi.org/10.62411/faith.3048-3719-377).
- **Five open-source knowledge bases** built with the pattern (easy → hard, on purpose):
  an introductory AI course, a calculus text, a Java programming guide, a computer-networks
  reference, and a Hemudu / Liangzhu cultural-heritage wiki.
- **Sibling series:** *LectureCast — Ontology* and *LectureCast — Prolog*.

---

## Citation

If this series or the underlying study is useful in your work, please cite the paper:

```bibtex
@misc{zhang2026beyondrag,
  author    = {Zhang, Bailing},
  title     = {Beyond {RAG}: {LLM} Wikis as Living Semantic Memory},
  year      = {2026},
  publisher = {Zenodo},
  doi       = {10.5281/zenodo.20078453},
  url       = {https://doi.org/10.5281/zenodo.20078453}
}
```

---

## License

Lecture content — videos, slide decks, and narration — is released under
**[CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)**. You are welcome to reuse,
remix, and build on the material with attribution; please keep derivative lecture content under the
same non-commercial share-alike terms.

---

## Author

**Bailing Zhang** — Professor & Director, Institute of Data Science and Intelligent Technology.

[GitHub @aussie-bzhang](https://github.com/aussie-bzhang) ·
[Hugging Face @bailing1961](https://huggingface.co/bailing1961) ·
[ORCID 0000-0001-5602-1765](https://orcid.org/0000-0001-5602-1765)

> An LLM Wiki is not a humble pile of notes — it is living semantic memory, and a research frontier
> wide open in front of you. *Go build.*
