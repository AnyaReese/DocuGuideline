# iGEM 项目文档写作指南

!!! abstract "本指南旨在规范团队文档写作，确保文档的一致性和可读性"

## 专业内容规范

### 专业术语

首次出现的专业术语需要同时给出中英文对照。

=== "术语首次出现"
    !!! failure "错误用法"
        ```markdown
        我们构建了规律成簇间隔短回文重复序列编辑目标基因。
        ```

    !!! success "正确用法"
        ```markdown
        我们构建了 CRISPR（Clustered Regularly Interspaced Short Palindromic Repeats，规律成簇间隔短回文重复序列）系统来编辑目标基因。后续实验中继续使用 CRISPR 系统...
        ```

### 内容格式统一规范

!!! abstract "当多人协作编写文档时，需要保持格式的一致性，避免同一概念出现不同的表达方式。"

=== "标题层级使用"
    !!! failure "错误示例"
        ```markdown
        # 实验方法
        **Cycle 1**
        具体步骤...
        
        ## cycle_2
        具体步骤...
        
        ## 1cycle
        具体步骤...
        ```

    !!! success "正确示例"
        ```markdown
        # 实验方法
        ## 循环步骤
        ### Cycle 1
        具体步骤...
        
        ### Cycle 2
        具体步骤...
        
        ### Cycle 3
        具体步骤...
        ```
        或其他统一方法

        !!! note "规则说明"
            - 同级内容保持一致的标题等级
            - 同类概念使用统一的命名方式
            - 避免跳级使用标题

=== "强调格式统一"
    !!! failure "错误用法"
        ```markdown
        **重要步骤**
        1. 加入 Buffer
        2. **调节 pH 至 7.4**
        3. __温度控制__ 在 37℃

        ## 注意事项
        **1. 避免污染**
        2. *轻柔混匀*
        ```

    !!! success "正确用法"
        ```markdown
        ## 重要步骤
        1. 加入 Buffer
        2. 调节 pH 至 7.4（关键步骤）
        3. 温度控制在 37 °C

        ## 注意事项
        1. 避免污染
        2. 轻柔混匀
        ```

        !!! note "说明"
            - 请各外关注 x 级标题与加粗字体的区别，在飞书文档中可能并不明显。
            - 正文中需要强调的内容统一使用加粗或括号注释
            - 列表项保持统一格式

=== "专业术语统一"
    !!! failure "混乱示例"
        ```markdown
        第一次实验用 E.coli，
        第二次实验用 E. coli，
        第三次实验用大肠杆菌 (E-coli)
        ```

    !!! success "统一示例"
        ```markdown
        首次出现：大肠杆菌（Escherichia coli，E. coli）
        后续使用：E. coli
        ```

???+ tip "格式统一检查清单"
    - [ ] 标题层级是否一致
    - [ ] 专业术语写法是否统一
    - [ ] 强调格式是否统一
    - [ ] 列表格式是否统一
    - [ ] 单位表示是否统一
    - [ ] 数字格式是否统一（如 1000 vs 1,000）

=== "常见统一性问题"
    | 内容类型 | 不推荐写法 | 推荐写法 |
    |:---------|:-----------|:---------|
    | 实验步骤 | Step1、step-1、**步骤1** | Step 1 |
    | 温度单位 | 37℃、37°C、37度 | 37 °C |
    | 时间单位 | 30min、30 mins、30分钟 | 30 min |
    | 浓度单位 | 5mM、5 millimolar、5毫摩尔 | 5 mM |
    | 体积单位 | 20ul、20μL、20微升 | 20 μL |
    | 序号格式 | ①、(1)、**1.** | 1. |

!!! warning "特别注意"
    - 加粗（**）不是用来表示标题的，标题统一使用 # 
    - 同一文档中的相同概念应该使用相同的表达方式
    - 单位符号前要加空格
    - 专业术语首次出现需要中英文对照，后续保持统一格式

另外，在长文本出现很多加粗内容的时候，最好在飞书上提供一份 markdown 源码，这样后续就不用手动添加 `<strong>` 标签了

### 超链接规范

=== "处理超链接"
    !!! failure "不要这样做"
        使用需要悬浮才能看到的链接：
        ![hypo](./img/hypo.png)

    !!! success "推荐做法"
        直接列出链接文本和地址：
        ```markdown
        [PCR 实验方法](https://example.com/pcr-protocol)
        [基因克隆指南](https://example.com/cloning-guide)
        [实验数据分析](https://example.com/data-analysis)
        ```
        ![hypo](./img/hypo-right.png)

## 图表规范

### 图片规范

- 图片需要清晰可见
- 图片需要去除水印，避免有截断的内容（影响美观和完成度）
- 图片尽量统一说明文字（比如单篇文档中都有或者都没有）

### 表格规范

对于复杂表格，建议：

    1. 使用在线 Markdown 表格生成器
    2. 考虑使用 HTML 表格
    3. 必要时可以将表格制作为图片插入

### 数学公式

使用 KaTeX 语法书写数学公式。

=== "行内公式"
    !!! failure "错误用法"
        Word 内嵌。wiki 将受极大折磨。

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


## 参考文献规范

!!! warning "可能的后续修改"
    - 预计加入 reference 自动编号，这样就不需要大家手动调了。但在实际实现之前，还是需要大家手动维护。

### 参考文献格式

=== "基本格式"
    ```markdown
    # 中英文文档使用相同的参考文献编号
    [1] Author, A. A., & Author, B. B. (Year). Title of article. Journal Name, Volume(Issue), page-range.
    ```

=== "引用示例"
    !!! failure "错误做法"
        ```markdown
        # zh.md
        这项技术在基因编辑领域有重要应用[1]。

        # en.md
        This technology has important applications in gene editing[2].  // 编号不一致！
        ```

    !!! success "正确做法"
        ```markdown
        # zh.md
        这项技术在基因编辑领域有重要应用[1]。

        # en.md
        This technology has important applications in gene editing[1].  // 保持编号一致
        ```

### 参考文献列表维护

=== "列表格式"
    ```markdown
    ## References
    [1] An, L., Jan, C. L., Feng, J., Wang, Z., Zhan, L., & Xu, X. (2019). Inequity in Access: Cataract Surgery Throughput of Chinese Ophthalmologists from the China National Eye Care Capacity and Resource Survey. Ophthalmic Epidemiology, 27(1), 29–38. https://doi.org/10.1080/09286586.2019.1678654
    ```

### 特别注意事项

!!! warning "常见问题"
    - 不要在中英文文档中使用不同的参考文献
    - 不要改变参考文献的编号顺序
    - 不要在翻译时省略或添加引用
    - 确保所有引用的文献都在参考文献列表中
    - 注意检查 DOI 链接的正确性

=== "引用检查清单"
    - [ ] 中英文文档引用编号一致
    - [ ] 参考文献格式统一
    - [ ] 所有引用都有对应的参考文献
    - [ ] DOI 链接可访问
    - [ ] 参考文献信息完整准确
    - [ ] 引用位置在中英文中对应

## 协作实践

### 文档审查

在确认完成文档更改前检查：

- [ ] 语法拼写是否正确
- [ ] 图片是否清晰可见
- [ ] 英文标点是否规范
- [ ] 专业术语是否统一
- [ ] 图表是否清晰完整
- [ ] 参考文献是否规范

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

