---
title: git技巧
date: 2023-04-28 10:53:24
category: git
---

# 开始
本地分支是和远程分支独立的，只通过关联进行pull，push操作
对！你发现了一个非常关键的点！👏

> 💥 **如果你只是执行 `git checkout -b xxx`，默认是基于你当前所在的分支来创建的！**

---

### 🧠 举个例子来说明：

#### 场景：

你刚 clone 完一个项目，默认在 `main` 分支上。

然后你执行：

```bash
git checkout -b my-feature
```

那么结果是：

- `my-feature` 是基于 `main` 的
- 它的内容和提交历史都是从 `main` 复制过来的

---

### ✅ 想基于 `dev` 创建分支，要这样做：

你需要**明确指定分支来源**：

```bash
git checkout -b my-feature origin/dev
```

这个意思是：
- 用远程的 `origin/dev` 创建一个新的本地分支 `my-feature`
- 并且自动跟踪远程的 `origin/dev`（也可以不自动）

---

### 🔍 或者你可以分两步做得更清晰：

```bash
# 1. 创建并切换本地 dev 分支
git checkout -b dev origin/dev

# 2. 再基于 dev 创建自己的功能分支
git checkout -b my-feature
```

这样 `my-feature` 就是从 `dev` 分支上分出来的，内容就一致了 ✅

---

### 🧪 快速对比：

| 命令                              | 基于哪个分支？       |
|-----------------------------------|-----------------------|
| `git checkout -b xxx`             | 当前所在分支 ❗（比如 main） |
| `git checkout -b xxx origin/dev`  | 基于远程的 dev 分支  |
| `git checkout -b xxx dev`         | 基于本地的 dev 分支  |

---

