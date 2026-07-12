# ASR Research Project

A rigorous and reproducible quantitative research programme.

## Research checklist

- [ ] Research question and hypotheses documented
- [ ] Data provenance and licence documented
- [ ] Reproduction environment defined
- [ ] Tests and validation included
- [ ] Limitations and failure cases documented
- [ ] CITATION.cff updated

## Development

```bash
python -m venv .venv
source .venv/bin/activate
pip install -e .[dev]
pytest
```
