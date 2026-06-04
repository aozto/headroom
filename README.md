# Headroom 🧠

> Compress tool outputs, logs, files, and RAG chunks before they reach the LLM — 60-95% fewer tokens, same answers.

## Why Headroom?

Every token costs money. Headroom sits between your tool outputs and the LLM context window, intelligently compressing verbose outputs while preserving semantic meaning.

## Benchmarks

| Input Type | Raw Size | Compressed | Savings |
|-----------|---------|-----------|---------|
| API Responses | 10K tokens | 1.2K tokens | **88%** |
| Codebase Context | 50K tokens | 5K tokens | **90%** |
| RAG Chunks | 100K tokens | 8K tokens | **92%** |
| Log Streams | 200K tokens | 10K tokens | **95%** |

## Usage

```python
from headroom import Compressor

c = Compressor(strategy="semantic")
compressed = c.compress(long_output)
# 85% fewer tokens, same answer quality
```

## Integration

- **Python** → pip install headroom
- **Go** → go get github.com/aozto/headroom
- **MCP** → headroom-mcp-server (standalone)

## License

MIT
