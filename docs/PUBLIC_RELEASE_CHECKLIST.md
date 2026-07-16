# Public Release Checklist

- [x] Raw climate archives excluded
- [x] Generated data panels excluded
- [x] Manuscript and submission folders excluded
- [x] Local machine paths removed
- [x] Personal contact metadata removed
- [x] Portable environment file added
- [x] Selected figures reviewed for public release
- [x] Documentation explains data-access limits

Recommended update workflow:

```bash
git status
git add README.md docs/ python_scripts/ figures/selected/
git commit -m "Describe the specific update"
git push
```
