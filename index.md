![Image](resources/fig2.gif)

![Image](resources/fig3.gif)
<p align="center">
Two examples of synthetic action sequences. Upper sequence indicates the Cough action category, while below sequence indicates the Blow nose action category.
</p>


# Abstract

Over the past two years, Coronavirus disease 2019 (COVID-19) caused a significant loss on both the economy and public health. As a result, researchers began to notice the importance of detecting a novel disease at an early stage. Leveraging from the rapid development of artificial intelligence (AI), many AI-based COVID-19 detection approaches have been presented recently. However, a well-trained AI model always demands high-quality and sufficient data, which is hard to obtain during an early spreading stage of the novel disease. In this paper, we present a novel skeleton-based action synthesis method, which can effectively generate high-quality and diverse sequential actions corresponding to the most common COVID-19 symptoms. In order to obtain synthetic action sequences, we propose a GAN inversion method that can generate a series of synthetic action sequences by editing a real action sequence. We evaluate the proposed method on a well-known action recognition dataset in two levels: skeleton quality and action recognition.  The results show that our method outperforms the baseline approaches, and it can also be effectively deployed to action recognition modules with significant performance improvement. 

# Overview

![Image](resources/fig1.png)
<p align="center">
Overview of the proposed method. Subfigure (a) indicates the original StyleGAN2 generation approach. Subfigure (b) indicates the proposed method.
</p>


We introduce the proposed method in this section with details. In above figure, we demonstrate the overview of the proposed method and compare it to the original StyleGAN2 generation approach. Basically, a traditional StyleGAN2 generation process starts from sampling a latent vector ***z*** from latent space ***Z*** and map it into latent vector ***w*** with a mapping network ***F(•)***. Then, generator ***G(•)*** takes both latent vector ***w*** and random noise vector ***n*** and synthesizes a fake skeleton image. The drawback of the traditional StyleGAN2 generation process is that it is not controllable for certain action categories, for instance, coughing and blowing the nose. Comparing to the traditional StyleGAN2 generation process, the proposed method takes a reference input of a real skeleton image. Rather than generating a fake image with a random category, the proposed method can generate synthetic images with a certain category that is conditioned by the reference input.

# Acknowlegements
This research work is supported by the Air Force Office of Scientific Research under award number FA2386-19-1-4001.  
