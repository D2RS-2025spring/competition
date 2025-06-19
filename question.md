# 基础复现：重现随机森林模型预测ARGs水平转移的关键结果

## 1.来源论文
Lund, D., Parras-Moltó, M., Inda-Díaz, J.S. et al. Genetic compatibility and ecological connectivity drive the dissemination of antibiotic resistance genes. Nat Commun 16, 2595 (2025).  
[全文链接](https://www.nature.com/articles/s41467-025-57825-3)

## 2.任务描述
使用论文提供的开源代码与数据，复现预测抗生素抗性基因（ARGs）水平转移的随机森林模型，重现文中五大关键结果

## 3.指南

### 3.1所需数据与代码
[下载地址](https://zenodo.org/records/14901409)

### 3.2要求

#### 复现目标清单
| **序号** | **关键结果**                  | **验证标准**                                                                 | 对应图表 |
|----------|-------------------------------|-----------------------------------------------------------------------------|----------|
| 1        | 水平转移基因鉴定与随机森林模型性能              | 准确识别**6,276个**水平转移事件，其中APH占比**29.9%**，Class B β-内酰胺酶显著偏低；模型AUROC≥**0.87**，Tet RPG模型AUROC≥**0.92** |<img src="https://github.com/user-attachments/assets/81457992-361c-47ea-8a5e-eb26e8f3293b" alt="图2" width="200"/>|
| 2        | 因子重要性分析                | 确认`genome-gene 5mer distance`为最重要抑制因子，`Human co-occurrence`为最强促进因子 |<img src="https://github.com/user-attachments/assets/58604bf8-e20b-4742-89e4-d6e28f02d587" alt="图3" width="200"/>|
| 3        | 遗传不相容性阈值效应          | 当基因组5-mer距离>**0.025**时转移概率骤降，ARG-基因组距离>**0.15**时概率趋近0 |<img src="https://github.com/user-attachments/assets/1d4ec672-8a63-49b1-b48d-0d2042b6e46d" alt="图4" width="200"/>|
| 4        | 人类-废水传播网络             | 人类网络含**5门10纲**核心节点（如大肠杆菌），废水网络含**不动杆菌-假单胞菌**强连接 |<img src="https://github.com/user-attachments/assets/37692cb5-338b-424c-9bb1-fe993108305f" alt="图5" width="200"/>|

#### 提交结果格式
Markdown格式

Html格式

Notebook格式
