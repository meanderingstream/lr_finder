---
title: Learning Rate Finder
theme: moon
revealOptions:
    transition: 'fade'
---
## Intro

Scott Mueller

###### smueller.tampa.ai@gmail.com

---
## Tampa.ai

Looking for Presenters


---
## A disciplined approach to neural network hyper-parameters: Part 1 – learning rate, batch size, momentum, and weight decay

https://arxiv.org/abs/1803.09820


---
* Super Convergence
* R1: Unreasonable Effectiveness of Validation/Test Loss
* R2: Horizontal Part of Test Loss
* Underfitting
* Overfitting
* Cyclical Learning Rates

---
* R3: Amount of Regularization Must Be Balanced
* R4: Highest Performance Minimizing Computational Time
* R5: Optimial Momentum Improves Network Training
* R6: Weight Decay is Key Knob for Tuning Regularization
* Short Recipe

---
## Super Convergence
<img src="./images/LRvsCLRresnet56.png"  height="500">

---
## Cyclical Learning Rate vs One Cycle
<img src="./images/CLR_1Cycle.png"  width="1000">

---
## Unreasonable Effectiveness OF Validation/Test Loss
<img src="./images/testLoss1.png"  height="450">

---
## R1: Test Loss Indicator of Network's Convergence
<img src="./images/under-overfitting.png" height="450">

---
## Underfitting
<img src="./images/3layerLoss.png"  height="500">

---
## R2: Horizontal Part of Test Loss
<img src="./images/imagenetTestLoss3.png"  height="500">

---
## Learning Rate Range Test
<img src="./images/lr_finder.png"  width="500">

---
## Overfitting
<img src="./images/imagenetResnetOverfitting.png"  height="500">

---
## Cyclical Learning Rate
<img src="./images/LRvsCLRresnet56.png"  height="500">

---
## One Cycle

<img src="./images/imagenetResnetSC2.png"  height="500">

---
## R3: Amount of Regularization Must Be Balanced

* Large Learning Rates

* Small Batch Sizes

* Weight Decay

* Dropout

---
## Batch Size Effect on Test Loss
<img src="./images/resnet56CifarTBSLoss.png"  height="500">

---
## R4: Highest Performance Minimizing Computational Time
<img src="./images/imagenetInceptionSC2.png"  height="500">

---
## R5: Optimial Momentum Improves Network Training

<img src="./images/3layerCMtestLoss.png"  height="450">

Momentum Rate Finder Not Useful

---
## Cyclical Momentum Opposite of Learning Rate Cycle

<img src="./images/CLR_CM.png"  width="450">

High Momentum when LR small, vice versa

---
## R6: Weight Decay is Key Knob for Tuning Regularization
<img src="./images/3layerWDTestLoss.png"  height="450">

Easier to determine best WD from test loss

---
## Everything Together
<img src="./images/3layerWDCLRCMTestLoss.png"  height="500">

---
## Short Recipe

* Learning Rate Range Test - Determine Max LR
 
  - Use 1 Cycle

* Batch size from your GPU size

* Cyclical Momentum in opposite direction from Cyclical LR

* Weight Decay - Grid Search to 1 significant figure

  - Complex datasets less regulation so smaller values 0.0001 - 0.000001

---
## Hyperparameter Clues are in Test Loss - Early in Training

<img src="./images/imagenetInceptionSC2.png"  height="500">

---
## One Cycle Focused on Adam Optimization

* Newer Optimizations may Require Different Approaches

  - Ranger (High LR for a while & Cosine Decay)

---

[Knowfalls.com](https://knowfalls.com/team.html)

###### scottmueller@knowfalls.com

Looking for Founder Engineers

Elixir, Functional Programming, Rails, Experience

---

https://iconof.com/1cycle-learning-rate-policy
