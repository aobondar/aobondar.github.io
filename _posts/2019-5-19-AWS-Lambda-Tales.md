---
layout: post
title: 4 years with AWS Lambda (and why we left it behind)
---

In 2015 I was a CTO of a small startup, trying to figure out how to deal with horrifically growing size of our MVP, having only a team of two engineers. Our team has a lack of building production-ready web services, thus first experience of writing django-based backend was painful. So when we started a new product, I started digging for new backend-stack, that could help us move faster.

And by some twist of fate I fell in love with AWS Lambdas at that moment.

So the next four years we used to write REST services, based on Lambdas. Now I see, that more and more people thinks about using lambdas in production, so I want to warn them about caveeats, by telling the story of evolution of our homebrew lambda-based framework. And the long story short:

## Lambda is not a good generic choise for building REST-API

* We wanted to have **No-Ops envirenment**, but have to **write a complex homebrew framework** for deploying and monitoring

* We wanted to forget about **scaling issues**, but in fact we **had to always keep an eye on the load metrics**, and configure homebrew envirenment-controller software to meet our SLA's

* We wanted **to stay ignorant about system administration**, but in fact **had to learn too much details about proprietary AWS technologies**

* We get **vendor-locked** for a long time, and loose ability to leverage an open-source python toolchain. What to say, we even **didn't have a debugging tools**!


## But all this started with a great expectations and enthusiasm

{% include disqus.html %}
