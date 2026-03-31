graph LR
    Core[("统计学核心<br/>样本推测总体 + 量化不确定性")]
    
    subgraph P1[Phase 1: 模式与建模]
        P1Q[核心问题: 数据长什么样？]
        P1C[关键概念: 形状/中心/离散/正态/Z-score]
        P1I[核心直觉: 模型是给乱数据的一把尺]
        P1Ch[教材: Ch 1,2,3,6]
    end
    
    subgraph P2[Phase 2: 随机性的桥梁 ⭐]
        P2Q[核心问题: 样本统计量如何变化？]
        P2C[关键概念: 抽样分布/CLT/标准误]
        P2I[核心直觉: 大样本让随机性可预测]
        P2Ch[教材: Ch 4,5,7]
    end
    
    subgraph P3[Phase 3: 判决与推断]
        P3Q[核心问题: 结论有多可靠？]
        P3C[关键概念: CI/假设检验/P值/Z vs T]
        P3I[核心直觉: 用概率语言做有依据的判断]
        P3Ch[教材: Ch 8,9,10]
    end
    
    Core --> P1
    Core --> P2
    Core --> P3
    
    style P2 fill:#fff9c4,stroke:#fbc02d,stroke-width:3px
    style Core fill:#e3f2fd,stroke:#1976d2,stroke-width:2px