```mermaid

flowchart TD
    H0[设立原假设 H0<br/>无罪推定]
    H1[设立备择假设 Ha<br/>有罪主张]
    Data[收集样本数据]
    Calc[计算检验统计量<br/>Z 或 T]
    Pval[计算 P-value<br/>假设 H0 为真时<br/>出现当前证据的概率]
    Compare{P-value < α?<br/>通常α=0.05}
    Reject[拒绝 H0<br/>证据充分]
    Fail[不拒绝 H0<br/>证据不足]
    
    H0 --> Data --> Calc --> Pval --> Compare
    H1 -.-> Compare
    Compare -->|是 | Reject
    Compare -->|否 | Fail
    
    style H0 fill:#1e3a5f,stroke:#4a9eff,stroke-width:2px,color:#ffffff
    style H1 fill:#1e3a5f,stroke:#4a9eff,stroke-width:2px,color:#ffffff
    style Data fill:#1e4f3a,stroke:#4aff9e,stroke-width:2px,color:#ffffff
    style Calc fill:#1e4f3a,stroke:#4aff9e,stroke-width:2px,color:#ffffff
    style Pval fill:#5f4a1e,stroke:#ffcc4a,stroke-width:2px,color:#ffffff
    style Compare fill:#2d2d2d,stroke:#cccccc,stroke-width:2px,color:#ffffff
    style Reject fill:#4f1e3a,stroke:#ff4a9e,stroke-width:2px,color:#ffffff
    style Fail fill:#1e3a5f,stroke:#4a9eff,stroke-width:2px,color:#ffffff
```
```mermaid
flowchart TD
    subgraph CI[置信区间]
        direction TB
        CI1[构建区间]
        CI2[网在动<br/>真值不动]
        CI3[95% = 100 次<br/>95 个网捕获真值]
        CI1 --> CI2 --> CI3
    end
    
    subgraph HT[假设检验]
        direction TB
        HT1[假设 H0 为真]
        HT2[算 P-value]
        HT3[P<α则拒绝 H0]
        HT1 --> HT2 --> HT3
    end
    
    CI ~~~ HT
    Link[本质相同<br/>角度不同]
    CI -.-> Link
    HT -.-> Link
    
    style CI fill:#1e4f3a,stroke:#4aff9e,stroke-width:2px,color:#ffffff
    style HT fill:#5f4a1e,stroke:#ffcc4a,stroke-width:2px,color:#ffffff
    style Link fill:#2d2d2d,stroke:#cccccc,stroke-width:2px,color:#ffffff
    style CI1 fill:#1e4f3a,stroke:#4aff9e,stroke-width:1px,color:#ffffff
    style CI2 fill:#1e4f3a,stroke:#4aff9e,stroke-width:1px,color:#ffffff
    style CI3 fill:#1e4f3a,stroke:#4aff9e,stroke-width:1px,color:#ffffff
    style HT1 fill:#5f4a1e,stroke:#ffcc4a,stroke-width:1px,color:#ffffff
    style HT2 fill:#5f4a1e,stroke:#ffcc4a,stroke-width:1px,color:#ffffff
    style HT3 fill:#5f4a1e,stroke:#ffcc4a,stroke-width:1px,color:#ffffff
```
```mermaid
graph LR
    Pop[总体 Population<br/>参数：μ, σ<br/>通常未知]
    Sample[样本 Sample<br/>统计量：x̄, s<br/>可以计算]
    Sampling[抽样分布 
    Sampling Distribution<br/>所有可能样本统计量的分布]
    
    Pop -->|抽取 | Sample
    Sample -->|重复多次 | Sampling
    
    subgraph CLT[中心极限定理 CLT]
        CLT1[无论总体形状如何]
        CLT2[只要 n 足够大]
        CLT3[样本均值的分布趋近正态]
        CLT1 --> CLT2 --> CLT3
    end
    
    Sampling --> CLT
    
    style Pop fill:#1e3a5f,stroke:#4a9eff,stroke-width:2px,color:#ffffff
    style Sample fill:#5f4a1e,stroke:#ffcc4a,stroke-width:2px,color:#ffffff
    style Sampling fill:#1e4f3a,stroke:#4aff9e,stroke-width:2px,color:#ffffff
    style CLT fill:#4f1e3a,stroke:#ff4a9e,stroke-width:3px,color:#ffffff
    style CLT1 fill:#4f1e3a,stroke:#ff4a9e,stroke-width:1px,color:#ffffff
    style CLT2 fill:#4f1e3a,stroke:#ff4a9e,stroke-width:1px,color:#ffffff
    style CLT3 fill:#4f1e3a,stroke:#ff4a9e,stroke-width:1px,color:#ffffff
```