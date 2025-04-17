---
title: LoRA相关
date: 2025-03-31 13:55:23
category: LLM基础
---

## 找到 LoRA 的核心文件

最新版本 LoraModel 继承自 BaseTuner，核心是`_create_and_replace`函数中的`target.update_layer`函数

最后找到\peft\tuners\lora\layer.py，进行修改即可
