# Welcome

![Cover](Figures/Fig_1.jpg)

The PigeonSuperModel is an open source repository of multiple pre-trained deep-learning models for markerless pose tracking in pigeons. We provide pre-trained weights for different ResNet and UNet models to be used in [DeepLabCut](https://deeplabcut.github.io/DeepLabCut) and [SLEAP](https://sleap.ai/), as well as a manually labeled dataset with 1151 frames to train and evaluate further models.

## Why a PigeonSuperModel?

Advances in computational neuroethology and markerless pose estimation are making it ever easier for researchers to quantify animal behavior from non-invasive video recordings. Yet, these models still rely on specialized hardware (particularly GPUs) for heavier computations, and model training usually take several days (which makes cloud solutions such as colab impractical). A further downside is the (yet) missing standards for video recording and analysis, which makes reproducibility across labs somewhat tricky.

With this PigeonSuperModel we provide multiple pre-trained neural networks for out-of-the-box video analysis of pigeon behavior. Using a shared PigeonSuperModel across labs, we advocate for a standardized set of markers for pigeon tracking and generalizable models across experiments, animals, and camera views.

We make our dataset openly available with 1151 manually labeled video frames of different pigeons in different settings, recorded from multiple camera views. We also provide multiple pre-trained models for popular markerless tracking software (i.e., [DeepLabCut](https://deeplabcut.github.io/DeepLabCut) and [SLEAP](https://sleap.ai/)) to be used out-of-the-box on your own data without additional configurations. We originally trained these models to generalize well across different experimental setups, using different cameras and different animals. Nonetheless, we found that these pre-trained models can be easily re-trained on outlier frames to specialize on any particular data set, if needed.

## Dataset

The dataset we provide consists of 1151 manually labeled frames from 4 different experiments and depicts single animals in various poses captured in different experimental setups. It is especially well balanced to generalize to new videos. We originally designed it to train neural networks (e.g. using DeepLabCut or SLEAP) for video analysis via markerless pose estimation in pigeons. It can also be used for 3D pose reconstruction in multi-camera setups using e.g., [Anipose](https://anipose.readthedocs.io/en/latest/index.html). [Read more](Dataset.md).

## Models

Using this dataset, we trained multiple DeepLabCut models based on different architectures (`resnet-50`, `resnet-101`, `resnet-152`) and compared tracking performance across different training stages. We make the final, pre-trained models available for out-of-the-box analysis of new videos. Moreover, we used the same dataset to train `UNet` models in SLEAP and benchmark performance differences, training and inference rates. [Read more](Models.md).

## Tutorial

To wrap it all up, we provide some further instructions on how to make use of our pre-trained models in either DeepLabCut or SLEAP, including a section on how to re-train these models to your specific experimental setup. We also guide you through the entire process in DeepLabCut and SLEAP with beginner friendly jupyter notebooks. [Read more](Tutorial.md).

## Content

* [Dataset](Dataset.md)
* [Models](Models.md)
* [Tutorial](Tutorial.md)
* [Get in Touch](GetInTouch.md)

## Open Source License

This is an open source project and we want to actively encourage you to use it as a resource for your work. For questions or feedback please use the `Issues` feature of GitLab [here](https://gitlab.ruhr-uni-bochum.de/ikn/pigeonsupermodel/-/issues). We are happy to help you out setting up your own project. The copyright remains with the [Institute of Cognitive Neuroscience](https://www.ikn.psy.ruhr-uni-bochum.de/indexE.html).

## Reference

If you find either the dataset or the pre-trained models provided in the PigeonSuperModel to be useful for your research, please cite:
> Hidalgo-Gadea, G., Möser, S.C., ... & Güntürkün, O. (2022). In preparation

## Contributors

The PigeonSuperModel is a group effort by the entire [Biopsychology Team](https://www.ruhr-uni-bochum.de/biopsy/members.html) with the Institute of Cognitive Neuroscience (IKN) at the Ruhr-University Bochum. The project originated from common interest in using machine learning for animal tracking, which led us to create a common video dataset from multiple experiments within the lab. Guillermo Hidalgo Gadea and Sarah C. Möser curated the dataset and trained the PigeonSuperModel. [Read more](GetInTouch.md).

Multiple researchers from the department contributed to this dataset. A special thank you goes to [Noemi Rook](https://www.ruhr-uni-bochum.de/biopsy/members_noemi.html), [Neslihan Wittek](https://www.ruhr-uni-bochum.de/biopsy/members_neslihan.html), [John M. Tuff](https://www.ruhr-uni-bochum.de/biopsy/members_john.html), [Mengmeng Li](https://www.bio.psy.ruhr-uni-bochum.de/members_mengmeng.html) and [Celil S. Sevincik](https://www.ruhr-uni-bochum.de/biopsy/members_semih.html).

## Funding

This work was carried out at the Institute of Cognitive Neuroscience (IKN), Department of Biopsychology at the Ruhr-University Bochum and supported by the Deutsche Forschungsgemeinschaft DFG (German Research Foundation) through SFB 1372 project number 395940726, subproject Neu06, as well as in the context of funding the Research Training Group “Situated Cognition” (GRK 2185/1).
