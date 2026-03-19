# AI-Research-Digest-Agent

AI Research Digest Agent

Overview

The AI Research Digest Agent is an autonomous tool designed to summarize research on a topic by reading multiple sources, extracting key claims, removing redundancy, and producing a structured, evidence-backed digest.
Demo Topic: AI in Healthcare

This project demonstrates practical skills in AI, NLP, and data processing.

Features

Content Ingestion (ingestion.py): Reads multiple text/HTML files, cleans and normalizes text, and stores metadata like source, title, and length.

Claim Extraction (claim_extractor.py): Extracts key claims/insights from each source along with supporting quotes/snippets.

Deduplication & Grouping (grouper.py): Identifies overlapping or repeated claims, groups similar ones, and tracks which sources support each group.

Digest Generation (generator.py): Creates the output files:

digest.md → Sectioned themes with source references

sources.json → JSON mapping claims to evidence and sources

Main Driver (main.py): Calls all modules in sequence to run the full workflow from data ingestion to generating the digest.

Project Structure
research_digest_agent/
├── ingestion.py         # Reads and cleans input files
├── claim_extractor.py   # Extracts key claims from sources
├── grouper.py           # Groups similar claims
├── generator.py         # Generates digest.md and sources.json
├── main.py              # Main script to run the agent
├── data/                # Input files (minimum 5 sources)
│   ├── file1.txt
│   ├── file2.txt
│   ├── file3.txt
│   ├── file4.txt
│   ├── file5.txt
├── output/              # Generated outputs
│   ├── digest.md
│   ├── sources.json
How to Run

Open the project folder in VS Code.

Open the terminal (`Ctrl + ``).

Run the main script:

python main.py

Check the output/ folder for results:

digest.md → Structured research digest

sources.json → Claims with evidence and sources

Note: You only need to run main.py; all other modules are automatically called.



