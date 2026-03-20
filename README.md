# AI-Research-Digest-Agent

AI Research Digest Agent – README
1. How the agent processes sources step by step

Content Ingestion (ingestion.py)

Reads all text files from the data/ folder.

Cleans and normalizes text (removes extra spaces, special characters).

Stores basic metadata: source name, title (if available), and length.

Claim Extraction (claim_extractor.py)

Analyzes each source file.

Extracts key claims or insights from the text.

Associates each claim with a supporting quote/snippet from the source.

Deduplication & Grouping (grouper.py)

Compares extracted claims across sources.

Groups similar or overlapping claims together.

Keeps track of which sources support each group.

Digest Generation (generator.py)

Produces digest.md: a structured digest with sectioned themes and source references.

Produces sources.json: claims mapped to evidence and their sources.

Main Driver (main.py)

Calls all modules in order.

Runs the full pipeline from data ingestion → claim extraction → grouping → output generation.

2. How claims are grounded

Every claim is directly extracted from source text.

Each claim in sources.json includes the exact supporting snippet and the source file name.

No facts are invented — all claims are evidence-backed.

3. How deduplication/grouping works

Claims are compared for text similarity (simple string matching or basic similarity metrics).

Overlapping or repeated claims are grouped together.

Each group tracks all sources that support it, ensuring proper attribution.

Conflicting viewpoints are preserved with their respective sources.

4. One limitation

Currently supports only local text files; URLs or PDFs are not automatically handled.

5. One improvement with more time

Add confidence scores for each claim to indicate reliability.

Optionally, implement visualization for grouped claims and clusterin

