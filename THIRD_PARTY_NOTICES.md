# 第三方来源说明

`miki-writer` 的方法论蒸馏改造自以下两个项目，具体文本规则已经重写，但结构和方法论上有直接继承关系。

## Humanizer-zh（MIT License）

来源：https://github.com/op7418/Humanizer-zh

`references/de-ai-calibration.md` 的"注入观点和个性"一节直接依赖这个项目。Humanizer-zh 自身在其仓库里声明翻译自上游的 `humanizer` 项目，并参考了 `stop-slop` 项目——具体仓库地址以 Humanizer-zh 当时仓库说明为准（未在此处逐一核实链接，避免记录错误地址）；本文件只记录到 Humanizer-zh 这一层直接来源，更上游的两层未单独重写引用。上游许可证原文：

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

## 枪手 qiangshou-skill（PolyForm Noncommercial License 1.0.0）

来源：https://github.com/shengjidaguai-china/qiangshou-skill

以下方法论直接继承自这个项目：五类事实核验（仓库可验证/用户亲述/第三方反馈/作者推断/时效数据）、六步技术写法（问题→为什么难→尝试与取舍→具体实现→可量化结果→适用边界）、五种主导推进线（事件/认知/决策/实验/人物关系变化）、终稿保护规则、轻量自进化的具体参数。

原始许可证是 [PolyForm Noncommercial License 1.0.0](https://polyformproject.org/licenses/noncommercial/1.0.0)：允许修改和衍生，但**仅限非商业用途**，需要把这份条款一并给到使用者。本仓库采用同一份协议（见根目录 [LICENSE](LICENSE)）。这意味着 miki-writer 这个 Skill 本身只能用于非商业用途；商业使用需要取得覆盖上游材料（qiangshou-skill 和 Humanizer-zh 各自的授权链）以及 miki-writer 新增内容的**全部**必要授权，不是只联系其中一方就够——这份说明不构成法律意见，真要商业化前建议做一次正式的法律核验。
