# AI 嘉豪测试 · 开源题库

「AI 嘉豪测试」的公开题库——一套专治「不懂 AI 却装懂、乱秀黑话、自以为是」的中文 AI 素养题。

- 在线测试：**https://jiahao.nagi.fun**
- by [NAGI STUDIO](https://github.com/nagi-studio) · 配套严肃榜单 [bench.nagi.fun](https://bench.nagi.fun)

本仓库只放**题库内容（开源）**；网站本体闭源（和 [nagi-bench](https://github.com/nagi-studio/nagi-bench) / nagi-bench-site 一样的拆分）。

## 文件

- **`questions.json`** —— 全部题目：题干、选项、正确答案、「拆穿」解析、分区、分值。28 题，6 个分区（基础 / 消消乐连线 / 附加 / 避坑·经济 / 人文 / 压轴）。
- **`personas.json`** —— 7 档结果人设（嘉豪本豪 → 扫地僧）+ 每档的随机吐槽池 + 标签。

## 题目格式

```jsonc
// choice 题
{
  "kind": "choice",
  "code": "Q1",
  "section": "basic",
  "points": 10,
  "tag": "next token",
  "stem": "……",
  "options": [{ "id": "a", "text": "……" }, ...],
  "answer": "b",            // 正确选项的 id
  "trap": "……"             // 选错时弹出的「拆穿」解析
}
// match 题（消消乐连线）：items / targets / solution(itemId → targetId)
```

> 选项在前端**随机打乱**，位置不携带信息（答案以 `id` 记）。

## 设计原则（欢迎按此 PR 纠错 / 补题）

1. **不考定义，考机制**——考真实理解，不考背术语。
2. **干扰项要等长、等「行话浓度」**——不能「无脑选最长的就对」。
3. **事实须可核**——涉及具体数字 / 命名要能给出来源。

## License

题库内容采用 MIT，见 [LICENSE](./LICENSE)。
