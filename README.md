# 📘 README - PQ一致性检测分析系统

## 🇨🇳 中文版本

---

## 📌 项目简介

本项目用于对**比例电磁阀 / 液压阀测试数据**进行自动化分析与质量评估，包括：

* PQ（压力-流量）性能曲线分析
* 多产品一致性对比
* 迟滞（Hysteresis）分析
* 加权一致性影响建模
* 自动生成 Excel + PNG + SVG 工程报告

支持批量 CSV 数据自动处理。

---

# 🧭 版本迭代记录（Version History）

## 🟢 v1.0（基础分析版）

**关键词：数据读取 + 基础曲线**

* CSV数据批量读取
* PQ基础曲线绘制
* 简单流量-压差关系分析
* matplotlib基础图表输出

📌 特点：

> 单机脚本，无结构化报告

---

## 🟡 v2.0（工程分析版）

**关键词：一致性 + Excel报告**

新增：

* 多文件一致性分析
* max/min/avg统计
* Excel自动生成（openpyxl）
* 迟滞计算（前50% vs 后50%）
* 标准流量点匹配（5/10/20/40/60 L/min）

📌 特点：

> 从“画图工具”升级为“测试分析工具”

---

## 🔴 v3.0（当前版本｜工程系统版）

**关键词：权重模型 + 自动修正 + SVG报告**

### 🚀 核心升级

#### 1️⃣ 加权一致性影响模型

* 引入电流 + 流量双权重机制
* 自动识别“最影响一致性的文件”
* 输出修正系数（scale factor）

#### 2️⃣ PQ分析增强

* 前50%数据建模
* 多电流曲线自动标注
* 支持批量产品对比图

#### 3️⃣ 迟滞分析升级

H = |P_{forward} - P_{reverse}|

* 自动计算滞环偏差
* Excel + 图像双输出

#### 4️⃣ 一致性工程图增强

* 双区域（前50% / 后50%）
* ±bar / ±% 动态标签切换
* 工业图表样式统一

#### 5️⃣ 输出系统升级

* Excel（4个Sheet）
* PNG高清图（300 DPI）
* SVG矢量图（支持鼠标悬浮文件名）
* 自动输出目录管理（防重名）

📌 特点：

> 已接近“工业测试分析软件级别”

---

## 📂 输出结构

```text
检测结果输出/
│
├── 产品检测结果总表.xlsx
├── 性能图表/
├── 迟滞图.png
├── 一致性图.png
├── 压差平均值图.png
├── 所有产品PQ曲线对比图.png
└── 所有产品PQ曲线对比图_矢量.svg
```

---

## ⚙️ 运行方式

```bash
pip install pandas numpy matplotlib openpyxl
python main.py
```

---

## 📌 应用场景

* 电磁阀研发测试
* 液压系统标定
* 工业流量控制分析
* 批量实验数据处理

---

---

# 🇬🇧 English Version

---

## 📌 Overview

This project is an automated analysis system for **proportional solenoid valve / hydraulic test data**, including:

* PQ (Pressure-Flow) curve analysis
* Multi-product consistency evaluation
* Hysteresis analysis
* Weighted influence modeling
* Automatic Excel + PNG + SVG reporting

---

# 🧭 Version History

## 🟢 v1.0 - Basic Analysis

* CSV batch loading
* Basic PQ curve plotting
* Simple pressure-flow visualization

📌 Status:

> Prototype script

---

## 🟡 v2.0 - Engineering Analysis

* Multi-file consistency comparison
* Max/min/avg statistics
* Excel report generation
* Hysteresis calculation (forward vs reverse)

📌 Status:

> Engineering-level analysis tool

---

## 🔴 v3.0 - Full Engineering System

### 🚀 Major upgrades

#### Weighted consistency model

* Current + flow weighted influence
* Automatic outlier file detection
* Scaling factor recommendation

#### PQ system upgrade

* First 50% data modeling
* Multi-current curve annotation
* Batch product comparison

#### Hysteresis analysis

H = |P_{forward} - P_{reverse}|

#### Output system upgrade

* Excel (4 sheets)
* High-res PNG (300 DPI)
* SVG vector output (interactive labels)
* Auto folder management

📌 Status:

> Engineering-grade analysis system

---

# 📦 GitHub上传建议（可选）

推荐仓库结构：

```text
PQ-System/
│
├── main.py
├── README.md
├── requirements.txt
├── sample_data/
└── output/
```

---

# 📌 requirements.txt

```txt
pandas
numpy
matplotlib
openpyxl
```