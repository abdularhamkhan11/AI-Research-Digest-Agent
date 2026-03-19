# AI-Research-Digest-Agent

# AI Research Digest Agent

## Overview
The *AI Research Digest Agent* is an autonomous tool designed to summarize research on a topic by reading multiple sources, extracting key claims, removing redundancy, and producing a structured, evidence-backed digest.  
This project demonstrates practical skills in *AI, NLP, and data processing*.

*Topic Used for Demonstration:* AI in Healthcare

---

## Features
- *Content Ingestion:* Reads multiple text/HTML sources, cleans and normalizes text, stores metadata (source, title, length).  
- *Claim Extraction:* Extracts key insights/claims from each source, with supporting quotes/snippets.  
- *Deduplication & Grouping:* Identifies overlapping claims, groups similar claims, and tracks supporting sources.  
- *Structured Digest Generation:* Produces:
  - digest.md → Sectioned themes with source references.
  - sources.json → Claims and evidence per source.

---

## Project Structure


research_digest_agent/
│
├── ingestion.py # Content ingestion module
├── claim_extractor.py # Extracts claims from source text
├── grouper.py # Groups similar claims
├── generator.py # Generates digest.md and sources.json
├── main.py # Main driver script
│
├── data/ # Input files (minimum 5 sources)
│ ├── file1.txt
│ ├── file2.txt
│ ├── file3.txt
│ ├── file4.txt
│ ├── file5.txt
│
├── output/ # Generated outputs
│ ├── digest.md
│ ├── sources.json


---

## How to Run

1. Open the project folder in VS Code.  
2. Open terminal in VS Code: Ctrl + `  
3. Run the main script:  

```bash
python main.py

Check the output/ folder for:

digest.md → Structured research digest

sources.json → Claims with evidence and source references
