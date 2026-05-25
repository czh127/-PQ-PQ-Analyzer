\# PQ Analyzer



工业级比例阀 / 电磁阀 PQ 曲线自动分析平台  

Industrial PQ Curve Analysis Platform for Proportional Valves and Electro-Hydraulic Systems



\---



\# 项目简介 | Introduction



PQ Analyzer 是一个用于比例电磁阀、液压阀及电液控制系统测试数据分析的 Python 工程项目。  



PQ Analyzer is a Python-based engineering project designed for automatic analysis of proportional valve and electro-hydraulic system test data.



该项目能够自动读取测试 CSV 数据，并完成：



The platform automatically processes CSV test files and provides:



\- PQ 曲线分析 | PQ curve analysis

\- 一致性分析 | Consistency evaluation

\- 迟滞分析 | Hysteresis analysis

\- 自动绘图 | Automatic plotting

\- Excel 数据导出 | Excel report exporting

\- 批量文件处理 | Batch data processing

\- 数据滤波与异常处理 | Data filtering and validation



适用于 | Suitable for:



\- 比例减压阀 | Proportional pressure valves

\- 比例溢流阀 | Proportional relief valves

\- 高速开关阀 | High-speed switching valves

\- 电液控制系统 | Electro-hydraulic systems

\- 工业测试平台 | Industrial testing platforms



\---



\# 功能特性 | Features



\## 1. PQ 曲线自动分析 | Automatic PQ Curve Analysis



\- 自动提取不同电流下的 PQ 数据  

&#x20; Extracts PQ data under different current levels



\- 自动匹配参考流量点  

&#x20; Matches reference flow points automatically



\- 自动生成性能曲线  

&#x20; Generates performance curves automatically



\---



\## 2. 一致性分析 | Consistency Evaluation



\- 多产品一致性对比  

&#x20; Multi-product consistency comparison



\- 自动计算偏差百分比  

&#x20; Automatic deviation percentage calculation



\- 一致性评分分析  

&#x20; Consistency scoring analysis



\---



\## 3. 迟滞分析 | Hysteresis Analysis



自动计算 | Automatically calculates:



\- 上升曲线 | Rising curve

\- 下降曲线 | Falling curve

\- 迟滞误差 | Hysteresis error



并生成迟滞特性图。  

Generates hysteresis characteristic plots automatically.



\---



\## 4. 自动绘图 | Automatic Plotting



自动生成 | Automatically generates:



\- 单产品性能图 | Single-product performance plots

\- PQ 对比图 | PQ comparison plots

\- 一致性图 | Consistency plots

\- 迟滞图 | Hysteresis plots



\---



\## 5. Excel 自动导出 | Excel Report Exporting



自动生成 | Automatically exports:



\- 原始数据表 | Raw data tables

\- 一致性结果 | Consistency results

\- 迟滞结果 | Hysteresis results

\- 分析结果总表 | Summary analysis tables



\---



\# 技术栈 | Tech Stack



\- Python

\- Pandas

\- NumPy

\- Matplotlib

\- OpenPyXL



\---



\# 项目结构 | Project Structure



```text

PQ-Analyzer/

│

├── main.py

├── config.py

├── requirements.txt

│

├── core/

│   ├── cleaner.py

│   ├── filter.py

│   ├── pq\_analysis.py

│   ├── hysteresis.py

│   └── consistency.py

│

├── plotting/

│

├── export/

│

├── input/

│

└── output/

```



\---



\# 安装方法 | Installation



\## 1. 克隆项目 | Clone Repository



```bash

git clone https://github.com/YourName/PQ-Analyzer.git

```



\---



\## 2. 安装依赖 | Install Dependencies



```bash

pip install -r requirements.txt

```



\---



\## 3. 运行程序 | Run Program



将 CSV 文件放入项目目录后运行：  

Place CSV files into the project directory and run:



```bash

python main.py

```



\---



\# 输出结果 | Outputs



程序将自动生成：  

The program automatically generates:



\- PNG 图表 | PNG plots

\- Excel 分析报告 | Excel analysis reports

\- 自动输出目录 | Automatic output folders



\---



\# Roadmap | 开发计划



\- \[x] PQ 曲线分析 | PQ curve analysis

\- \[x] 一致性分析 | Consistency evaluation

\- \[x] 迟滞分析 | Hysteresis analysis

\- \[x] Excel 自动导出 | Excel exporting

\- \[ ] GUI 图形界面 | GUI interface

\- \[ ] PDF 自动测试报告 | PDF automatic reports

\- \[ ] 实时数据采集 | Real-time data acquisition

\- \[ ] AI 异常诊断 | AI fault diagnosis

\- \[ ] 数据库存储 | Database integration

\- \[ ] 在线分析平台 | Online analysis platform



\---



\# 项目目标 | Project Vision



该项目旨在建立一个工业级电液测试数据分析平台，实现：



This project aims to build an industrial-grade electro-hydraulic test data analysis platform featuring:



\- 自动化测试分析 | Automated testing analysis

\- 数据可视化 | Data visualization

\- 测试标准化 | Test standardization

\- 智能故障诊断 | Intelligent fault diagnosis



\---



\# License



MIT License

