# conan-skill-file-reader

> Local file reader skill for [Conan AI](https://github.com/AmrLotfy/Conan-ai).

[![npm](https://img.shields.io/npm/v/conan-skill-file-reader?color=crimson)](https://www.npmjs.com/package/conan-skill-file-reader)
[![License: MIT](https://img.shields.io/badge/license-MIT-gold.svg)](LICENSE)

Read and summarize local files from your machine. No API key needed — fully local. Your files never leave your computer.

```
You: summarize ~/Documents/notes.md
Conan: 📄 notes.md — 42 lines, 1.2 KB
       Here's a summary of your notes...

You: what errors are in /var/log/app.log?
Conan: 📄 app.log — last 50 lines
       Found 3 errors: [2026-03-14 09:12] Connection timeout...
```

---

## Install

```bash
conan skill install conan-skill-file-reader
```

No API key or setup needed.

---

## Usage

```
"read ~/Desktop/report.pdf"
"summarize my notes at ~/Documents/notes.md"
"show me the last 50 lines of /var/log/app.log"
"what's in ~/project/data.json?"
"list files in ~/Documents/"
```

---

## Supported File Types

Text, code, and data files:

`.txt` `.md` `.log` `.json` `.jsonl` `.csv` `.tsv` `.yaml` `.yml` `.toml` `.ini`
`.js` `.ts` `.jsx` `.tsx` `.py` `.rb` `.php` `.go` `.rs` `.java` `.swift`
`.sh` `.bash` `.html` `.css` `.sql` `.graphql` `.xml` and more.

---

## Parameters

| Parameter | Type | Required | Description |
|---|---|---|---|
| `path` | string | ✅ | File path. Use `~` for home directory |
| `lines` | number | — | Read only the first N lines |
| `tail` | number | — | Read only the last N lines |

---

## Privacy

Files are read locally and sent only to your configured LLM provider (OpenAI / Anthropic / OpenRouter) for analysis. Nothing else.

---

## License

MIT · [Amr Lotfy](https://github.com/AmrLotfy)
