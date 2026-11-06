# Lexis-WorkBank

**The ODE dictionary data and its generated Obsidian Lexis word bank.**
**《新牛津英汉双解大词典》词典本体，以及基于它构建的 Obsidian Lexis 词库。**

English · [简体中文](#简体中文)

---

## English

### About

This folder holds two things: the dictionary files themselves, and a word bank
generated from them for the [Lexis](#) plugin in Obsidian.

- **The dictionary** is the *Oxford Dictionary of English, 3rd edition* (2019-02-12),
  bilingual EN→ZH, distributed as the standard MDict pair `.mdx` + `.mdd`. The `.mdx`
  holds the 243,303 headword entries; the `.mdd` holds the resources (style sheet,
  scripts, and the pronunciation and other images) that the entries reference.
- **The word bank** is a flat set of Markdown files, one per entry, written in the
  format the Lexis plugin reads.

### Repository layout

```
Lexis-WorkBank/
├── ODE 3e 20191231M.mdx    dictionary entries  (87.5 MB)
├── ODE 3e 20191231M.mdd    dictionary resources (22.1 MB)
└── lexis-workbank.zip      generated word bank  (78.1 MB)
```

### The word bank

`lexis-workbank.zip` unpacks to one `.md` file per headword. Each file follows the same
template:

```markdown
---
tags:
---
[[WordBank]]
#### 释义
> n. 风景，景色；（舞台或电影的）布景
#### 例句
> - Spectacular views of mountain scenery. —— 壮丽的山景。
```

| Field | Contents |
|---|---|
| Frontmatter | Empty `tags:` block, matching the Lexis convention |
| First line | `[[WordBank]]`, the tag that files this note as a word-bank entry |
| `#### 释义` | Part of speech plus the Chinese definitions, up to four per entry, joined with `；` |
| `#### 例句` | English example and its Chinese translation, joined with `——`; up to two |

A few points about the data, measured against these exact files:

- **Coverage.** 243,119 of the dictionary's 243,303 entries produce a file (99.9%).
  The 184 that do not are stub entries in the source data carrying no definition text
  at all, in any language.
- **Definitions.** Chinese definitions are used wherever the dictionary provides them.
  About 116,000 entries are English-only in the source; for those the English
  definition is used instead, so every file still has a `#### 释义` section.
- **Examples.** Roughly 10% of entries carry an example. ODE supplies examples mainly
  for common words; rare words, proper nouns and multi-word phrases generally have
  none, so many files have an empty `#### 例句` section.
- **Name collisions.** 267 pairs differ only in case, which Windows and macOS cannot
  store side by side. These are disambiguated with a `_2` suffix.
- **Links.** `[[WordBank]]` is the only wiki-link in a generated file. Source-specific
  links are deliberately absent, so the files do not depend on notes outside the vault.

### Regenerating the word bank

The files were produced by parsing the `.mdx` directly, in this order:

1. Read entries with [`mdict-utils`](https://pypi.org/project/mdict-utils/).
2. For each entry, take the Chinese definitions (`cn_def`); where an entry has none,
   fall back to its English definition (`aw5`), which is nested and needs balanced
   tag matching rather than a plain regex.
3. Take the example pairs (`xxn` + `p.cn`) when present.
4. Write one Markdown file per headword.

### Notes for reuse

- The two dictionary files are a matched pair. Copy both; the `.mdx` alone will render
  without styling or pronunciation images.
- `lexis-workbank.zip` is the 243,000-file tree packed once, because unpacked it is
  243,119 small files — far more than is practical to commit individually.

### Copyright and disclaimer

The *Oxford Dictionary of English* is the property of Oxford University Press. It is
kept here for **personal study, research and reference only**. No commercial use,
redistribution or resale is intended or permitted. If you are a rights holder and want
a file removed, please open an issue and it will be taken down promptly.

The generated word bank is derived from that dictionary and follows the same terms.

Please support the publisher by buying a legitimate copy.

---

## 简体中文

### 简介

本文件夹保存两样东西：词典本体，以及从中生成、供 Obsidian 的 [Lexis](#) 插件使用的词库。

- **词典本体**是《新牛津英汉双解大词典》第 3 版（2019-02-12），英汉双解，采用标准
  MDict 的 `.mdx` + `.mdd` 双文件形式。`.mdx` 存放 243,303 条词条，`.mdd` 存放词条
  引用的资源（样式表、脚本、发音及其他图片）。
- **词库**是一组平铺的 Markdown 文件，一个词条一个文件，按 Lexis 插件读取的格式书写。

### 仓库结构

```
Lexis-WorkBank/
├── ODE 3e 20191231M.mdx    词典词条   (87.5 MB)
├── ODE 3e 20191231M.mdd    词典资源   (22.1 MB)
└── lexis-workbank.zip      生成的词库 (~N0 MB)
```

### 词库说明

`lexis-workbank.zip` 解压后是一个词条一个 `.md` 文件，每个文件格式相同：

```markdown
---
tags:
---
[[WordBank]]
#### 释义
> n. 风景，景色；（舞台或电影的）布景
#### 例句
> - Spectacular views of mountain scenery. —— 壮丽的山景。
```

| 段落 | 内容 |
|---|---|
| frontmatter | 空的 `tags:` 块，与 Lexis 的约定一致 |
| 首行 | `[[WordBank]]`，把这个笔记归入词库的标签 |
| `#### 释义` | 词性 + 中文释义，每个词条最多 4 条，用 `；` 分隔 |
| `#### 例句` | 英文例句与其中文翻译，用 `——` 分隔，最多 2 条 |

以下是基于这批文件实测的几点说明：

- **覆盖情况。** 词典 243,303 条词条中，243,119 条生成了文件（99.9%）。未生成的
  184 条是源数据里的空壳条目，任何语言下都没有释义文本。
- **释义。** 词典提供中文释义时一律用中文。约有 11.6 万条在原词典中只有英文释义，
  这类词条改用英文释义，从而保证每个文件都有 `#### 释义` 段。
- **例句。** 约 10% 的词条带例句。ODE 主要为常用词配例句，冷僻词、专有名词和多数
  多词短语本身没有，因此不少文件的 `#### 例句` 段为空。
- **重名。** 有 267 组词条仅大小写不同，Windows 和 macOS 无法并存，已用 `_2` 后缀区分。
- **链接。** 生成的文件中唯一的双链是 `[[WordBank]]`，刻意不带任何源笔记链接，避免
  依赖词库之外的笔记。

### 重新生成词库

这批文件是直接解析 `.mdx` 得到的，步骤依次为：

1. 用 [`mdict-utils`](https://pypi.org/project/mdict-utils/) 读取词条。
2. 每个词条取中文释义（`cn_def`）；没有中文的，回退到英文释义（`aw5`）。后者存在
   嵌套标签，必须做标签配平而不能用普通正则。
3. 有例句的，取英文原句与中文翻译（`xxn` + `p.cn`）配对。
4. 每个词条写出一个 Markdown 文件。

### 复用提示

- 两个词典文件是配套的一对，需要一起复制。只有 `.mdx` 时能显示内容，但没有样式和
  发音图片。
- `lexis-workbank.zip` 是 24 万个文件的整体压缩包。解压后是 243,119 个小文件，
  逐个提交并不现实，因此打包存放。

### 版权声明

《新牛津英汉双解大词典》版权归牛津大学出版社所有，此处仅用于**个人学习、研究与
参考**，不用于任何商业用途、再分发或转售。如版权方希望移除文件，请提交 issue，
会尽快处理。

生成的词库派生自该词典，遵循相同条款。

请通过正规渠道购买正版，支持出版社。

---

### License

This README and the folder structure are released under
[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
The dictionary and the word bank derived from it are **not** covered by this license —
see the copyright notice above.