---
title: "[TCC] Proposta do Projeto"
date: 2026-06-18 18:00:00 +/-0300
categories: [TCC, Proposta Inicial]
tags: [Machine Learning, YOLO, Astronomy, Detecção de Objetos, AI]
---

Fernando Gouveia Lima\\
Orientadora: Nina S. T. Hirata

### Introdução 

Os grandes levantamentos astronômicos realizados revolucionaram a forma como o Universo é estudado. Projetos observacionais modernos produzem milhões de imagens de objetos celestes, tornando inviável a análise manual. Nesse contexto, técnicas de Aprendizado de Máquina e Visão Computacional passaram a desempenhar um papel fundamental na automatização de tarefas como detecção e classificação de objetos astronômicos.

Entre esses levantamentos destaca-se o Legacy Survey, que disponibiliza imagens multibanda. A disponibilidade dessas diferentes bandas fornece informações complementares sobre a composição física e espectral dos objetos observados, permitindo que modelos computacionais explorem características que não estão presentes em imagens RGB tradicionais.

Este trabalho propõe o desenvolvimento e treinamento de modelos da família YOLO para detecção e classificação de galáxias utilizando imagens multibanda provenientes do Legacy Survey. O objetivo central é investigar o potencial das informações espectrais fornecidas pelas diferentes bandas na identificação de morfologias, como galáxias elípticas e espirais, comparando diferentes arquiteturas e estratégias de representação dos dados. Também com o intuito de melhorar o desempenho e métricas como *Mean Average Precision* (mAP), precisão, etc.

Além da avaliação quantitativa, o projeto pretende realizar uma análise qualitativa dos modelos treinados por meio de técnicas de interpretabilidade (Grad-CAM). Também serão extraídos os embeddings gerados pelas redes neurais, possibilitando a visualização do espaço de características através de técnicas de redução de dimensionalidade, como UMAP ou t-SNE, com o objetivo de investigar como diferentes classes morfológicas se organizam no espaço latente aprendido pelo modelo.

Como extensão do trabalho, pretende-se explorar aplicações adicionais desses embeddings, como a detecção de anomalias ou relação de similaridade entre galáxias. Além disso, comparar diferentes arquiteturas quanto ao seu desempenho, custo computacional e capacidade de generalização.

### Metodologia

Inicialmente, será realizada uma revisão da literatura sobre detecção e classificação morfológica de galáxias, com foco em trabalhos que utilizam imagens multibanda e modelos da família YOLO.

Em seguida, serão utilizadas imagens do Legacy Survey contendo galáxias com classificação morfológica conhecida, priorizando galáxias espirais e elípticas. As imagens serão organizadas de forma a preservar as diferentes bandas espectrais, permitindo comparar estratégias de representação dos dados.

Depois, será realizado o pré-processamento das imagens, incluindo normalização, geração das anotações para treinamento, balanceamento entre classes e técnicas de aumento de dados (data augmentation), visando melhorar a capacidade de generalização dos modelos.

Posteriormente, serão treinados modelos da família YOLO para realizar a detecção e classificação das galáxias. Diferentes arquiteturas, configurações de treinamento e estratégias de utilização das bandas espectrais serão comparadas, buscando identificar aquelas que apresentam melhor desempenho.

Os modelos serão avaliados utilizando métricas como Mean Average Precision (mAP), precisão, revocação e F1-score, além de aspectos como tempo de inferência, custo computacional e capacidade de generalização.

Também serão empregadas técnicas de interpretabilidade, como Grad-CAM, para analisar quais regiões das imagens mais influenciam as decisões dos modelos. Por fim, serão extraídos os embeddings gerados pelas redes neurais e visualizados por meio de técnicas como UMAP e t-SNE, permitindo investigar a organização das diferentes classes morfológicas no espaço latente. Como estudo exploratório, pretende-se avaliar a utilização desses embeddings em tarefas como busca por similaridade entre galáxias e detecção de anomalias.

### Cronograma

As atividades planejadas estão divididas em três períodos (T1, T2 e T3)

| Atividade                                                   | T1 (Meses 1-3) | T2 (Meses 4-6) | T3 (Meses 7-9) |
| :---------------------------------------------------------- | :------------: | :------------: | :------------: |
| Revisão da literatura e de modelos YOLO                     |       ●        |       ●        |                |
| Estudo do Legacy Survey e preparação do conjunto de dados   |       ●        |       ●        |                |
| Treinamento e Experimentos                                  |                |       ●        |       ●        |
| Ánalise de métricas e Comparação dos Modelos                |                |       ●        |       ●        |
| Extração e visualização dos embeddings e Interpretabilidade |                |                |       ●        |
| Estudo exploratório                                         |                |                |       ●        |
| Escrita da monografia e preparação da apresentação          |                |       ●        |       ●        |

### Referências Bibliográficas

Abaixo, apresentamos uma bibliografia inicial para o projeto. Alguns textos possivelmente não sendo utilizados e outros novos sendo adicionados.

[1] A. Dey et al., "Overview of the DESI Legacy Imaging Surveys," The Astronomical Journal, vol. 157, no. 5, p. 168, 2019.

[2] G. Jocher and J. Qiu, "Ultralytics YOLO11," 2024. [Online]. Available: https://github.com/ultralytics/ultralytics

[3] S. Dieleman, K. W. Willett, and J. Dambre, "Rotation-invariant Convolutional Neural Networks for Galaxy Morphology Prediction," Monthly Notices of the Royal Astronomical Society, vol. 450, no. 2, pp. 1441–1459, 2015.

[4] L. van der Maaten and G. Hinton, "Visualizing Data using t-SNE," Journal of Machine Learning Research, vol. 9, pp. 2579–2605, 2008.

[5] D. Baron, "Machine Learning in Astronomy: A Practical Overview," 2019. [Online]. Available: https://arxiv.org/abs/1904.07248

[6] M. Ntampaka et al., "The Role of Machine Learning in the Next Decade of Cosmology," Bulletin of the American Astronomical Society, vol. 51, no. 3, 2019.

[7] R. R. Selvaraju et al., "Grad-CAM: Visual Explanations from Deep Networks via Gradient-based Localization," in Proceedings of the IEEE International Conference on Computer Vision (ICCV), 2017.
