# Unrestricted Adversarial Examples Challenge

In the Unrestricted Adversarial Examples Challenge, attackers submit arbitrary adversarial inputs, and defenders are expected to assign low confidence to difficult inputs while retaining high confidence and accuracy on a clean, unambiguous test set.

This repository contains code for [the warm-up to the challenge](warmup.md), as well as [the public proposal for the contest](contest_proposal.md).

![image](https://user-images.githubusercontent.com/306655/44686400-f0b74800-aa02-11e8-8967-fa354244813f.png)


### <a name="leaderboard"></a>Leaderboard for the warm-up to the contest
We include three attacks in [the warm-up to the contest](warmup.md):

- 1000 Linfinity-ball adversarial examples generated by SPSA
- 1000 spatial adversarial examples (via grid search)
- 100 L2-ball adversarial examples generated by a decision-only attack

The top few distinct models for each dataset are shown below.  You can see all submissions in [the full scoreboard](scoreboard.md). 

#### Two-Class MNIST dataset
![tcu_mnist_example 2x](https://user-images.githubusercontent.com/306655/45503196-f6b76380-b73a-11e8-8f9f-81213bfe41db.png)

| Defense               | Submitted by  | Clean data | Spatial grid attack | SPSA attack | L2-ball attack |  Submission Date |
| --------------------- | ------------- | ------------ |------------ |--------------- |--------------- | --------------- |
| [MadryPGD LeNet Baseline](#)  |  Google Brain |    100.0%    |      ??    |     ??   |     ??     |  Aug 28th, 2018 |
| [Undefended LeNet Baseline](#)   |  Google Brain   |    100.0%    |     ??    |     ??    |     ??     |  Aug 27th, 2018 |
All percentages above correspond to the model's accuracy at 80% coverage.

#### Bird or Bicycle dataset
![bob_example 2x](https://user-images.githubusercontent.com/306655/45503195-f6b76380-b73a-11e8-986d-12310d2fb6f6.png)

| Defense               | Submitted by  | Clean data | Spatial grid attack | SPSA attack | L2-ball attack |  Submission Date |
| --------------------- | ------------- | ------------| ------------ |--------------- |--------------- | --------------- |
| [Pytorch ResNet <br>(via bird-or-bicycle extras)](unrestricted_advex/undefended_pytorch_resnet)  |  Google Brain |    99.0%    |     45.2%   | 12.8%   |     ??     |  Sept 13th, 2018 |
| [Keras ResNet <br>(via ImageNet)](unrestricted_advex/undefended_keras_resnet)   |  Google Brain   |    99.5%    |     ??    |     ??    |     ??     |  In progress |
All percentages above correspond to the model's accuracy at 80% coverage.


### Submitting a defense for the warm-up

The [warm-up before the contest](warmup.md) is currently underway and is accepting submissions. If you have additional questions, feel free to [submit a new GitHub issue](https://github.com/google/unrestricted-adversarial-examples/issues/new) with the "question" tag and we will respond shortly.

## The contest

The contest phase will begin after the warm-up attacks have been conclusively solved. We have published the [contest proposal](https://github.com/google/unrestricted-adversarial-examples/blob/master/contest_proposal.md) and are soliciting feedback from the community.


## Paper
You can learn more about the motivation and structure of the contest in our recent paper:

**Unrestricted Adversarial Examples**<br>
*Tom B. Brown, Nicholas Carlini, Chiyuan Zhang, Catherine Olsson, Paul Christiano and Ian Goodfellow*<br>
[Arxiv paper preprint](https://drive.google.com/open?id=1T0yiu9LPv_Qh-qYhYFLj9dxjnkca8fkG)
