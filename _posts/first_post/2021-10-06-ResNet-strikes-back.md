---
layout: post
title: 'ResNet strikes back: An improved training procedure in timm 논문 리뷰'
date: '2022-03-11 01:10:00 +0700'
tags:
  - Object Detection
  - ResNet
  - timm
description: test description
categories: jekyll update
published: true
comments: true
use_math: true
---


블로그 첫 글로 무슨 글을 쓸지 고민 하다가 논문 리뷰를 하기로 하고, 또 무슨 논문을 리뷰할까 찾아보다가 페이스북에서 **ResNet strikes back: An improved training procedure in timm** 이라는 논문이 나왔다는 게시글을 보고 논문을 살펴보았습니다. 

이 논문은 [pytorch-image-models github] (a.k.a timm)의 원작자인 Ross Wightman의 논문입니다. [Ross-Wightman-github] 에 들어가보니 소개글에 아래와 같이 적혀있었습니다. 개인적으로 깊이 감명 받았습니다. 

> Always learning, constantly curious. Building ML/AI systems, watching loss curves.

아무튼, 이 논문은 딥러닝 모델을 학습하는데 있어서 기본적이면서도 유용한 테크닉들이 잘 소개되어 있으며, 제안하는 학습방법을 적용해서 top-1 acc를 75.3%에서 80.4% 으로 끌어올렸다는 점에서 인상적이라 블로그 첫 게시물을 이 논문으로 정했습니다. 


Introduction

이미지 분류 분야 등에서 모델의 성능은 다음과 같이 정의됩니다. 

$ accuracy(model)=f(A, \tau , N) $

여기서 $$ A $$는 아키텍처 설계(architecture design), $$ T $$는 하이퍼파라미터(hyperparameters)같은 학습 설정(tranining setting), $$ N $$은 측정 노이즈(measurement noise)를 뜻합니다. 여기서 일반적으로 하이퍼파라미터 집합 또는 방법 선택에서 최대값을 선택할 때 발생하는 과적합(overfitting)도 포함됩니다. 또한 다른 시드(seeds)로 표준 편차(standard deviation)을 측정하거나, 별도의 평가 데이터 세트(evaluation dataset)을 사용하거나, 전이 작업(transfer tasks)에 대한 모델을 평가하는 것과 같이 노이즈 $$ N $$을 완화시키기 위한 몇 가지 사례들이 존재합니다. 





[timm-github]: https://github.com/rwightman/pytorch-image-models
[Ross-Wightman-github]: https://github.com/rwightman
[pytorch-image-models github]: https://github.com/rwightman/pytorch-image-models