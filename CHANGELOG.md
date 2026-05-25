# 📄 CHANGELOG

## [v2.1.0] - 2026.05.25
### Added
- 新增 **3 种一致性平均值计算模式**
  1. 原始 (max+min)/2 模式
  2. 全体产品真实平均值模式
  3. 指定基准文件作为标准值模式
- 新增配置项 `CONSISTENCY_MODE` 用于切换计算方式
- 新增配置项 `BASE_FILE_NAME` 用于指定基准文件

### Improved
- 优化一致性分析逻辑，计算更精准、更符合工业检测标准
- 提升数据稳定性与兼容性
- 优化图表生成与Excel报告输出体验

## [v7.0] - Final Release

### 🚀 Added（新增）

* 完成 PQ 产品一致性检测全流程自动化系统（12步骤完整pipeline）
* 支持多CSV批量读取与统一数据清洗
* 引入标准流量点匹配机制（REF_FLOW）
* 增加去程 / 回程 / 合并 PQ 曲线分析
* 新增产品一致性加权影响分析模型（核心算法）
* 新增迟滞分析模块（前50% vs 后50%数据对比）
* 新增一致性统计指标（max/min/avg/diff/%）
* 新增 Excel 自动化检测报告生成（openpyxl）
* Excel 内嵌迟滞与一致性 Scatter 图表
* 新增 PQ 总对比散点图（多产品对比）
* 新增单产品性能曲线图批量生成
* 新增压差平均值分析图
* 新增 PNG 图表自动输出系统
* 新增所有产品 PQ 总对比汇总图
* 新增去程/回程 PQ 单文件分析图
* 新增全文件去程/回程总对比图
* 新增 0mA / 60L/min 基准点修正分析
* 新增产品缩放系数建议（scale_suggest）

---

### 🧠 Core Improvements（核心改进）

* 引入 `CONFIG` 集中配置系统（完全参数化）
* 支持 CSV 编码自适应（gbk）
* 所有关键参数支持外部修改无需改代码
* 引入滑动平均滤波（pressure-only filtering）
* 数据清洗流程标准化（NaN / inf / None处理）
* 去程/回程逻辑统一为50%分割策略
* 提升多文件一致性筛选逻辑稳定性
* 引入 weighted deviation 加权模型（核心算法升级）

---

### 📊 Analysis Engine（分析引擎升级）

* 实现加权一致性影响评分系统：

  * 电流权重分级（0 / 300 / 600 / 900 mA）
  * 关键流量点增强权重（KEY_FLOW）
  * 输出文件影响占比 ranking
* 引入产品修正系数计算模型：

  * 基于 global mean / adjusted mean ratio
* 增加异常产品自动识别（worst file detection）

---

### 📈 Visualization（可视化升级）

* 完整 matplotlib 工程化图表系统
* 统一图表风格配置（字体 / 线宽 / 标注）
* 支持：

  * PQ 曲线
  * 迟滞曲线
  * 一致性曲线
  * 压差平均值曲线
* 增加自动防覆盖保存机制（save_safe_plot）
* 支持多产品颜色映射与自动分配

---

### 📦 Excel Report（报告系统升级）

* 完整 Excel 多Sheet结构：

  * 原始检测数据
  * 产品迟滞分析
  * 一致性对比分析
  * 加权影响分析报告
* 自动插入 Scatter Chart 图表
* 支持 Excel 内多产品曲线分组绘制
* 支持动态数据范围引用（Reference/Series）

---

### 🔧 Engineering Fixes（工程优化）

* 修复 CSV 读取异常跳过机制
* 修复空数据 groupby 崩溃问题
* 修复 NaN 导致一致性计算错误
* 修复 Excel 写入重复覆盖问题
* 修复图表文件覆盖问题（自动编号）
* 优化大文件循环性能（减少重复 dataframe 操作）
* 优化 groupby + merge 一致性计算效率

---

### 📁 Output System（输出系统升级）

* 自动创建输出目录（防重名递归编号）
* 分类输出结构：

  * 性能图表/
  * 01_去程PQ/
  * 02_回程PQ/
  * 03_去程+回程PQ/
* Excel + PNG 双路径输出体系
* 支持多文件批量自动归档

---

### ⚠️ Breaking Changes（不兼容变更）

* 不再使用手动单文件分析模式（全部改为批处理）
* 不再支持旧版单流量点分析逻辑
* 去程/回程逻辑统一为50%划分（旧版本兼容方式移除）

---

## [v6.0] - Analysis Expansion

### Added

* 增加迟滞分析功能
* 增加一致性分析统计
* 增加Excel基础报告生成
* 增加PNG图表输出
* 增加基础PQ曲线分析

### Changed

* 优化数据清洗流程
* 优化图表绘制结构

---

## [v5.0] - Consistency Engine

### Added

* 引入一致性分析算法雏形
* 增加工况均值计算
* 增加基础偏差分析

### Changed

* 优化数据分组结构

---

## [v4.0] - PQ Data Processing

### Added

* PQ标准流量点匹配
* CSV批量读取
* 基础数据结构构建（raw_data）

---

## [v2.0] - Initial Release

### Added

* 项目初始化
* CONFIG配置系统
* CSV读取基础框架
* 输出目录结构初始化
* matplotlib基础绘图支持
