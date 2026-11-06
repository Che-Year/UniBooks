# Network-Engineering

**Computer networking and computer-organization textbooks.**
**计算机网络与计算机组成原理教材。**

English · [简体中文](#简体中文) · [← 返回 UniBooks](../README.md)

---

## English

### About

This folder holds the networking and computer-organization textbooks in UniBooks. All
three are Chinese university course texts, scanned page by page; they are kept here for
personal study and reference.

### Contents

| # | Title (中文) | Title (EN) | Author | Edition | Publisher | ISBN | Pages | Size |
|---|--------------|------------|--------|---------|-----------|------|-------|------|
| 1 | 计算机网络 | Computer Networks | 谢希仁 (Xie Xiren) | 9th / 第9版 | 电子工业出版社 | 9787121527852 | 435 | 33.6 MB |
| 2 | 计算机网络 | Computer Networks | 谢希仁 (Xie Xiren) | 8th / 第8版 | 电子工业出版社 | 9787121411748 | 485 | 121.9 MB |
| 3 | 计算机组成原理 | Principles of Computer Organization | 蒋本珊 (Jiang Benshan) | 4th / 第4版 | 清华大学出版社 | 9787302530213 | 355 | 105.8 MB |

Direct links:

- [计算机网络（第 9 版）— 谢希仁](<计算机网络(第 9 版)-谢希仁-9787121527852.pdf>)
- [计算机网络（第 8 版）— 谢希仁](<计算机网络(第 8 版)-谢希仁-9787121411748.pdf>)
- [计算机组成原理（第 4 版）— 蒋本珊](<计算机组成原理(第4版)-蒋本珊-9787302530213.pdf>)

### Downloading

The three books total 262 MB. Two points, both measured against these exact files:

- **ZIP does not help.** All three are scanned image PDFs, so the content is already
  compressed. A maximum-compression ZIP shrinks them by roughly 2%, which is not worth
  keeping a second copy of every book.
- **The LFS bandwidth quota is the real limit.** GitHub's free tier gives this
  repository 1 GB of LFS traffic per month, and these three files total 262 MB, so
  after about four full downloads they stop resolving until the quota resets.

Because of that, prefer a resumable clone over clicking download:

```bash
git lfs install
git clone https://github.com/Che-Year/UniBooks.git
cd UniBooks
git lfs pull
```

The PDFs are stored with **Git LFS**, because two of them exceed GitHub's 100 MB
per-file limit. A clone without LFS support gives you small pointer files instead of
the actual PDFs.

If you already cloned and only see stub files, run `git lfs pull` inside the
repository. Browsing on GitHub.com works without LFS installed — the web viewer
resolves the files.

### Copyright and disclaimer

These books are the property of their respective authors and publishers. They are
collected here for **personal study, research, and reference only**. No commercial use,
redistribution, or resale is intended or permitted. If you are a rights holder and want
a file removed, please open an issue and it will be taken down promptly.

Please support the authors and publishers by buying legitimate copies.

---

## 简体中文

### 简介

本文件夹存放 UniBooks 中的计算机网络与计算机组成原理教材。三本都是中文高校课程用书，
逐页扫描件，仅用于个人学习与参考。

### 书目

| # | 书名 | 作者 | 版次 | 出版社 | ISBN | 页数 | 大小 |
|---|------|------|------|--------|------|------|------|
| 1 | 计算机网络 | 谢希仁 | 第 9 版 | 电子工业出版社 | 9787121527852 | 435 | 33.6 MB |
| 2 | 计算机网络 | 谢希仁 | 第 8 版 | 电子工业出版社 | 9787121411748 | 485 | 121.9 MB |
| 3 | 计算机组成原理 | 蒋本珊 | 第 4 版 | 清华大学出版社 | 9787302530213 | 355 | 105.8 MB |

直接下载：

- [计算机网络（第 9 版）— 谢希仁](<计算机网络(第 9 版)-谢希仁-9787121527852.pdf>)
- [计算机网络（第 8 版）— 谢希仁](<计算机网络(第 8 版)-谢希仁-9787121411748.pdf>)
- [计算机组成原理（第 4 版）— 蒋本珊](<计算机组成原理(第4版)-蒋本珊-9787302530213.pdf>)

### 下载说明

三本书合计 262 MB。以下两点是针对这几个文件的实测结论：

- **压缩成 zip 没有意义。** 三本都是扫描件，PDF 内部已压缩，用最高压缩率打包 zip
  只能省约 2%，不值得为此让仓库里多存一份副本。
- **真正的限制是 LFS 流量额度。** GitHub 免费额度给本仓库每月 1 GB 的 LFS 下载流量，
  这三个文件合计 262 MB，也就是大约完整下载四次后，当月就无法再拉取，要等下月重置。

因此建议用可续传的克隆方式，而不是在网页上直接点下载：

```bash
git lfs install
git clone https://github.com/Che-Year/UniBooks.git
cd UniBooks
git lfs pull
```

仓库中的 PDF 使用 **Git LFS** 存储，因为其中两本超过了 GitHub 单文件 100 MB 的限制。
未安装 LFS 时，克隆下来的只会是几十字节的指针文件，而不是真正的 PDF。

已经克隆但只看到占位文件的，在仓库目录内执行 `git lfs pull` 即可。在 GitHub 网页上
直接浏览和下载无需安装 LFS，网页端会自动解析文件。

### 版权声明

本文件夹所有书籍的版权归原作者及出版社所有，仅用于**个人学习、研究与参考**，不用于
任何商业用途、再分发或转售。如版权方希望移除某个文件，请提交 issue，会尽快处理。

请通过正规渠道购买正版图书，支持作者与出版社。

---

[← 返回 UniBooks](../README.md)