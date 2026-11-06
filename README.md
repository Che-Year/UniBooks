# UniBooks

**A curated library of university textbooks and study material.**
**大学教材与学习资料库。**

[简体中文](README.zh-CN.md) · **English**

---

## About

UniBooks keeps university-level textbooks and the study material built from them in
one place, so they are easy to find, cite and study from. Content is grouped by subject,
one folder per collection, and every folder documents itself.

Everything here is for personal study and reference.

## Collections

| Folder | Contents | Size |
|---|---|---|
| [Network-Engineering](Network-Engineering/README.md) | Computer networking and computer-organization textbooks, 3 scanned PDFs | 262 MB |
| [Lexis-WorkBank](Lexis-WorkBank/README.md) | The ODE bilingual dictionary and the Obsidian word bank generated from it | 188 MB |

### Network-Engineering

Textbooks for networking and computer organization: 谢希仁's *Computer Networks* (9th
and 8th editions) and 蒋本珊's *Principles of Computer Organization* (4th edition).
Stored with Git LFS. See the [folder README](Network-Engineering/README.md) for the
catalogue, download guidance and the LFS quota caveat.

### Lexis-WorkBank

The *Oxford Dictionary of English, 3rd edition* in bilingual EN→ZH form (`.mdx` + `.mdd`),
plus a 243,119-file Markdown word bank generated from it for the Obsidian Lexis plugin.
Stored as ordinary Git objects, so none of it consumes LFS quota. See the
[folder README](Lexis-WorkBank/README.md) for the file format and how the word bank was
generated.

## Downloading

Two storage mechanisms are in use, and they behave differently:

- **`Network-Engineering` uses Git LFS.** A plain clone without LFS installed gives you
  small pointer files instead of PDFs. Run `git lfs install` first. The free tier allows
  1 GB of LFS traffic per month, and these three books total 262 MB, so roughly four
  full downloads exhaust the month's quota.
- **`Lexis-WorkBank` uses ordinary Git objects.** No LFS setup needed; it is dragged
  down with every clone.

```bash
# Full clone, including the LFS-hosted books
git lfs install
git clone https://github.com/Che-Year/UniBooks.git
cd UniBooks
git lfs pull
```

To skip the 262 MB of textbooks and fetch only the text material:

```bash
GIT_LFS_SKIP_SMUDGE=1 git clone https://github.com/Che-Year/UniBooks.git
```

Browsing and downloading on GitHub.com works without LFS installed — the web viewer
resolves the files.

## Copyright and disclaimer

All books in this repository are the property of their respective authors and
publishers, and the dictionary is the property of Oxford University Press. Everything is
collected here for **personal study, research and reference only**. No commercial use,
redistribution or resale is intended or permitted. If you are a rights holder and want
a file removed, please open an issue and it will be taken down promptly.

Please support the authors, publishers and dictionary makers by buying legitimate
copies.

## License

This README and the repository structure are released under
[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). The books and the dictionary
are **not** covered by this license — see the copyright notice above.