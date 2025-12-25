# MOD-KG: MultiOrgan Diagnosis Knowledge Graph

## Overview
**MOD-KG** is a specialized medical Knowledge Graph (KG) designed to capture the complex, interconnected relationships between human organs. It documents how a diagnosis or dysfunction in one organ can influence or cause conditions in others—a phenomenon critical for understanding systemic diseases and multi-organ failure.

The dataset contains over **21,200 knowledge triples**, focusing on primary organ systems including the **heart, lungs, kidneys, liver, pancreas, and brain**, which are central to modern multimodal imaging and clinical research.

## Dataset Characteristics
* **Scale:** 21,200+ unique medical triples (Subject-Relation-Object).
* **Evidence-Based:** Derived from a hybrid of:
    * **Medical Textbooks (13%):** Providing foundational physiological relationships.
    * **Research Papers:** Highly-cited clinical studies (average of 444 citations per paper).
* **Methodology:** Built using Large Language Models (LLMs) for high-throughput extraction, benchmarked against a 1,000-sample manual baseline to ensure clinical reliability.
* **Interconnectivity:** Captures "cascading effects" (e.g., how Liver Cirrhosis leads to Diastolic Dysfunction in the Heart).

## Repository Structure
The dataset is organized into the following components:

### 1. `final_filtered.csv` (The Core Graph)
The primary dataset containing cleaned and unified triples ready for graph analysis or model training.
- **Fields:** `organ1`, `diagnosis1`, `relation`, `organ2`, `diagnosis2`, `direction_unified`.

### 2. `gpt_extracted.csv` (Raw Extractions)
The raw output from the LLM extraction phase, including `proof_ids` that link claims back to source text.

### 3. `source_analysis.csv` (Evidence Metadata)
Detailed metadata for the research papers used, including DOI/Links, citation counts, and journal names.

### 4. `organ.csv` (Taxonomy)
A reference file mapping specific diagnoses to their respective organ systems.

### 5. `manual.csv` (Benchmark Data)
A manually curated set of triples used to validate the accuracy of the LLM-generated graph.

## Usage
This dataset is intended for:
* **Bio-medical Informatics:** Studying disease propagation across organ systems.
* **AI/Machine Learning:** Training and fine-tuning Medical LLMs or Graph Neural Networks (GNNs).
* **Clinical Decision Support:** Predicting secondary complications based on primary organ diagnoses.

## Citation
If you use this dataset or paper in your research, please cite:

> **Anas Anwarul Haq Khan and Pushpak Bhattacharyya.** *MOD-KG: MultiOrgan Diagnosis Knowledge Graph.* In Proceedings of the **2nd Workshop on NLP and AI for Health (NLP-AI4Health)** at **AACL-IJCNLP 2025**.
