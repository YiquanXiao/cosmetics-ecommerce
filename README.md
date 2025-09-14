# Cosmetics E-commerce Data Analysis

**This README includes both English and 中文 versions.** **Click to jump to: [English Version](#english-version) | [中文说明](#中文说明)**

-----

## English Version

An analysis project based on a cosmetics shop's e-commerce event data. It includes two main parts: **EDA & Anomaly Analysis** and **Customer Segmentation**. This project combines funnel analysis, RFM modeling, K-Means clustering, and LightGBM for simulation.

**Kaggle Notebook Links:**

  * **Part 1 - EDA & Anomaly Analysis:** [Link](https://www.kaggle.com/code/yiquanxiao/cosmetics-e-commerce-eda-anomaly-analysis)
  * **Part 2 - Customer Segmentation:** [Link](https://www.kaggle.com/code/yiquanxiao/cosmetics-e-commerce-customer-segmentation-more)

-----

### Purpose

This project helps you:

  * **(Part 1)** Conduct in-depth Exploratory Data Analysis (EDA) to understand user behavior patterns, sales trends, and brand popularity.
  * **(Part 1)** Analyze the user conversion funnel (view → cart → purchase) and identify key drop-off points.
  * **(Part 1)** Perform anomaly analysis to detect bot-like activities, such as excessive browsing without purchasing.
  * **(Part 2)** Segment customers using RFM (Recency, Frequency, Monetary) rules and K-Means clustering.
  * **(Part 2)** Simulate clustering results using LightGBM for real-time customer labeling in a production environment.
  * Support business decisions related to marketing, user experience optimization, and fraud detection.

-----

### Directory Structure

```
cosmetics-ecommerce/
│   LICENSE
│   README.md
│   requirements.txt
│
├───customer segmentation/
│       cosmetics-e-commerce-customer-segmentation-more.ipynb
│
└───eda & anomaly analysis/
        cosmetics-e-commerce-eda-anomaly-analysis.ipynb
```

-----

### How to Use

#### 1️. Prepare the Dataset

Create a new Kaggle Notebook using the [eCommerce Events History in Cosmetics Shop dataset](https://www.kaggle.com/datasets/mkechinov/ecommerce-events-history-in-cosmetics-shop) OR download the data to your local directory.

#### 2️. Run the Notebooks

  * For exploratory analysis and anomaly detection, open `eda & anomaly analysis/cosmetics-e-commerce-eda-anomaly-analysis.ipynb`.
  * For customer segmentation, open `customer segmentation/cosmetics-e-commerce-customer-segmentation-more.ipynb` to run the RFM and K-Means analysis.

-----

### Requirements

  * Python 3.8+
  * pandas
  * numpy
  * matplotlib
  * seaborn
  * scikit-learn
  * lightgbm
  * tqdm
  * joblib
  * jupyter

Install via:

```bash
pip install -r requirements.txt
```

-----

### Notes

  * **Anomaly Analysis (Part 1)** helps identify non-human traffic (bots) by analyzing users with extremely high view counts but no purchases, ensuring data quality for further analysis.
  * The **Customer Segmentation (Part 2)** combines traditional RFM rules with unsupervised K-Means clustering to create more nuanced and data-driven user groups.
  * The **LightGBM model (Part 2)** is used to approximate K-Means labels, enabling near real-time customer scoring in production. SHAP plots provide insights into what drives customer grouping.

-----

## 中文说明

一个基于化妆品商店电商事件数据的分析项目，包含 **探索性数据分析（EDA）与异常检测** 与 **用户分层** 两大部分。项目结合了漏斗分析、RFM 规则建模、K-Means 聚类与 LightGBM 模拟。

**Kaggle Notebook 链接:**

  * **第一部分 - EDA 与异常检测:** [链接](https://www.kaggle.com/code/yiquanxiao/cosmetics-e-commerce-eda-anomaly-analysis)
  * **第二部分 - 用户分层:** [链接](https://www.kaggle.com/code/yiquanxiao/cosmetics-e-commerce-customer-segmentation-more)

-----

### 项目目的

该项目旨在：

  * **(第一部分)** 进行深入的探索性数据分析（EDA），理解用户行为模式、销售趋势和品牌热度。
  * **(第一部分)** 分析用户转化漏斗（浏览 → 加购 → 购买），定位关键流失环节。
  * **(第一部分)** 通过异常行为分析，识别机器人等自动化行为（如频繁浏览但不购买）。
  * **(第二部分)** 使用 RFM 模型和 K-Means 算法对用户进行行为分群。
  * **(第二部分)** 利用 LightGBM 模拟聚类结果，为生产环境中的实时用户打标签提供支持。
  * 为精细化营销、用户体验优化及欺诈检测等业务决策提供数据支持。

-----

### 目录结构

```
cosmetics-ecommerce/
│   LICENSE
│   README.md
│   requirements.txt
│
├───customer segmentation/
│       cosmetics-e-commerce-customer-segmentation-more.ipynb
│
└───eda & anomaly analysis/
        cosmetics-e-commerce-eda-anomaly-analysis.ipynb
```

-----

### 使用方法

#### 1️. 准备数据

在 [Kaggle 数据源](https://www.kaggle.com/datasets/mkechinov/ecommerce-events-history-in-cosmetics-shop) 上新建 Notebook 或者直接下载化妆品电商数据到本地。

#### 2️. 运行 Notebook

  * 如需进行探索性分析与异常检测，请打开 `eda & anomaly analysis/cosmetics-e-commerce-eda-anomaly-analysis.ipynb`。
  * 如需进行用户分层，请打开 `customer segmentation/cosmetics-e-commerce-customer-segmentation-more.ipynb` 运行 RFM 与 K-Means 分析。

-----

### 运行环境

  * Python 3.8+
  * pandas
  * numpy
  * matplotlib
  * seaborn
  * scikit-learn
  * lightgbm
  * tqdm
  * joblib
  * jupyter

使用以下命令安装依赖：

```bash
pip install -r requirements.txt
```

-----

### 注意事项

  * **异常分析（第一部分）** 通过分析拥有极高浏览量但无购买行为的用户，帮助识别非人类流量（机器人），为后续分析保证数据质量。
  * **用户分层（第二部分）** 结合了经典的 RFM 规则与无监督的 K-Means 聚类，以创建更细致、更数据驱动的用户群体。
  * **LightGBM 模型（第二部分）** 用于拟合聚类标签，可用于线上实时用户评分。使用 SHAP 可视化关键特征，辅助运营人员理解用户画像。