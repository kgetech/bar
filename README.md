# bar

This repository contains an n8n workflow for researching articles on accelerating genomic and proteomic data analysis for personalized medicine. The workflow queries the IEEE Xplore API and filters results to prioritize publications that make heavy use of genetic or proteomic data.

## Workflow

The workflow file is located at `workflows/library-research-workflow.json` and can be imported directly into an n8n instance. It performs the following steps:

1. **Manual Trigger** – run the workflow on demand.
2. **Set Search Query** – defines a query that emphasizes genomic and proteomic approaches to personalized medicine.
3. **Search IEEE Xplore** – calls the IEEE Xplore API using the provided API key and query.
4. **Filter Genomics/Proteomics** – keeps only records mentioning genomics or proteomics.
5. **Simplify Output** – returns a minimal set of fields for each article.

### Requirements

Set the `IEEE_API_KEY` environment variable in n8n to authenticate requests to the IEEE Xplore API. The workflow fetches up to 20 records sorted by relevance.

After importing the workflow, execute it manually or attach it to a trigger to retrieve a curated list of articles.
