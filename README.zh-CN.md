# UniBooks

**A curated library of university textbooks and study material.**
**大学教材与学习资料库。**

**简体中文** · [English](README.md)

---

## 简介

UniBooks 把大学教材以及基于这些教材整理的学习资料集中存放，便于查阅、引用和学习。
内容按主题分组，一个主题一个文件夹，每个文件夹都自带说明文档。

本仓库内容仅用于个人学习与参考。

## 内容分类

| 文件夹 | 内容 | 体积 |
|---|---|---|
| [Network-Engineering](Network-Engineering/README.md) | 计算机网络与计算机组成原理教材，3 本扫描版 PDF | 262 MB |
| [Lexis-WorkBank](Lexis-WorkBank/README.md) | 新牛津英汉双解大词典本体，以及由它生成的 Obsidian 词库 | 188 MB |

### Network-Engineering（网络工程）

网络与计算机组成原理方向的教材：谢希仁《计算机网络》第 9 版和第 8 版，蒋本珊
《计算机组成原理》第 4 版。使用 Git LFS 存储。书目、下载方式以及 LFS 流量额度的
注意事项见[该文件夹的说明](Network-Engineering/README.md)。

### Lexis-WorkBank（词库）

《新牛津英汉双解大词典》第 3 版英汉双解版（`.mdx` + `.mdd`），以及从中生成的
243,119 个 Markdown 文件，供 Obsidian 的 Lexis 插件使用。按普通 Git 对象存储，
不占用 LFS 额度。文件格式与生成方式见[该文件夹的说明](Lexis-WorkBank/README.md)。

## 下载说明

仓库里同时使用了两种存储方式，行为不同：

- **`Network-Engineering` 使用 Git LFS。** 未安装 LFS 直接克隆，得到的只是几十字节
  的指针文件而不是 PDF，所以要先执行 `git lfs install`。免费额度为每月 1 GB 的 LFS
  流量，而这三本书合计 262 MB，大约完整下载四次就会用尽当月额度。
- **`Lexis-WorkBank` 使用普通 Git 对象。** 不需要任何 LFS 设置，但每次克隆都会被
  一并拉下来。

```bash
# 完整克隆，包含 LFS 托管的三本教材
git lfs install
git clone https://github.com/Che-Year/UniBooks.git
cd UniBooks
git lfs pull
```

如果只想取文字资料、跳过 262 MB 的教材：

```bash
GIT_LFS_SKIP_SMUDGE=1 git clone https://github.com/Che-Year/UniBooks.git
```

在 GitHub 网页上直接浏览和下载无需安装 LFS，网页端会自动解析文件。

## 版权声明

本仓库所有书籍的版权归原作者及出版社所有，词典版权归牛津大学出版社所有。所有内容
仅用于**个人学习、研究与参考**，不用于任何商业用途、再分发或转售。如版权方希望移除
某个文件，请提交 issue，会尽快处理。

请通过正规渠道购买正版，支持作者、出版社与词典编纂方。

## 许可

本 README 与仓库结构以 [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
发布。书籍与词典本身**不**适用该许可，详见上方的版权声明。