---
layout: post
title: "3 questions about DL"
date: 2016-08-17
excerpt: ""
tags: [Computer Science]
comments: true
---


### Three questions while learning Deep Learning 

#### 学习深度学习过程中的几个问题

----------

1. 
	#### In my opinion, there are three points in selection of activation function as below.
	* continuous: for derivation
	* function value beween 0 and 1: for normalization
	* non-linear: to express higher complexity with deeper network

	#### Is it right?
	
		激活函数的选取有三个要点，对吗？
		1. 连续
		2. 0～1
		3. 非线性


2. 
	#### The book referred 2 methods to prevent learning slow-down:
	* keep σ as the activation funtion, while using cross-entropy as cost funtion instead of quadratic cost function
	* a soft-max output layer with log-likelihood cost

	#### I think this can only prevent learning slow-down of the last layer, i.e the output layer.<br>As for the other layers, viz. the hidden layers, whose activation function is still σ, σ′ remains to be in the partial derivative ∂C/∂w. Which means the problem slow-down still exists.<br>Change an appropriate activation function may be a solution.
		
		书上用两种方法来解决学习变慢问题
			1. 输出层依然用激活函数σ，成本函数改用交叉熵
			2. 应用softmax输出层，结合成本函数 log-likelihood cost function
		 我的理解是，这样只能部分解决学习变慢问题，
		 隐含层的参数学习变慢我认为可以通过修改激活函数来解决。


3. 
	#### Why config η, not delta(loss) or |delta(weight)| ? <br>For convenience? <br>Can we prevent slow-down of learning with the later configuration?
		
		是否可以通过限定weight offset vector length, 或损失函数的修改量来解决学习变慢问题？ 

----------

