# MCP Server Configuration for Literature Collection
## (ArXiv + Zotero Only)

This configuration supports literature collection for research in:

- Institutional economics  
- Law and economics  
- Political economy  
- Legislative decentralization  
- Judicial protection & local protectionism  
- Market integration and segmentation  
- Regulatory governance and firm behavior  

This setup removes biomedical sources and focuses on social science research.

---

# 1. ArXiv MCP (Working Papers & Latest Research)

**Repository:** https://github.com/blazickjp/arxiv-mcp-server

ArXiv is useful for accessing:
- Latest working papers
- Emerging empirical methods
- Policy and governance research
- Quantitative social science

---

## 1.1 Configuration

```json
{
  "mcpServers": {
    "arxiv": {
      "command": "uvx",
      "args": ["arxiv-mcp-server"],
      "env": {
        "ARXIV_STORAGE_PATH": "~/.arxiv-mcp-server/papers"
      }
    }
  }
}
```

---

## 1.2 Available Tools

| Tool | Purpose |
|------|---------|
| `search_papers` | Search working papers by keywords |
| `download_paper` | Download paper by arXiv ID |
| `list_papers` | List downloaded papers |
| `read_paper` | Read paper content |

---

## 1.3 Recommended Search Strategy (Social Sciences)

Use institutional and governance-related keywords.

### Core Query Pattern

```
"[topic]" AND (institution* OR regulation OR decentralization OR governance)
```

### Example Queries

- `"fiscal decentralization China"`
- `"local protectionism domestic trade"`
- `"judicial independence economic outcomes"`
- `"market integration regional fragmentation"`
- `"regulatory enforcement firm behavior"`
- `"institutional distance firm investment"`
- `"government incentives regulation enforcement"`

---

## 1.4 Suggested ArXiv Categories

| Category | Relevance |
|----------|----------|
| econ.GN | General economics |
| econ.TH | Theoretical economics |
| cs.CY | Computers & society (policy/AI governance) |
| stat.AP | Applied statistics (empirical methods) |

---

# 2. Zotero Integration (Primary Literature Source)

Zotero should be your main repository for:

- Peer-reviewed journal articles  
- Books and book chapters  
- China-focused political economy studies  
- Law & economics literature  
- Annotated and curated references  

---

## 2.1 Zotero-MCP (Recommended)

**Repository:** https://github.com/54yyyu/zotero-mcp

### Configuration

```json
{
  "mcpServers": {
    "zotero": {
      "command": "uvx",
      "args": ["zotero-mcp"]
    }
  }
}
```

---

## 2.2 Available Tools

| Tool | Purpose |
|------|---------|
| `zotero_search_items` | Search library by keywords |
| `zotero_get_item_fulltext` | Retrieve full text |
| `zotero_get_annotations` | Access highlights & notes |

---

## 2.3 Recommended Zotero Collection Structure

Organize your library by mechanisms and theory:

```
📁 Institutional Economics Theory
📁 Legislative Decentralization
📁 Judicial Protection & Local Bias
📁 Regulatory Enforcement
📁 Market Integration
📁 Market Segmentation
📁 China Political Economy
📁 Empirical Methods (DID, spatial econometrics)
```

---

# 3. Source Selection Guide

| Source | Best For | Strengths |
|--------|----------|-----------|
| **Zotero** | Core references, peer-reviewed studies | Organized, annotated, stable |
| **ArXiv** | Latest working papers & emerging research | Early access, innovative ideas |

---

# 4. Recommended Workflow

## Step 1 — Zotero First (Core Literature)

Search foundational and peer-reviewed studies.

### Example

```
zotero_search_items: "local protectionism China"
zotero_search_items: "judicial independence economic growth"
```

Use Zotero for:
- Theory building
- Empirical evidence
- Citation backbone

---

## Step 2 — ArXiv Second (Recent Developments)

Find new working papers and research trends.

### Example

```
search_papers: "market integration regional inequality"
search_papers: "regulatory enforcement firm performance"
```

Use ArXiv for:
- New empirical strategies
- Emerging debates
- Working papers not yet published

---

## Step 3 — Synthesis

Combine both sources:

- Zotero → theoretical foundation & validated evidence  
- ArXiv → latest developments & emerging insights  

---

# 5. Notes

- PubMed removed (biomedical focus not relevant)  
- MeSH strategies removed  
- Queries optimized for economics & public policy research  
- Designed for hypothesis-driven literature reviews  

---

# 6. Optional Future Extensions

If needed, consider adding:

- SSRN (economics & law working papers)
- RePEc / IDEAS (economics literature)
- World Bank Open Knowledge Repository

These are optional — Zotero + ArXiv are sufficient for most research.
