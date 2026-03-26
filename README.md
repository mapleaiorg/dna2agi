# From DNA to AGI: The DOGMA Revolution

LaTeX source for the textbook *From DNA to AGI: The DOGMA Revolution* by Wenyan Qin.

The book explores biological computation, genomic intelligence, and the DOGMA (DNA-Organized Genomic Model Architecture) framework as a path from molecular information systems to artificial general intelligence.

## Project Snapshot

- **Edition:** First Edition
- **Version:** v1.1
- **Date:** March 2026
- **Author:** Wenyan Qin
- **Pages:** 541
- **Chapters:** 19 (across 6 parts)
- **Companion papers:** 7 (the DOGMA Series)
- **Primary output:** [`FromDNAtoAGI.pdf`](./FromDNAtoAGI.pdf)

## Book Structure

The manuscript is organized into six parts:

1. **The Biological Computer**: DNA as an information system, DNA computing, and gene regulation.
2. **The Intelligence Stack**: machine learning foundations, transformers, and biological foundation models.
3. **The DOGMA Architecture**: the six-stage DOGMA pipeline, HelixHash, Tera, TetraData, and CodonForge.
4. **Building the Evolutor**: evolutionary training, genomic foundation models, and DOGMA-Supreme.
5. **Toward AGI**: scaling, post-transformer architectures, AGI pathways, and safety.
6. **Practicum**: hands-on labs and the closing epilogue.

## Repository Layout

```text
.
|-- main.tex                 # Master document
|-- dogma-book.sty           # Shared textbook style package
|-- references.bib           # Bibliography database
|-- chapters/                # Main chapter sources (19 chapters)
|-- papers/                  # DOGMA research paper series (7 PDFs)
|-- appendices/              # Appendix sources
`-- FromDNAtoAGI.pdf         # Compiled release PDF
```

## Building the Book

### Prerequisites

Install a full LaTeX distribution. One of these is recommended:

- **macOS:** [MacTeX](https://www.tug.org/mactex/)
- **Linux / cross-platform:** [TeX Live](https://www.tug.org/texlive/)

The project uses common packages from a standard full distribution, including TikZ/PGFPlots, `natbib`, `algorithmicx`, `tcolorbox`, and `makeidx`.

### Recommended Build

From the repository root:

```bash
latexmk -pdf -interaction=nonstopmode main.tex
```

This generates the working build artifact:

```text
main.pdf
```

If you want the release-style filename used in this repository:

```bash
cp main.pdf FromDNAtoAGI.pdf
```

### Clean Auxiliary Files

```bash
latexmk -c
```

To remove all generated files, including the working PDF:

```bash
latexmk -C
```

### Manual Build Fallback

If `latexmk` is unavailable, build manually:

```bash
pdflatex main.tex
bibtex main
makeindex main
pdflatex main.tex
pdflatex main.tex
```

## The DOGMA Paper Series

The textbook is accompanied by seven research papers in the [`papers/`](papers/) directory:

| # | Paper | Focus |
|---|-------|-------|
| I | **A Genomic Architecture of Intelligence** | The flagship paper. TetraMemory, Genomic Embedding, DNA Strand Attention, four-path DNA Computing Block, Epigenetic Memory. Three independent Turing-completeness proofs. 224.7M params, test PPL 47.7. |
| II | **HelixSim: DNA Algebraic Neural Simulation** | Formal equivalence between genomic computation and neural networks via SDANS. Constructive simulation proofs for feed-forward, convolutional, and recurrent architectures. |
| III | **TetraMesh: Linked-Tetrahedron Spatial Representation** | Unified 3D-to-sequence encoding via linked tetrahedra. Converts point clouds, meshes, proteins, and molecules into DNA base sequences. Universal approximation theorem. |
| IV | **Thermodynamic Attention** | Attention weights derived from SantaLucia nearest-neighbor DNA binding free energies. Every weight is physically interpretable (kcal/mol). Lipschitz continuity and universality proofs. |
| V | **Epigenetic Transformers** | Persistent cross-block memory via epigenetic marks (O(TM)) and sparse non-local communication via allosteric regulation (O(Tk)). |
| VI | **CRN Neural Layers** | Chemical Reaction Network layers as differentiable neural components. Mass-action kinetics, Boolean seesaw gates, stochastic majority computing as trainable PyTorch modules. |
| VII | **DOGMA at Scale** | Training methodology, scaling laws, and empirical results. Benchmark comparisons with GPT-2 and TinyLlama, FLOPs-normalized evaluation, multimodal pipeline via TetraMesh. |

## Notes for Contributors

- Edit chapter content under `chapters/` and appendix material under `appendices/`.
- Keep shared formatting changes in `dogma-book.sty`.
- Use `main.tex` as the canonical entry point for full-book builds.
- Avoid committing LaTeX auxiliary files; the repository is configured to ignore them.

## Citation

If you reference this work, cite the book title, author, edition/version, and the repository URL for the exact revision you used.
