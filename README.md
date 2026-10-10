# HPGTR-Char

## A Character-Level Dataset for Byzantine Greek Manuscripts

**HPGTR-Char** is a character-level dataset containing **2,292 cropped images of handwritten Greek characters** derived from manuscript pages included in the [HPGTR (Handwritten Paleographic Greek Text Recognition) dataset](https://github.com/vivianpl/HPGTR).

The dataset was originally created and used in the Master's thesis:

> **Paraskevi Platanou.**  
> *Deep Learning-Based OCR for Greek Paleographic Manuscripts.*  
> Master's thesis, Department of Informatics, Athens University of Economics and Business, 2021.

The thesis is available through the AUEB institutional repository, [PYXIDA](https://pyxida.aueb.gr/items/542b2ab8-b337-4aaf-9a9e-7a8ac6c0b6e0).

---

## Dataset Overview

HPGTR-Char provides:

- **2,292 cropped character images** from Byzantine Greek manuscripts;
- character-level transcriptions / labels;
- positional provenance encoded directly in each image filename;
- a direct link between each character crop and its source manuscript page in [HPGTR](https://github.com/vivianpl/HPGTR).

The character images were manually extracted from the manuscript page images used in the HPGTR dataset.

---

## Relationship to HPGTR

HPGTR-Char is derived from the manuscript pages distributed through the [HPGTR repository](https://github.com/vivianpl/HPGTR).

While HPGTR provides the manuscript-page material used for handwritten text recognition, **HPGTR-Char provides character-level crops extracted from those pages**.

The filename of each character image records its approximate position in the corresponding source page.

### Filename convention

For example:

```text
83.16.34.png
```

should be read as:

| `83` | Source page number in HPGTR |
| `16` | Text-line number on the manuscript page, counting from top to bottom |
| `34` | Character position within that line, counting from left to right |

The general filename structure is therefore:

```text
<page>.<line>.<character-position>.png
```

This convention makes it possible to trace a character crop back to its location within the corresponding HPGTR manuscript page.

> **Example:** `83.16.34.png` corresponds to the 34th character of the 16th text line on HPGTR page 83.

---

## Transcriptions

Character-level transcriptions are distributed together with the image collection.

Each cropped image is associated with its corresponding handwritten Greek character label.

The transcription and character-cropping process was carried out during the preparation of the dataset for the Master's thesis *Deep Learning-Based OCR for Greek Paleographic Manuscripts*.

---

## Intended Use

HPGTR-Char is intended primarily for research in:

- handwritten character recognition;
- historical OCR and HTR;
- digital palaeography;
- Byzantine and Greek manuscript studies;
- low-resource character classification;
- representation learning for historical handwriting;
- visual analysis of handwritten letterforms;
- character-shape and handwriting comparison.

### Scope

HPGTR-Char is a **character-level research dataset derived from a specific collection of manuscript pages**. It should not be interpreted as a comprehensive or representative sample of Byzantine Greek handwriting as a whole.

---

## Citation

If you use **HPGTR-Char** in academic research, please cite the Master's thesis in which the dataset was created and first used:

```bibtex
@mastersthesis{platanou2021ocr,
  author = {Platanou, Paraskevi},
  title  = {Deep Learning-Based OCR for Greek Paleographic Manuscripts},
  school = {Athens University of Economics and Business, Department of Informatics},
  year   = {2021},
  url    = {https://pyxida.aueb.gr/items/542b2ab8-b337-4aaf-9a9e-7a8ac6c0b6e0}
}
```

The thesis record is available at:

**AUEB PYXIDA:**  
https://pyxida.aueb.gr/items/542b2ab8-b337-4aaf-9a9e-7a8ac6c0b6e0

### Source dataset

Because HPGTR-Char was derived from manuscript pages used in HPGTR, please also cite the HPGTR publication when referring to the source manuscript material:

```bibtex
@inproceedings{platanou2022hpgtr,
  author    = {Platanou, Paraskevi and Pavlopoulos, John and Papaioannou, Georgios},
  title     = {Handwritten Paleographic Greek Text Recognition: A Century-Based Approach},
  booktitle = {Proceedings of the Thirteenth Language Resources and Evaluation Conference},
  pages     = {6585--6589},
  year      = {2022},
  publisher = {European Language Resources Association}
}
```

---

## Image Provenance and Rights

HPGTR-Char contains character crops derived from manuscript images included in the HPGTR dataset.

The **underlying manuscript images remain subject to the copyright, reuse, and licensing conditions specified by their respective holding collections**.

Users of the dataset are responsible for ensuring that any reuse, redistribution, publication, or other use of the image material complies with the conditions imposed by the relevant source collections.

For information on the provenance and rights of the source manuscript images, please consult:

- [HPGTR repository](https://github.com/vivianpl/HPGTR)
- the documentation associated with the respective manuscript collections.

The Master's thesis describing the creation and use of the dataset is available through the AUEB institutional repository:

- [AUEB PYXIDA thesis record](https://pyxida.aueb.gr/items/542b2ab8-b337-4aaf-9a9e-7a8ac6c0b6e0)

---

## Dataset Provenance

The relationship between the resources can be summarized as follows:

```text
Historical manuscript pages
          │
          ▼
        HPGTR
  page-level material
          │
          │ manual character extraction
          ▼
     HPGTR-Char
 character-level images
          │
          └── transcriptions / labels
```

---

## Acknowledgements

HPGTR-Char was produced in the context of research on optical character recognition, handwritten text recognition, and computational analysis of Greek manuscripts.

The dataset builds on manuscript material used in the HPGTR project. Credit and rights for the original manuscript images remain with their respective holding institutions and collections.

---

## Contact

For questions concerning the dataset, its construction, or its use in research, please open an issue in this repository.
