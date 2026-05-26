# EDA: Exploratory Data Analysis

## Guide

- 数据长什么样：前几行数据和各列的类型、缺失情况 `train.head()`, `train.info()`
- 缺失值多不多，如何处理缺失值（填充、删除等）
- 目标变量分布，正负样本的比例，处理类别不平衡 (Class Imbalance)
- 特征与目标的关系，用 groupby 和绘图（分析不同进站决策下，圈速、轮胎寿命等特征是否有明显差异）

- 带有时序特征的 tabular 分类问题
- 时序数据 ✅
- 空间数据 ❌

| Column                   | Mean                                               |
| ------------------------ | -------------------------------------------------- |
| `id`                     | 行号，无意义                                       |
| `Driver`                 | 车手名称                                           |
| `Compound`               | 轮胎配方（如 Soft 软胎、Medium 中性胎、Hard 硬胎） |
| `Race`                   | 比赛名称（如 Monaco GP）                           |
| `Year`                   | 比赛年份（2022-2025）                              |
| `PitStop`                | 当前圈是否是进站圈（0/1）                          |
| `LapNumber`              | 当前是第几圈                                       |
| `Stint`                  | 第几段 stint（两次进站之间的连续圈数算一个 stint） |
| `TyreLife`               | 当前轮胎已经跑了多少圈（换胎后从 0 开始计）        |
| `Position`               | 当前排名（第几名）                                 |
| `LapTime (s)`            | 当前圈用时（秒）                                   |
| `LapTime_Delta`          | 圈速变化（和前一圈的差值，负数 = 变快）            |
| `Cumulative_Degradation` | 累计轮胎衰退程度                                   |
| `RaceProgress`           | 比赛进度（0 = 开始，1 = 结束）                     |
| `Position_Change`        | 排名变化（正数 = 上升）                            |
| `PitNextLap`             | 目标：下一圈是否会进站（0/1）                      |

- 直觉
- 轮胎用越久（`TyreLife` 越大）、圈速变慢（`LapTime_Delta` 正值）、轮胎衰退越严重，越可能进站
- 时序数据，同一个车手之前表现，会影响当前表现
- 同一车手在前几圈的状态（轮胎衰退程度、圈速变化趋势）确实会影响后续是否进站
