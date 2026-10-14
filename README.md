# 译稿存档：美国 45 CFR 第 92 部分与 CLAS 国家标准（中文译本）

本目录是一个**本地 Git 存档库**，用于对译稿的 Markdown 版与 PDF 版做版本留痕。
每次修订提交后，都会产生一个唯一的提交码（commit hash），可据此精确回溯到某一版内容。

---

## 一、版本信息

| 项目 | 内容 |
| --- | --- |
| 版本标签 | `v1.0`（附注标签 / annotated tag） |
| 首次存档日期 | 2026-10-14 |
| 存档作者 | pp &lt;3108230747@qq.com&gt; |
| 内容提交码 | 见 `版本记录.txt` |
| 当前分支 | `main` |

---

## 二、存档内容

| 文件 | 说明 | 大小 |
| --- | --- | --- |
| `美国45CFR第92部分与CLAS国家标准_中文译本.md` | 中文译本（Markdown 源文件，四段式：译者说明 / 45 CFR 第 92 部分节选 / CLAS 国家标准 15 条 / 术语对照表） | 12,748 字节 |
| `美国45CFR第92部分与CLAS国家标准_中文译本.pdf` | 同内容的 A4 排版 PDF（微软雅黑，深蓝标题分级） | 366,048 字节 |
| `CHECKSUMS-SHA256.txt` | 上述两个文件的 SHA-256 校验值 | — |
| `版本记录.txt` | 版本码、提交码、校验值汇总 | — |
| `README.md` | 本说明文件 | — |

---

## 三、材料来源与生成方式

**原始英文材料（未纳入本库，仍保留在原位置）**

1. `MinerU_markdown_CFR-2025-title45-vol1-sec92-11_2110275961965268992.md`
   —— 45 CFR Subtitle A（2025-10-01 版）第 92 部分节选，**源文本首尾均不完整**，起于 § 92.10(c)(1)(ii) 句中、止于 § 92.101(b)(1)(i) 句中。
2. `MinerU_markdown_EnhancedNationalCLASStandards_Revised_June2025_2110276267767779328.md`
   —— CLAS 国家标准（2025 年 6 月修订版）全文。

**生成链路**

- 英译中并合并为单个 Markdown 文件（译文中以【译者注】标明源文本缺损与版式噪声）；
- Markdown → HTML：本地脚本 `md2html.py`（零第三方依赖，内置中文 A4 排版样式）；
- HTML → PDF：Microsoft Edge 无头打印（`--headless=new --print-to-pdf`）。

---

## 四、常用操作

```bash
# 查看提交历史（带标签）
git log --oneline --decorate

# 查看 v1.0 存档详情
git show v1.0

# 回到 v1.0 版本（只读查看）
git checkout v1.0

# 校验文件是否被改动（应与 CHECKSUMS-SHA256.txt 一致）
Get-FileHash "美国45CFR第92部分与CLAS国家标准_中文译本.md" -Algorithm SHA256

# 导出一个可移动的单文件存档包
git bundle create 译稿存档_v1.0.bundle --all
```

> 注：本机 `git` 位于 `C:\Users\我是小菜菜\AppData\Local\Programs\Git\cmd\git.exe`。
