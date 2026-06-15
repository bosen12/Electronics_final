# 基礎電子學 重點整理與習題詳解

本專案整理《基礎電子學》第 10、11、12 章的**重點摘要**與**章末習題完整詳解**，以 LaTeX 排版輸出為 PDF。

## 章節內容

| 章節 | 主題 | 習題數 |
|------|------|--------|
| 第 10 章 | FET 數位電路 | 11 題 |
| 第 11 章 | BJT 數位電路 | 10 題 |
| 第 12 章 | 差動及多級放大器 | 19 題 |

## 檔案結構

```
├── 第10章_FET數位電路_詳解.pdf       # 輸出 PDF
├── 第11章_BJT數位電路_詳解.pdf
├── 第12章_差動及多級放大器_詳解.pdf
├── build/                            # LaTeX 原始檔
│   ├── eedu.sty                      # 共用樣式
│   ├── chapter10.tex
│   ├── chapter11.tex
│   ├── chapter12.tex
│   └── fig/                          # 電路圖 (從掃描裁切)
└── C 10 1.pdf, C 10 2.pdf, ...       # 原始掃描 PDF
```

## 編譯方式

需要 XeLaTeX 環境（如 MiKTeX）與微軟正黑體字型。

```bash
cd build
latexmk -xelatex chapter10.tex
latexmk -xelatex chapter11.tex
latexmk -xelatex chapter12.tex
```

## 涵蓋主題

- **第 10 章**：數位反相器雜訊邊界、傳輸延遲、CMOS 反相器與邏輯閘、環形振盪器
- **第 11 章**：簡單 BJT 反相器、TTL 電路系列 (74S/74LS/74AS/74ALS)、BiCMOS
- **第 12 章**：BJT/MOSFET 差動放大器、電流鏡 (基本/Wilson/Widlar)、主動負載、多級放大器
