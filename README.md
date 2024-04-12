# KDD2024-Rebuttal

## We hope that the additional experimental results will address your concerns.

### Table 1: the disorder prediction performance of new baselines. (BraGCL and BRAINNETTF) 
| Methods       | HIV-fMRI(Acc) | HIV-fMRI(AUC) | HIV-DTI(Acc)  | HIV-DTI(AUC)  | BP-fMRI(Acc)  | BP-fMRI(AUC)  | BP-DTI(Acc)   | BP-DTI(AUC)   | ADHD(Acc)     | ADHD(AUC)     |
|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|
| BraGCL [1]       | 0.68±0.17     | 0.68±0.17     | 0.64±0.09     | 0.64±0.09     | 0.63±0.04     | 0.63±0.05     | 0.58±0.13     | 0.57±0.14     | 0.61±0.03     | 0.61±0.03     |
| BRAINNETTF [2]    | 0.71±0.10     | 0.80±0.11     | 0.78±0.09     | 0.82±0.07     | 0.57±0.08     | 0.57±0.15     | 0.49±0.07     | 0.56±0.14     | 0.56±0.06     | 0.64±0.03     |
| Ex(ours)      | 0.71±0.10     | 0.76±0.13     | 0.70±0.11     | 0.77±0.10     | 0.65±0.05     | 0.67±0.07     | 0.62±0.07     | 0.66±0.06     | 0.66±0.03     | 0.69±0.02     |
| BrainEx(ours) | **0.76±0.15** | **0.87±0.27** | **0.84±0.15** | **0.83±0.25** | **0.75±0.24** | **0.74±0.03** | **0.69±0.14** | **0.83±0.13** | **0.72±0.06** | **0.76±0.05** |

**Conclusion**: Our method still obtains the best performance compared with two new baselines.

[1] X. Luo, G. Dong, J. Wu, A. Beheshti, J. Yang, and S. Xue, “An interpretable brain graph contrastive learning framework for brain disorder analysis,” in Proceedings of the 17th ACM International Conference on Web Search and Data Mining, 2024, p. 1074–1077.

[2] X. Kan, W. Dai, H. Cui, Z. Zhang, Y. Guo, and C. Yang. Brain network transformer. Advances in Neural Information Processing Systems, 35:25586–25599, 2022.

### Table 2: the ablation study on BP and ADHD datasets.
| Variants    | BP-fMRI(Acc)  | BP-fMRI(AUC)  | BP-DTI(Acc)   | BP-DTI(AUC)   | ADHD(Acc)     | ADHD(AUC)     |
|-------------|---------------|---------------|---------------|---------------|---------------|---------------|
| ENG-Ex      | 0.60±0.06     | 0.61±0.06     | 0.51±0.10     | 0.51±0.08     | 0.63±0.04     | 0.65±0.04     |
| Ex-w/o(S)   | 0.58±0.07     | 0.60±0.06     | 0.49±0.08     | 0.45±0.15     | 0.62±0.05     | 0.65±0.05     |
| Ex-w/o(F)   | 0.58±0.07     | 0.60±0.05     | 0.50±0.10     | 0.44±0.16     | 0.62±0.04     | 0.64±0.05     |
| Ex-w/o(Sub) | 0.54±0.04     | 0.59±0.05     | 0.49±0.09     | 0.45±0.16     | 0.62±0.04     | 0.65±0.06     |
| Ex          | **0.65±0.05** | **0.67±0.07** | **0.62±0.07** | **0.66±0.06** | **0.66±0.03** | **0.69±0.02** |
 
**Conclusion**: the variants of Ex get worse performance on BP and ADHD datasets, which demonstrates the effectiveness of our designs.

### Table 3: The time cost comparison on three datasets. (here, because our method includes the pre-training process on larger source datasets and the test process on target task datasets, we report the test task time for our method.)
| Methods       | HIV-DTI(Sec) | BP-DTI(Sec) | ADHD(Sec) |
|---------------|--------------|-------------|-----------|
| BrainGNN      | 19.358       | 21.088      | 64.114    |
| IBGNN         | 44.532       | 51.299      | 243.492   |
| GIB           | 28.949       | 34.117      | 128.205   |
| BrainEx(ours) | 46.588       | 59.556      | 269.098   |

**Conclusion**: As shown in the table 3, our method does not represent too high time cost with other methods.

### Table 4: The interpretation comparison results with other methods on HIV. 
| Methods        | HIV (Salient ROI Comparison)                                                                                                                                           |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IBGNN          | Middle frontal gyrus, parahippocampal gyrus, cuneus, and amygdala.                                                                                                     |
| GIB            | Thalamus, medial and lateral cingulate gyrus, lenticular nucleus, and superior frontal gyrus.                                                                          |
| BrainEX (Ours) | Anterior cingulate, paracingulate gyrus, hippocampus, and inferior frontal gyrus.                                                                                      |
| **Analysis**   | Existing findings: Anterior cingulate, paracingulate gyri, inferior frontal gyrus, and parahippocampal gyrus. Our interpretation results are closer to the findings.   |

### Table 5: The interpretation comparison results with other methods on BP. 
| Methods        | BP (Salient ROI Comparison)                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------|
| IBGNN          | Visuo-motor coordination, superior temporal gyrus,  subdivision of retrosplenial cortex, and dorsal entorhinal cortex. |
| GIB            | Inferior temporal gyrus, ventromedial prefrontal cortex,  fusiform gyrus, and broca's area.                            |
| BrainEX (Ours) | Secondary visual cortex, visuo-motor coordination and orbitofrontal area.                                              |
| **Analysis**   | Existing findings: abnormal visual processing areas. Our interpretation results include more related areas.            |



### Table 6: The interpretation comparison results with other methods on ADHD. 
| Methods        | ADHD (Salient ROI Comparison)                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| IBGNN          | Middle frontal gyrus, orbital middle frontal gyrus, insula,  middle occipital gyrus, and superior temporal gyrus.                                   |
| GIB            | Precentral gyrus, medial and lateral cingulate gyrus, hippocampus, and angular gyrus.                                                               |
| BrainEX (Ours) | Inferior frontal gyrus, medial and lateral cingulate gyrus,  and cuneus, superior temporal gyrus, thalamus.                                         |
| **Analysis**   | Existing findings: thalamus, cortex, cingulate gyrus, amygdala, cerebellum. Interpretation results of BrainEx and GIB are closer to the findings.   |

**Conclusion**: In summary, the interpretable results provided by our method are better than other baselines and are closer to the existing findings. Here we spend much time providing salient brain region analysis, and the abnormal connection analysis still needs more time in traceability analysis, so it is not provided.
