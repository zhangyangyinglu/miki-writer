# 第三方来源说明

`miki-writer` 最初参考并蒸馏改造自以下项目。本仓库里的具体文本规则大多已经过重写，
但方法论和结构上仍有继承关系，如实列出来源，不代表全部内容均为独立原创。

## Humanizer-zh（MIT License）

来源：https://github.com/op7418/Humanizer-zh

`references/de-ai-calibration.md` 中"注入观点和个性"一节的方法论参考了这个项目。
原始许可证如下（2026-09-08 从上游仓库取得）：

```
MIT License

Copyright (c) 2026 歸藏

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 枪手 qiangshou-skill（PolyForm Noncommercial License 1.0.0，2026-09-08 确认）

来源：https://github.com/shengjidaguai-china/qiangshou-skill

`miki-writer` 最初是从这个项目蒸馏改造而来。核对过双方的公开 README 后，以下内容
基本是照搬过来的，不是独立想到的相同做法：

- 五类事实核验（仓库可验证/用户亲述/第三方反馈/作者推断/时效数据）——名称和顺序一致。
- 六步技术写法"问题→为什么难→尝试与取舍→具体实现→可量化结果→适用边界"——逐字一致。
- 五种主导推进线（事件变化/认知变化/决策变化/实验变化/人物关系变化）——一致。
- 终稿保护规则（删除不可恢复、否决的建议不重提、只能改明确授权的错别字）——高度一致。
- 轻量自进化的具体参数（对比手改终稿、纯排版不算、两篇重复才转正、明确指令立即生效、
  每篇最多 2 条、"这次不要学习"跳过）——具体数字和触发词一致。

原始许可证是 **PolyForm Noncommercial License 1.0.0**（本仓库根目录 `LICENSE`
文件的原文就是这份协议）：允许基于它做修改和衍生作品，但**限定非商业用途**，
并要求把这份条款（或链接）一并给到拿到软件的人；查过原仓库没有额外的
`Required Notice:` 具体文本要求。

**因此本仓库也采用同一份 PolyForm Noncommercial License 1.0.0**，这是目前能确定
合规的最直接选择。这意味着：这份 Skill 本身（不是用它写出来的内容）只能用于非商业
用途；如果 Miki 未来想把 miki-writer 这个 Skill 本身用于商业场景（比如作为付费产品
的一部分），需要单独联系枪手的作者取得授权，不能直接假设现在的许可证覆盖那种用法。

## de-AI-writing（许可证状态：保持疑问）

来源：https://github.com/OUBIGFA/De-AI-Prompt-Enhancer-Writer-Booster-SKILL（确认存在，
public 仓库）。

这个仓库**没有任何 LICENSE 文件**（GitHub API 确认 `license: None`），按 GitHub
默认规则等于"保留所有权利"。它自己是基于 Humanizer-zh（MIT）升级的，但 OUBIGFA
自己新增的内容没有单独给许可证。`references/de-ai-calibration.md` 的两阶段检测方法
和它的方法论有相似之处（分层检测、去模板化），但没有找到六步写法那种逐字一致的
证据，重合程度不如 qiangshou 确定。

**状态：Miki 明确要求保持疑问，不下结论**——不认定"确实蒸馏了"，也不认定"完全无关"，
这条留待她自己判断或联系原作者核实。
