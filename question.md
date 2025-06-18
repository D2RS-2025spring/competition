# 基础复现：重现随机森林模型预测ARGs水平转移的关键结果

## 来源论文
Lund, D., Parras-Moltó, M., Inda-Díaz, J.S. et al. Genetic compatibility and ecological connectivity drive the dissemination of antibiotic resistance genes. Nat Commun 16, 2595 (2025).  
[全文链接](https://www.nature.com/articles/s41467-025-57825-3)

## 任务描述
使用论文提供的开源代码与数据，复现预测抗生素抗性基因（ARGs）水平转移的随机森林模型，重现以下五大关键结果：

## 复现目标清单
| **序号** | **关键结果**                  | **验证标准**                                                                 | 对应图表 |
|----------|-------------------------------|-----------------------------------------------------------------------------|----------|
| 1        | 水平转移基因鉴定              | 准确识别**6,276个**水平转移事件，其中APH占比**29.9%**，Class B β-内酰胺酶显著偏低 | 图2b     |
| 2        | 随机森林模型性能              | 通用模型AUROC≥**0.87**，Tet RPG模型AUROC≥**0.92**                             | 图2c-d   |
| 3        | 因子重要性分析                | 确认`genome-gene 5mer distance`为最重要抑制因子，`Human co-occurrence`为最强促进因子 | 图3      |
| 4        | 遗传不相容性阈值效应          | 当基因组5-mer距离>**0.025**时转移概率骤降，ARG-基因组距离>**0.15**时概率趋近0 | 图4a-b   |
| 5        | 人类-废水传播网络             | 人类网络含**5门10纲**核心节点（如大肠杆菌），废水网络含**不动杆菌-假单胞菌**强连接 | 图5      |

## 操作步骤指南

### 1. 环境搭建
```bash
# 创建复现环境
conda create -n arg_reproduce python=3.8 r=4.1
conda activate arg_reproduce

# 安装依赖
pip install -r https://raw.githubusercontent.com/davidgllund/factors_influencing_HGT_of_ARGs/main/requirements.txt
