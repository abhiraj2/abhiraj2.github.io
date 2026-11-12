---
layout: page
title: "GPU Options Pricer"
importance: 4
status: ""
stack: [C++20, Apple Metal, GPU Kernels, Monte Carlo]
github: https://github.com/abhiraj2/options-pricing-engine
---

A Monte Carlo engine built on Apple Metal compute kernels. It prices 10,000 options about 300× faster than the serial CPU baseline and is validated against the closed-form solution to under 0.05% error.
