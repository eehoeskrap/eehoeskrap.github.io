---
layout: post
title: 'ResNet strikes back: An improved training procedure in timm 논문 리뷰'
date: '2021-10-06 19:54:00 +0700'
tags:
  - Object Detection
  - ResNet
description: test description
categories: jekyll update
published: true
comments: true
use_math: true
---


블로그 첫 글로 무슨 글을 쓸지 고민 하다가 논문 리뷰를 하기로 하고, 또 무슨 논문을 리뷰할까 찾아보다가 페이스북에서 **ResNet strikes back: An improved training procedure in timm** 이라는 논문이 나왔다는 게시글을 보고 논문을 살펴보았습니다. 

이 논문은 [pytorch-image-models github] (a.k.a timm)의 원작자인 Ross Wightman의 논문입니다. [Ross-Wightman-github] 에 들어가보니 소개글에 아래와 같이 적혀있었습니다. 개인적으로 깊이 감명 받았습니다. 

__Always learning, constantly curious. Building ML/AI systems, watching loss curves.

아무튼, 이 논문은 딥러닝 모델을 학습하는데 있어서 기본적이면서도 유용한 테크닉들이 잘 소개되어 있으며, 제안하는 학습방법을 적용해서 top-1 acc를 75.3%에서 80.4% 으로 끌어올렸다는 점에서 인상적이라 블로그 첫 게시물을 이 논문으로 정했습니다. 


Introduction

이미지 분류 분야 등에서 모델의 성능은 다음과 같이 정의됩니다. 

accuracy(model)=f(A, \tau , N)






[timm-github]: https://github.com/rwightman/pytorch-image-models
[Ross-Wightman-github]: https://github.com/rwightman
