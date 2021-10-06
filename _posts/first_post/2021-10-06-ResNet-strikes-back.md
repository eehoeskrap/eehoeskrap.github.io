---
layout: post
title:  "ResNet strikes back: An improved training procedure in timm 논문 리뷰"
date:   2021-10-06 19:54:00 +0700
tags: [javascript, react]
description: test description
categories: jekyll update
---


블로그 첫 글로 무슨 글을 쓸지 고민 하다가 논문 리뷰를 하기로 하고, 또 무슨 논문을 리뷰할까 찾아보다가
페이스북에서 ResNet strikes back: An improved training procedure in timm 이라는 논문이 나왔다는 게시글을 보고 논문을 살펴보았다.

이 논문은 pytorch-image-models github[timm-github] (a.k.a timm)의 원작자인 Ross Wightman의 논문이다.
Ross Wightman github[Ross-Wightman-github] 에 들어가보니 소개글에 아래와 같이 적혀있었는데, 진짜 멋있다.
'Always learning, constantly curious. Building ML/AI systems, watching loss curves.'

아무튼, 이 논문은 딥러닝 모델을 학습하는데 있어서 기본적이면서도 유용한 테크닉들이 잘 소개되어 있으며, 
제안하는 학습방법을 적용해서 top-1 acc를 75.3%에서 80.4% 으로 끌어올렸다는 점에서 인상적이라 블로그 첫 게시물을 이 논문으로 정했다!






[timm-github]: https://github.com/rwightman/pytorch-image-models
[Ross-Wightman-github]: https://github.com/rwightman



블로그를 다시 개설하게 되었습니다. 이 글은 `테스트` 를 위한 페이지 입니다. 
```
코드 테스트
```

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

참고자료 링크 테스트 [Jekyll docs][jekyll-docs]  

[jekyll-docs]: https://eehoeskrap.github.io/
