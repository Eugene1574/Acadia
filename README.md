# EnergAI: A Large Language Model–Driven Generative Design Method for Early-Stage Building Energy Optimization
Abstract: *Early-stage planning in architectural development strongly influences project quality, cost, and sustainability across the building life cycle. In practice, this stage involves multiple stakeholders, such as design, cost, market, engineering, and operations, whose objectives and information sources are often heterogeneous and difficult to coordinate. To address this challenge, this paper proposes PlanGPT-MAS, a multi-agent large language model framework for early-stage decision-making in complex architectural development. First, we construct ArchPlan-Multimodal, a multimodal dataset based on 120 real residential development cases, integrating textual documents and architectural drawings across design, cost, market, construction, and operations. Second, we develop a multi-agent framework that combines retrieval-augmented generation, Actor-Critic weight optimization, and multi-round negotiation to support dynamic objective balancing and explainable decision-making. Third, experiments including baseline comparison, ablation studies, robustness analysis, and expert evaluation demonstrate the effectiveness of the proposed method. PlanGPT-MAS achieves an average expert-reference alignment score of 0.8410, outperforming EqualWeight by 3.57% and RandomWeight by 11.96%. This automated metric indicates stronger consistency with expert-annotated planning references, while blind expert evaluation is further used to assess the design quality of the generated schemes in terms of feasibility, coordination, interpretability, and professional acceptability, providing an interpretable and scalable pathway for human–AI collaboration in architectural development..*


[**Paper**]() | [**Project Page**]() | [**Model Weights**]() | [**Huggingface Demo**]() |


*Figure 1) Examples of design schemes and corresponding annotations in the dataset*
![img](figure/figure1.png)

*Figure 2) EnergAI closed-loop iterative workflow of parametric input, LLM prompting, performance simulation, and semantic feedback.*
![img](figure/figure2.png)

*Figure 3) Experimental site.*
![img](figure/figure3.png)

*Figure 4) Scatter plot of annual EUI vs. annual energy cost for the human-designed model and the geometry-oriented LLM-designed model.*
![img](figure/figure4.png)

*Figure 5) Impact of climate information on EUI and energy cost.*
![img](figure/figure5.png)

*Figure 6) Impact of design strategy on EUI.*
![img](figure/figure6.png)

*Figure 7)  Impact of design strategy on energy cost.*
![img](figure/figure7.png)

*Figure 8) Wordclouds.*
![img](figure/figure8.png)

*Figure 9) Mean energy-saving rate versus the number of prompt dimensions. *
![img](figure/figure9.png)



## Table

*Parameter ranges and corresponding regulatory or empirical references defining the feasible constraint space Ω (Beijing, ASHRAE Zone 4)*
![img](figure/table1.png)

*Statistics of the influence of different prompt dimensions on EUI saving rate (EUI saving rate = (Baseline EUI – Current EUI) / Baseline EUI).*
![img](figure/table2.png)



## TODO List

- [x] Release part of LowEnergy-FormNet dataset. 
- [ ] Release EnergAI code and pretrain weights.
- [ ] Upload EnergAI training dataset.




## Inference

```
python EnergAI_Infer.py --dataset LowEnergy-FormNet --model_path ckpts/EnergAI/model_final.pt --prompt_strategy performance-oriented
```
## Train

```
python EnergAI_Train.py --dataset LowEnergy-FormNet --batch_size 32 --prompt_strategy geometry-oriented
```

