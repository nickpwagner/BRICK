---
id: 563dde44-ef5a-4bee-b081-535687057b47
---

___
# Introduction to Neural Networks — Part 1 | by Harsha Bommana | Deep Learning Demystified | Medium

**Links**: [Omnivore](https://omnivore.app/me/introduction-to-neural-networks-part-1-by-harsha-bommana-deep-le-18aa36f3c55) |  [Web](https://medium.com/deep-learning-demystified/introduction-to-neural-networks-part-1-e13f132c6d7e)
Status: #ARTICLE
**Tags**: [[]]

> [!Abstract] 
> A detailed explanation of how neural networks are structured and why. Each component of a neural network is explained and why a neural network is able to learn from data.

**Authors**: [[Harsha Bommana]]
**Revision Date**: 2019-05-26 15:33:58
**Import Date**: 2023-09-18 04:03:44
___

# Highlights

> The brain is essentially a bunch of neurons connected to each other in a huge interconnected network. [⤴️](https://omnivore.app/me/introduction-to-neural-networks-part-1-by-harsha-bommana-deep-le-18aa36f3c55#bb557685-d09d-4420-978d-ee5b0e1ec351)  ^bb557685

> Neural pathways become **stronger** upon frequent usage, and our brain essentially tries to use pathways which have proven to give us better results over time. [⤴️](https://omnivore.app/me/introduction-to-neural-networks-part-1-by-harsha-bommana-deep-le-18aa36f3c55#a05079ca-68bb-48d7-837b-b060ed4b0bc7)  ^a05079ca

> Y is the **final value** of the node. [⤴️](https://omnivore.app/me/introduction-to-neural-networks-part-1-by-harsha-bommana-deep-le-18aa36f3c55#d19f2849-2865-487c-bd00-ee25bb1fe8ad)  ^d19f2849

> will result in a **linear** [⤴️](https://omnivore.app/me/introduction-to-neural-networks-part-1-by-harsha-bommana-deep-le-18aa36f3c55#6d9e29fe-2468-4e6e-a127-a311175044aa)  ^6d9e29fe

> between the input [⤴️](https://omnivore.app/me/introduction-to-neural-networks-part-1-by-harsha-bommana-deep-le-18aa36f3c55#05a3edc4-2a14-4566-a90f-1da6a6c73e1b)  ^05a3edc4

> ReLU: [⤴️](https://omnivore.app/me/introduction-to-neural-networks-part-1-by-harsha-bommana-deep-le-18aa36f3c55#b7497bab-2893-4533-97c4-1328b3a2a0ef)  ^b7497bab

> Linear Unit. [⤴️](https://omnivore.app/me/introduction-to-neural-networks-part-1-by-harsha-bommana-deep-le-18aa36f3c55#ab317b33-0a65-45a6-977b-8f551cd89d7b)  ^ab317b33

> function because [⤴️](https://omnivore.app/me/introduction-to-neural-networks-part-1-by-harsha-bommana-deep-le-18aa36f3c55#0e5a1c96-24a7-45d3-a0dc-32d0b7ccfa5f)  ^0e5a1c96

> **Sigmoid:** Sigmoid is essentially a function bounded between 0 and 1. [⤴️](https://omnivore.app/me/introduction-to-neural-networks-part-1-by-harsha-bommana-deep-le-18aa36f3c55#0507c58a-c175-417e-9100-f478ca158440)  ^0507c58a

> Hence this function _squishes_ values which are very high or very low to values between 0 and 1. [⤴️](https://omnivore.app/me/introduction-to-neural-networks-part-1-by-harsha-bommana-deep-le-18aa36f3c55#c9668ec8-22b2-4520-b8c9-97820b6cba2d)  ^c9668ec8

> This is useful in neural networks sometimes to ensure values aren’t extremely high or low. [⤴️](https://omnivore.app/me/introduction-to-neural-networks-part-1-by-harsha-bommana-deep-le-18aa36f3c55#37d4d801-0f4e-4192-b85d-2a3c03bbb80b)  ^37d4d801

> This concludes this part of the tutorial. [⤴️](https://omnivore.app/me/introduction-to-neural-networks-part-1-by-harsha-bommana-deep-le-18aa36f3c55#ef330f8d-b584-4d8f-a29e-2f9eb0969b27)  ^ef330f8d

> Thank you for reading! [⤴️](https://omnivore.app/me/introduction-to-neural-networks-part-1-by-harsha-bommana-deep-le-18aa36f3c55#c3be0d8c-83e1-4dda-8f48-9db600b050df)  ^c3be0d8c

> Read more [⤴️](https://omnivore.app/me/introduction-to-neural-networks-part-1-by-harsha-bommana-deep-le-18aa36f3c55#2a1a41a9-528f-4953-9b19-e990a9cc6f70)  ^2a1a41a9

