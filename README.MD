<p align="center">
  <img src="./images/icon.jpg" alt="GPT4V for Generic Anomaly Detection" width="300" />
</p>

# Towards Generic Anomaly Detection and Understanding: Large-scale Visual-linguistic Model (GPT-4V) Takes the Lead.

[![License](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-red.svg)](LICENSE)

📃 [Read the Full Paper](https://arxiv.org/pdf/2311.02782)

Yunkang Cao*, Xiaohao Xu*, Chen Sun*, Xiaonan Huang, Weiming Shen.
(*These authors contribute equally.)

---

## Table of Contents

- [Introduction](#introduction)
- [Observations](#observations)
- [GPT-4V for Generic Anomaly Detection](#gpt-4v-for-generic-anomaly-detection)
- [Citation](#citation)
- [Acknowledgments](#acknowledgments)

---

## Introduction

Anomaly detection is a crucial task across different domains and data types. However, existing anomaly detection models are often designed for specific domains and modalities. This study explores the use of GPT-4V(ision), a powerful visual-linguistic model, to address anomaly detection tasks in a generic manner. We investigate the application of GPT-4V in multi-modality, multi-domain anomaly detection tasks, including image, video, point cloud, and time series data, across multiple application areas, such as industrial, medical, logical, video, 3D anomaly detection, and localization tasks. To enhance GPT-4V's performance, we incorporate different kinds of additional cues such as class information, human expertise, and reference images as prompts. Based on our experiments, GPT-4V proves to be highly effective in detecting and explaining global and fine-grained semantic patterns in zero/one-shot anomaly detection. This enables accurate differentiation between normal and abnormal instances. Overall, GPT-4V exhibits promising performance in generic anomaly detection and understanding, thus opening up a new avenue for anomaly detection.

**All cases and corresponding prompts for evaluations can be found in ``./Cases``.**

**The evaluations were conducted before November 7, 2023. GPT-4V has shown gradual improvement and may deliver even stronger performance in the future.**

---

## To-Do List

- [ ] Evaluate quantitative results
- [ ] Evaluate GPT-4V in multi-round conversations

---

## Observations

GPT-4V demonstrates robust anomaly detection capabilities in various multi-modal and multi-field tasks. It excels in comprehending image context, discerning normal standards, and comparing provided images effectively.

### GPT-4V can address multi-modality and multi-field anomaly detection tasks in zero/one-shot regime

- **Multi-Modality Anomaly Detection**: GPT-4V handles diverse data types like images, point clouds, and X-rays, making it adaptable to multi-modal tasks, surpassing single-modal detectors.

- **Multi-Field Anomaly Detection**: GPT-4V performs well in industrial, medical, pedestrian, traffic, and time series anomaly detection, showcasing its versatility across domains.

- **Zero/One-Shot Anomaly Detection**: GPT-4V adapts to different inference scenarios, utilizing language prompts for anomaly detection, with or without reference images.

### GPT-4V can understand both global and fine-grained semantics for anomaly detection

- **Global Semantics**: GPT-4V recognizes overarching abnormal patterns or behaviors, making it suitable for identifying anomalies in broader contexts, e.g., traffic anomaly detection.

- **Fine-Grained Semantics**: GPT-4V precisely localizes anomalies within complex data, enhancing its ability to detect subtle irregularities, e.g., industrial image anomaly detection.

### GPT-4V can automatically reason for anomaly detection

GPT-4V automatically reasons complex normal standards and provides explanations for detected anomalies. It adds interpretability to its results, making it valuable for understanding irregularities in various domains.

### GPT-4V can be enhanced with increasing prompts

Additional prompts improve GPT-4V's anomaly detection performance, responding to class information, human expertise, and reference images.

### GPT-4V can be constrained in real-world application but still promising

While GPT-4V shows promise, challenges exist in highly complex scenarios, such as industrial applications and ethical constraints in the medical field. Further enhancements and fine-tuning may be required to address these challenges and unlock its potential.

---

## GPT-4V for Generic Anomaly Detection

### Industrial Image Anomaly Detection

**Task Introduction**: Industrial image anomaly detection is a critical component of manufacturing processes aimed at upholding product quality. Following the establishment of the MVTec AD dataset, various methods have thrived in this field.

![Industrial Image Anomaly Detection](./images/industrial-ad-case1-zero-shot.png)
![Industrial Image Anomaly Detection](./images/industrial-ad-case1-one-shot.png)

### Industrial Image Anomaly Localization

**Task Introduction**: Industrial image anomaly localization entails a more intricate process than mere image anomaly detection. Its potential for image anomaly localization warrants further exploration.

![Industrial Image Anomaly Localization](./images/industrial-al-case1.png)
![Industrial Image Anomaly Localization](./images/industrial-al-case2.png)

### Point Cloud Anomaly Detection

**Task Introduction**: Geometrical information holds a crucial role in fields like industrial anomaly detection, especially when dealing with categories lacking textual information. In contrast, CPMF proposes a novel approach by transforming point clouds into depth images.

![Point Cloud Anomaly Detection](./images/pcd-ad-case1-zero-shot.png)
![Point Cloud Anomaly Detection](./images/pcd-ad-case1-one-shot.png)

### Logical Anomaly Detection

**Task Introduction**: In addition to structural anomalies, there exists another type of anomaly, named logical anomalies. Existing logical anomaly detection methods typically relied on solely visual context.

![Logical Anomaly Detection](./images/logical-ad-case1.png)
![Logical Anomaly Detection](./images/logical-ad-case2.png)

### Medical Image Anomaly Detection

**Task Introduction**: Anomaly detection in medical imaging is pivotal for early diagnosis and effective treatment planning. GPT-4V shows promising future in enhancing the performance of anomaly detection tasks in various medical imaging modalities.

![Medical Image Anomaly Detection](./images/Chest%20X-Ray%20Case_1.png)
![Medical Image Anomaly Detection](./images/Chest%20X-Ray%20Case_2.png)

### Medical Image Anomaly Localization

**Task Introduction**: Anomaly localization is imperative for clinicians to understand the extent and nature of the pathology.

![Medical Image Anomaly Localization](./images/Endoscopy%20Localization%20Case.png)

### Pedestrian Anomaly Detection

**Task Introduction**: Pedestrian anomaly detection is dedicated to recognizing irregular activities within pedestrian interactions captured in video streams.

![Pedestrian Anomaly Detection](./images/pedestrian-anomaly-detection-case1.png)

### Traffic Anomaly Detection

**Task Introduction**: Traffic anomaly detection aims at identifying the commencement and conclusion of abnormal events in traffic scenarios.

![Traffic Anomaly Detection](./images/traffic-anomaly-detection-case1.png)
![Traffic Anomaly Detection](./images/traffic-anomaly-detection-case2.png)

### Time Series Anomaly Detection

**Task Introduction:** Time series anomaly detection refers to the task of identifying unusual or abnormal patterns in sequential data over time.

![Time Series Anomaly Detection](./images/time-series-ad-case-1.png)
![Time Series Anomaly Detection](./images/time-series-ad-case-2.png)

For more details, please refer to the [document](https://arxiv.org/pdf/2311.02782).


### Citation

If you found this study useful in your research or applications, please kindly cite using the following BibTeX:

```bibtex
@article{cao2023genericad,
  title={Towards Generic Anomaly Detection and Understanding: Large-scale Visual-linguistic Model (GPT-4V) Takes the Lead},
  author={Yunkang Cao and Xiaohao Xu and Chen Sun and Xiaonan Huang and Weiming Shen},
  journal={arXiv preprint arXiv:2311.02782},
  year={2023}
}
```


---

### Acknowledgments

Our study is largely inspired by [GPT-4V](http://arxiv.org/abs/2309.17421), [GPT-4V for Medical](http://arxiv.org/abs/2310.09909), [SoM](http://arxiv.org/abs/2310.11441), [CPMF](https://arxiv.org/abs/2303.13194). Thanks for their wonderful work!

```bibtex
@article{yang2023dawnoflmms,
  title={The Dawn of LMMs: Preliminary Explorations with GPT-4V (ision)},
  author={Yang, Zhengyuan and Li, Linjie and Lin, Kevin and Wang, Jianfeng and Lin, Chung-Ching and Liu, Zicheng and Wang, Lijuan},
  journal={arXiv preprint arXiv:2309.17421},
  year={2023}
}

@article{yang2023SoM,
	title = {Set-of-Mark Prompting Unleashes Extraordinary Visual Grounding in {GPT}-4V},
	journal = {{arXiv preprint, arXiv}:2310.11441},
	year = {{2023}},
	author = {Yang, Jianwei and Zhang, Hao and Li, Feng and Zou, Xueyan and Li, Chunyuan and Gao, Jianfeng},
}

@article{liu2023hallusionbench,
  title={HallusionBench: You See What You Think? Or You Think What You See? An Image-Context Reasoning Benchmark Challenging for GPT-4V (ision), LLaVA-1.5, and Other Multi-modality Models},
  author={Liu, Fuxiao and Guan, Tianrui and Li, Zongxia and Chen, Lichang and Yacoob, Yaser and Manocha, Dinesh and Zhou, Tianyi},
  journal={arXiv preprint arXiv:2310.14566},
  year={2023}
}

@article{wu2023cangpt,
	title = {Can {GPT}-4V(ision) Serve Medical Applications? Case Studies on {GPT}-4V for Multimodal Medical Diagnosis},
author = {Wu, Chaoyi and Lei, Jiayu and Zheng, Qiaoyu and Zhao, Weike and Lin, Weixiong and Zhang, Xiaoman and Zhou, Xiao and Zhao, Ziheng and Zhang, Ya and Wang, Yanfeng and Xie, Weidi},
  journal={arXiv preprint arXiv:2310.09909},
  year={2023}
}

@article{cao2023cpmf,
	title = {Complementary Pseudo Multimodal Feature for Point Cloud Anomaly Detection},
	journal = {arXiv preprint arXiv:2303.13194},
	author = {Cao, Yunkang and Xu, Xiaohao and Shen, Weiming},
	year = 2023,
}


```

[![Star History Chart](https://api.star-history.com/svg?repos=caoyunkang/GPT4V-for-Generic-Anomaly-Detection&type=Date)](https://star-history.com/#caoyunkang/GPT4V-for-Generic-Anomaly-Detection&Date)
