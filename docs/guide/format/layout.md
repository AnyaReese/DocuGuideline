# iGEM 项目文档写作指南

!!! abstract "本指南旨在规范团队文档写作，确保文档的一致性和可读性"

## 中文转英文写作基本规范

### 中英文混排

中英文混排时需要注意空格的使用。

=== "中英文之间的空格"
    !!! failure "错误用法"
        ```markdown
        我们使用PCR方法扩增DNA片段。
        ```

    !!! success "正确用法"
        ```markdown
        我们使用 PCR 方法扩增 DNA 片段。
        ```

=== "数字与单位"
    !!! failure "错误用法"
        ```markdown
        温度为37°C时进行反应
        ```

    !!! success "正确用法"
        ```markdown
        温度为 37 °C 时进行反应
        ```

### 标点符号

标点符号的使用需要遵循中文排版规范。

=== "中文句子中的标点"
    !!! failure "错误用法"
        ```markdown
        实验结果表明,该基因的表达量显著上升.
        ```

    !!! success "正确用法"
        ```markdown
        实验结果表明，该基因的表达量显著上升。
        ```

=== "括号的使用"
    !!! failure "错误用法"
        ```markdown
        荧光素酶(luciferase)可以用作报告基因
        ```

    !!! success "正确用法"
        ```markdown
        荧光素酶（luciferase）可以用作报告基因
        ```

## 专业内容规范

### 专业术语

首次出现的专业术语需要同时给出中英文对照。

=== "术语首次出现"
    !!! failure "错误用法"
        ```markdown
        我们构建了 CRISPR 系统来编辑目标基因。
        ```

    !!! success "正确用法"
        ```markdown
        我们构建了 CRISPR（Clustered Regularly Interspaced Short Palindromic Repeats，规律成簇间隔短回文重复序列）系统来编辑目标基因。后续实验中继续使用 CRISPR 系统...
        ```

### 实验数据呈现

实验数据的呈现需要规范化。

=== "数据描述"
    !!! failure "错误用法"
        ```markdown
        OD600=0.6加IPTG,37度培养2h
        ```

    !!! success "正确用法"
        ```markdown
        当 OD600 值达到 0.6 时加入 IPTG（终浓度 1 mM），在 37 °C 条件下培养 2 h。
        ```

## 图表规范

### 图片插入

图片插入时需要考虑排版效果。

=== "基本图片插入"
    !!! failure "错误用法"
        ```markdown
        ![](images/result.png)
        ```

    !!! success "正确用法"
        ```markdown
        <div style="text-align: center;">
        <img src="images/result.png" width="70%" style="margin: 0 auto;">
        <p>图 1: 实验结果分析图</p>
        </div>
        ```

???+ note "关于图片路径"
    图片路径应该基于 docs/ 目录的相对路径。例如，如果你的文档在 `docs/project/methods.md`，图片在 `docs/images/result.png`，则路径应写作 `../images/result.png`。

### 表格规范

表格需要清晰地展示数据结构。

=== "基本表格"
    !!! failure "错误用法"
        ```markdown
        |样品|OD600|处理|
        |-|-|-|
        |1|0.5|control|
        ```

    !!! success "正确用法"
        ```markdown
        | 样品编号 | OD600 值 | 处理条件 |
        |:--------:|:--------:|:---------|
        | 1        | 0.5      | 对照组   |
        | 2        | 0.6      | 实验组   |
        ```
        
        !!! note "说明"
            - 使用冒号控制对齐方式
            - 保持表头的中文说明
            - 数据列建议居中对齐

### 数学公式

使用 KaTeX 语法书写数学公式。

=== "行内公式"
    !!! failure "错误用法"
        ```markdown
        PCR扩增效率为2^n
        ```

    !!! success "正确用法"
        ```markdown
        PCR 扩增效率为 \(2^n\)
        ```

=== "独立公式"
    !!! failure "错误用法"
        ```markdown
        根据 Beer-Lambert 定律:
        A = εbc
        ```

    !!! success "正确用法"
        ```markdown
        根据 Beer-Lambert 定律：

        \[A = \varepsilon bc\]

        其中 \(A\) 为吸光度，\(\varepsilon\) 为摩尔消光系数，\(b\) 为光程，\(c\) 为浓度。
        ```

## 文件组织规范

### 文件命名

!!! note "文件命名规则"
    - 使用小写字母
    - 用连字符(-)分隔单词
    - 使用有意义的描述性名称
    
=== "文件命名示例"
    !!! failure "错误命名"
        ```
        Experiment1.md
        PCR Protocol.md
        实验方法.md
        ```

    !!! success "正确命名"
        ```
        pcr-protocol.md
        enzyme-digestion.md
        transformation-method.md
        ```

## 协作最佳实践

### 版本控制

=== "提交信息规范"
    !!! success "良好的提交信息"
        ```
        feat: 添加 PCR 实验方法文档
        
        - 添加标准 PCR 反应体系配置
        - 添加温度循环程序参数
        - 补充注意事项和故障排除
        ```

### 文档审查

在提交重要更改前检查：

- [ ] 中英文间距是否规范
- [ ] 专业术语是否统一
- [ ] 图表是否清晰完整
- [ ] 参考文献是否规范

### 常见问题解决

???+ question "为什么我的图片显示不出来？"
    1. 检查图片路径是否正确
    2. 确认图片文件名大小写是否匹配
    3. 验证图片格式是否支持（推荐使用 PNG、JPG）

???+ question "如何处理复杂的表格？"
    对于复杂表格，建议：

    1. 使用在线 Markdown 表格生成器
    2. 考虑使用 HTML 表格
    3. 必要时可以将表格制作为图片插入

???+ question "数学公式显示异常？"
    1. 确认已在 mkdocs.yml 中配置了 KaTeX
    2. 检查公式语法是否正确
    3. 注意转义字符的使用

## 附录

### 常用 Markdown 语法速查

```markdown
# 一级标题
## 二级标题

**加粗** *斜体*

- 无序列表
1. 有序列表

> 引用文本

[链接文本](URL)

![图片描述](图片路径)

`行内代码`

```代码块```
```

### 实用工具推荐

- 语法检查
    - Grammarly (语法检查)
    - Hemingway Editor (写作风格)

- 图片处理
    - ImageOptim (图片压缩)
    - Snipaste (截图工具)

- 表格工具
    - Tables Generator
    - Markdown Table Maker

