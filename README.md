# RMP-YOLO: A Robust Motion Predictor for Partially Observable Scenarios even if You Only Look Once

**Authors**: Jiawei Sun, Jiahui Li,  Tingchen Liu, Chengran Yuan, Shuo Sun, Zefan Huang and Marcelo H. Ang Jr.
**Rank 3rd** on 2024 Waymo Motion Prediction Competition

## Abstract
We introduce RMP-YOLO, a unified framework designed to provide robust motion predictions even with incomplete input data. 
Our key insight stems from the observation that complete and reliable historical trajectory data plays a pivotal role in ensuring accurate motion prediction. Therefore, we propose a new paradigm that prioritizes the reconstruction of intact historical trajectories before feeding them into the prediction modules. Our approach introduces a novel scene tokenization module to enhance the extraction and fusion of spatial and temporal features. Following this, our proposed recovery module reconstructs agents' incomplete historical trajectories by leveraging local map topology and interactions with nearby agents. The reconstructed, clean historical data is then integrated into the downstream prediction modules. Our framework is able to effectively handle missing data of varying lengths and remains robust against observation noise, while maintaining high prediction accuracy. Furthermore, our recovery module is compatible with existing prediction models, ensuring seamless integration. Extensive experiments validate the effectiveness of our approach, and deployment in real-world autonomous vehicles confirms its practical utility. In the 2024 Waymo Motion Prediction Competition, our method, RMP-YOLO, achieves state-of-the-art performance, securing third place.


## Introduction
we introduce a simple MLP-based recovery module combined with one layer of local attention transformer to reconstruct the historical trajectories. Our contributions are summarized as follows:
- We introduce RMP-YOLO, a novel framework that prioritizes reconstructing agents' incomplete historical trajectories by leveraging local map topology and agent interactions. This reconstruction process effectively handles varying lengths of missing data, ensuring robustness against noise and incomplete observations.
- The recovery module we propose is simple and lightweight. Moreover, it integrates seamlessly with existing motion prediction models, enhancing their robustness without the need for extensive modifications.
- Our method won third place in the 2024 Waymo Motion Prediction Competition. We deploy our algorithms on real vehicles to validate the effectiveness of our methods. We will open-source our code to support the robotics community after the paper is accepted. 


## Results
！[Visualization Results](visualizationi.png "viualization")

## Citation
If you find this paper useful, please cite it as:
```bibtex
@misc{sun2024rmpyolorobustmotionpredictor,
      title={RMP-YOLO: A Robust Motion Predictor for Partially Observable Scenarios even if You Only Look Once}, 
      author={Jiawei Sun and Jiahui Li and Tingchen Liu and Chengran Yuan and Shuo Sun and Zefan Huang and Anthony Wong and Keng Peng Tee and Marcelo H. Ang Jr},
      year={2024},
      eprint={2409.11696},
      archivePrefix={arXiv},
      primaryClass={cs.RO},
      url={https://arxiv.org/abs/2409.11696}, 
}
