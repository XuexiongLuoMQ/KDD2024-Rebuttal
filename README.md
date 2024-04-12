# KDD2024-Rebuttal

## We hope that the additional experimental results will address your concerns.

### Table 1 (the disorder prediction performance of new baselines (BraGCL and BRAINNTTF) )
| Methods       | HIV-fMRI(Acc) | HIV-fMRI(AUC) | HIV-DTI(Acc)  | HIV-DTI(AUC)  | BP-fMRI(Acc)  | BP-fMRI(AUC)  | BP-DTI(Acc)   | BP-DTI(AUC)   | ADHD(Acc)     | ADHD(AUC)     |
|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|
| BraGCL [1]       | 0.68±0.17     | 0.68±0.17     | 0.64±0.09     | 0.64±0.09     | 0.63±0.04     | 0.63±0.05     | 0.58±0.13     | 0.57±0.14     | 0.61±0.03     | 0.61±0.03     |
| BRAINNETTF [2]    | 0.71±0.10     | 0.80±0.11     | 0.78±0.09     | 0.82±0.07     | 0.57±0.08     | 0.57±0.15     | 0.49±0.07     | 0.56±0.14     | 0.56±0.06     | 0.64±0.03     |
| Ex(ours)      | 0.71±0.10     | 0.76±0.13     | 0.70±0.11     | 0.77±0.10     | 0.65±0.05     | 0.67±0.07     | 0.62±0.07     | 0.66±0.06     | 0.66±0.03     | 0.69±0.02     |
| BrainEx(ours) | **0.76±0.15** | **0.87±0.27** | **0.84±0.15** | **0.83±0.25** | **0.75±0.24** | **0.74±0.03** | **0.69±0.14** | **0.83±0.13** | **0.72±0.06** | **0.76±0.05** |
Conclusion: Our method still obtain the best perfromance compared with two new baselines.
[1] X. Luo, G. Dong, J. Wu, A. Beheshti, J. Yang, and S. Xue, “An interpretable brain graph contrastive learning framework for brain disorder analysis,” in Proceedings of the 17th ACM International Conference on Web Search and Data Mining, 2024, p. 1074–1077.
[2] X. Kan, W. Dai, H. Cui, Z. Zhang, Y. Guo, and C. Yang. Brain network transformer. Advances in Neural Information Processing Systems, 35:25586–25599, 2022.
