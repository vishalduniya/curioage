+++
title = 'My First Post'
date = 2024-01-14T07:07:07+01:00
draft = false
tags = ['test', 'first']
math = true
toc= true
+++
## Introduction

This is **bold** text, and this is *emphasized* text.

> [!tip] Callouts can have custom titles
> Like this one.

Visit the [Hugo](https://gohugo.io) website!



## Testing  Equations

Block math:

$$
 \varphi = 1+\frac{1} {1+\frac{1} {1+\frac{1} {1+\cdots}}} 
$$


## Inline Code

This website is created in `Hugo`.


## Code Block

```py
import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
from matplotlib import rcParams

# Set font style
rcParams['font.sans-serif'] = 'Arial'

df = pd.read_excel("Peak_Voltage_TI-IB.xlsx", names=["type", "voltage", "error"])

x = df["type"].values
y = df["voltage"].values
yerr = df["error"].values

colors=["#254D70", "#C78A3B"]

plt.figure(figsize=(4, 2.6))

plt.bar(x, y, width=0.6, color= colors, edgecolor='k', alpha=0.6)
plt.errorbar(x, y, yerr=yerr, fmt='none', ecolor='black', capsize=10)
plt.xlabel("tVolt", fontsize=14)
plt.ylabel("Voltage (V)", fontsize=14)
plt.xticks(fontsize=12)
plt.yticks(fontsize=12)
plt.tight_layout()
# plt.savefig("Voltage_tVolt_TIvsIB-2x3.jpg", dpi = 1200, bbox_inches = 'tight')
plt.show()
```



