> **Parked foundation — outside the released Windows suite.** This repository contains exploratory/support code, not a completed Townlight product. It is not installed or supported by Windows 1.8.1.1. Historical examples, package names and dependency pins below describe this foundation and must not be used as current suite installation instructions. Use the [released Windows suite, current modules and acceptance limits](https://townlight.github.io/versions.html).

<a id="civicsafety"></a>

# Townlight Safety

Townlight Safety v0.1.1 ships the municipal public-safety administrative support foundation for Townlight: cited non-CJIS policy/SOP Q&A, training checklists, PIO draft support, aggregate public-statistics summaries, optional database-backed training/PIO workpapers, FastAPI runtime, public sample UI, docs, tests, browser QA, and release gates.

It is not a CAD/RMS integration, dispatch tool, enforcement workflow, investigative workflow, evidence system, CJI ingestion path, legal advice engine, live LLM runtime, or public-safety connector.

Install:

```bash
python -m pip install -e ".[dev]"
python -m uvicorn civicsafety.main:app --host 127.0.0.1 --port 8143
```

Townlight Safety v0.1.1 is pinned to `civiccore==0.3.0`.

Optional workpaper persistence is available with `CIVICSAFETY_WORKPAPER_DB_URL`. Set it to a SQLAlchemy database URL to store generated non-CJI training checklists and PIO drafts for later supervisor/PIO review. If unset, POST endpoints remain stateless and retrieval endpoints return an actionable setup message.

## License

Code: AGPL-3.0-only, with the TownLight Public Institution Exception for qualifying deployments. See [LICENSE](LICENSE) and [LICENSE-EXCEPTION.md](LICENSE-EXCEPTION.md).
Documentation: CC BY 4.0 ([LICENSE-DOCS](LICENSE-DOCS)).
