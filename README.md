# FlexID
FlexID: Decoupling Identity and Extrinsic Facial Attributes in Zero-Shot Identity-Preserving Generation


## Introduction
Previous studies on identity-preserving image generation have often prioritized the restoration of intrinsic identity attributes, with insufficient attention given to extrinsic visual attributes such as glasses, hairstyles, tattoos, and face shapes, leading to degraded facial similarity.In this work we propose FlexID, a new solution based on diffusion models that significantly improves facial similarity between generated and reference images.We introduce a novel multi-attribute face representation method that leverages multi-modal features to learn hierarchical characteristics. Through a multi-stage learning approach, these features are mapped to distinct facial attribute spaces, resulting in rich facial embedding representations that aid in maintaining facial details during the generation process. Additionally, our multi-stage training strategy decouples the intrinsic ID attributes from extrinsic styling attributes, enabling independent control of facial posture, identity, and styling details through image prompts for image generation.Experimental results demonstrate that our method excels in generating consistency, successfully improving facial similarity from 72\% to 84\%. 

![framework](assets/images/framework.png)



## Application Summary
![app overview](assets/images/app_overview.png)


## Qualitative Analysis
![baselinecomp](assets/images/baselinecomp_v3.png)


## Quantitative Analysis
Quantitative comparison with different methods.The best result is shown in bold, and the second best is underlined. 'IPAdapter∗' refers to IPAdapter-faceID-plus-v2, while 'IPAdapter†'
denotes IPAdapter-faceID-Portrait-Unnormal. 'PuLID' represents the result of inference by PuLID v1 model on SDXL Lighting, while 'PuLID‡' represents the result of inference by PuLIDv1.1 on SDXL. Additionally, since UniPortrait does not have an open-source model, we tested 50 images using recommended parameters from the official demo to calculate similarity scores as a reference, yielding an FlexID similarity score of 0.85 for these images. Furthermore, we selected two works based on SD1.5 with high similarity scores as additional references; however, due to differences in the underlying models, we only calculated face similarity for comparison.
![quantitative analysis.png](assets/images/quantitative_analysis.png)


## Flexible Control
![other](assets/images/muscle_display.png)
