# UniBooks

**A curated library of university textbook PDFs.**
**大学教材 PDF 图书馆。**

English · [简体中文](#简体中文)

---

## English

### About

UniBooks is a personal collection of university-level textbooks, kept in one place so
they are easy to find, cite, and study from. Books are grouped by subject area, with one
folder per discipline. Everything here is for personal study and reference.

### Repository layout

```
UniBooks/
└── Network-Engineering/
    ├── 计算机网络(第 8 版)-谢希仁-9787121411748.pdf
    ├── 计算机网络(第 9 版)-谢希仁-9787121527852.pdf
    └── 计算机组成原理(第4版)-蒋本珊-9787302530213.pdf
```

### Network-Engineering

| # | Title (中文) | Title (EN) | Author | Edition | Publisher | ISBN | Pages | Size |
|---|--------------|------------|--------|---------|-----------|------|-------|------|
| 1 | 计算机网络 | Computer Networks | 谢希仁 (Xie Xiren) | 9th / 第9版 | 电子工业出版社 | 9787121527852 | 435 | 34 MB |
| 2 | 计算机网络 | Computer Networks | 谢希仁 (Xie Xiren) | 8th / 第8版 | 电子工业出版社 | 9787121411748 | 485 | 122 MB |
| 3 | 计算机组成原理 | Principles of Computer Organization | 蒋本珊 (Jiang Benshan) | 4th / 第4版 | 清华大学出版社 | 9787302530213 | 355 | 106 MB |

Direct links:

- [计算机网络（第 9 版）— 谢希仁](<Network-Engineering/计算机网络(第 9 版)-谢希仁-9787121527852.pdf>)
- [计算机网络（第 8 版）— 谢希仁](<Network-Engineering/计算机网络(第 8 版)-谢希仁-9787121411748.pdf>)
- [计算机组成原理（第 4 版）— 蒋本珊](<Network-Engineering/计算机组成原理(第4版)-蒋本珊-9787302530213.pdf>)

### Cloning

The PDFs are stored with **Git LFS**, because two of them exceed GitHub's 100 MB
per-file limit. A clone without LFS support gives you small pointer files instead of the
actual PDFs.

```bash
# One-time setup
git lfs install

# Clone with the files
git clone https://github.com/Che-Year/UniBooks.git
cd UniBooks
git lfs pull
```

If you already cloned and only see stub files, run `git lfs pull` inside the repository.

Browsing on GitHub.com works without LFS installed — the web viewer resolves the files.

### Copyright and disclaimer

All books in this repository are the property of their respective authors and publishers.
They are collected here for **personal study, research, and reference only**. No commercial
use, redistribution, or resale is intended or permitted. If you are a rights holder and want
a file removed, please open an issue and it will be taken down promptly.

Please support the authors and publishers by buying legitimate copies of the books you use.

---

## 简体中文

### 简介

UniBooks 是一个个人大学教材 PDF 库，把常用教材集中存放，便于查阅、引用和学习。
书籍按学科分类，每个学科一个文件夹。本仓库仅用于个人学习与参考。

### 仓库结构

```
UniBooks/
└── Network-Engineering/
    ├── 计算机网络(第 8 版)-谢希仁-9787121411748.pdf
    ├── 计算机网络(第 9 版)-谢希仁-9787121527852.pdf
    └── 计算机组成原理(第4版)-蒋本珊-9787302530213.pdf
```

### Network-Engineering（网络工程）

| # | 书名 | 作者 | 版次 | 出版社 | ISBN | 页数 | 大小 |
|---|------|------|------|--------|------|------|------|
| 1 | 计算机网络 | 谢希仁 | 第 9 版 | 电子工业出版社 | 9787121527852 | 435 | 34 MB |
| 2 | 计算机网络 | 谢希仁 | 第 8 版 | 电子工业出版社 | 9787121411748 | 485 | 122 MB |
| 3 | 计算机组成原理 | 蒋本珊 | 第 4 版 | 清华大学出版社 | 9787302530213 | 355 | 106 MB |

直接下载：

- [计算机网络（第 9 版）— 谢希仁](<Network-Engineering/计算机网络(第 9 版)-谢希仁-9787121527852.pdf>)
- [计算机网络（第 8 版）— 谢希仁](<Network-Engineering/计算机网络(第 8 版)-谢希仁-9787121411748.pdf>)
- [计算机组成原理（第 4 版）— 蒋本珊](<Network-Engineering/计算机组成原理(第4版)-蒋本珊-9787302530213.pdf>)

### 克隆说明

仓库中的 PDF 使用 **Git LFS** 存储，因为其中两本超过了 GitHub 单文件 100 MB 的限制。
如果未安装 LFS，克隆下来的只会是几十字节的指针文件，而不是真正的 PDF。

```bash
# 首次使用需安装一次
git lfs install

# 克隆并拉取文件
git clone https://github.com/Che-Year/UniBooks.git
cd UniBooks
git lfs pull
```

已经克隆但只看到占位文件的，在仓库目录内执行 `git lfs pull` 即可。

在 GitHub 网页上直接浏览和下载无需安装 LFS，网页端会自动解析文件。

### 版权声明

本仓库所有书籍的版权归原作者及出版社所有，仅用于**个人学习、研究与参考**，
不用于任何商业用途、再分发或转售。如版权方希望移除某个文件，请提交 issue，会尽快处理。

请通过正规渠道购买正版图书，支持作者与出版社。

---

### License

The README and repository structure are released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
The books themselves are **not** covered by this license — see the copyright notice above.