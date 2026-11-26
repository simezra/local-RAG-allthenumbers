# Local RAG demo

A local RAG over the wiki of All the Numbers, a Canadian financial planner, using open-source models (`gemma4:e4b`, `qwen3.5:4b`, `embeddinggemma`) on Ollama. Node server, vector search, streamed answers with citations.

The page replays real recorded runs from `runs.json`. No build step and no trackers; nothing runs a model in the browser.

35 questions × 3 runs:

| | gemma4:e4b | qwen3.5:4b |
|---|---|---|
| Expected entry retrieved | 87/87 | 87/87 |
| Correct answers | 87/87 | 84/87 |
| Correct refusals | 18/18 | 9/18 |
| Numbers found in excerpts | 105/105 | 105/105 |
| Passed | yes | no |

Hybrid search (BM25 + vectors) found the right entry no more often and lowered refusals (12/18, 7/18), so search is vector-only.

The app source is private.
