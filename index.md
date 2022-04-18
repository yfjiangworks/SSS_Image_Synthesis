![Image](resources/fig1.png)
<p align="center">
The SSS image synthesis process. The left part depicts the training procedure while right part shows the testing procedure. The model is divided into three main sections: the image feature extractor, the generator, and the discriminator. The black solid arrow represents the data flow from the real image to the synthesized image, before moving from the discriminator to a region-based decision. The black dotted arrows represent the navigation process for multi-scale semantic segmentation maps. We mark the inputs and outputs of training procedures in blue.
</p>


# Abstract
Side-scan sonar (SSS) is a critical sensor device used to explore underwater environments in the deep sea. Gathering SSS data, however, is an expensive and time-consuming task because it requires sensor towing and involves complicated field operations.  Recently, deep learning has been making advances rapidly in the field of computer vision. Benefiting from this development, generative adversarial networks (GANs) have been demonstrated to produce realistic synthetic data of various types, including images and acoustics signals. In this paper, we propose a GAN-based semantic image synthesis model based on generative adversarial network that can generate high-quality SSS images at a low cost in less time. We evaluate the proposed model using both shallow and deep water SSS datasets that include a diverse range of imaging conditions such as high and low sonar operating frequencies and different landscapes. The experimental results show that the proposed method can effectively generate synthesized SSS data characterized by the shape and style of real data, thereby demonstrating its promising potential for SSS data augmentation in diverse SSS relevant machine learning tasks.

# Overview
In this paper, we formulate the SSS data generation problem as a semantic image synthesis task. The synthesis procedure starts from a random vector ***z*** that obeys the Gaussian distribution of a real image. Random vector ***z*** is then passed to generator network ***G*** to upsample the noise and collect detailed information (e.g., seabed landscape and shadows) from the real SSS image. During the generation process, a segmentation map is used to guide the synthesis of the details. Figure above shows the synthesis process with generator ***G***.
The proposed method follows the general concept of SPADE \cite{park2019semantic}, which consists of three components: a pixel distribution predictor, a generator, and a discriminator. 


# Synthetic SSS image samples
![Image](resources/fig2.png)
<p align="center">
Overview of the proposed method.
</p>

![Image](resources/fig3.png)
<p align="center">
SSS object image samples generated under high (left) and low (right) operational frequencies. The first row presents the segmentation maps that pass through the proposed method as input (black pixels: seabed; blue pixels: highlighted area; green pixels: shadows). The second row shows the original SSS images and the third row displays the SSS images generated using the proposed method.
</p>

# Acknowlegements
This work was funded by the Agency for Defense Development of Korea under Grant UD190005DD.

# Citation
```
@article{jiang2020side,
  title={Side-Scan Sonar Image Synthesis Based on Generative Adversarial Network for Images in Multiple Frequencies},
  author={Jiang, Yifan and Ku, Bonhwa and Kim, Wanjin and Ko, Hanseok},
  journal={IEEE Geoscience and Remote Sensing Letters},
  volume={18},
  number={9},
  pages={1505--1509},
  year={2020},
  publisher={IEEE}
}
```
