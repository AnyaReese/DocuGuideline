
## 中文转英文写作基本规范

### 标点符号

!!! abstract "由于大部分队员采用的方式是先写中文再做翻译，容易出现标点符号未统一的情况，需要特别注意。"

=== "英文标点的空格规范"
    !!! failure "错误用法"
        ```markdown
        The PCR reaction includes:DNA template,primers,and dNTPs.We added IPTG(1mM)to induce expression.
        ```

    !!! success "正确用法"
        ```markdown
        The PCR reaction includes: DNA template, primers, and dNTPs. We added IPTG (1 mM) to induce expression.
        ```

        !!! note "规则说明"
            - 逗号、句号后需要加空格
            - 冒号后需要加空格
            - 括号前后都需要加空格
            - 单位与数字之间需要加空格

=== "容易混淆的标点对照"
    !!! warning "中英文标点对照表"
        | 中文标点 | 英文标点 | 使用场景 |
        |:--------:|:--------:|:---------|
        | ，      | ,        | 并列、停顿 |
        | 。      | .        | 句末 |
        | ：      | :        | 解释说明 |
        | （）    | ( )      | 补充说明 |
        | "..."   | "..."    | 引用 |
        | 、      | ,        | 并列 |
        | ！      | !        | 感叹 |
        | ？      | ?        | 疑问 |

=== "中英文混排的标点选择"
    !!! failure "错误用法"
        ```markdown
        我们使用 PCR (Polymerase Chain Reaction),进行基因扩增.
        The experiment showed that,该基因在高温下表达上调。
        ```

    !!! success "正确用法"
        ```markdown
        我们使用 PCR（Polymerase Chain Reaction），进行基因扩增。
        The experiment showed that the gene was upregulated under high temperature.
        ```

        !!! note "原则"
            - 以句子的主要语言决定标点符号的选择
            - 避免在同一句子中混用中英文标点
            - 专业术语解释使用括号时，遵循主句的语言规范

???+ tip "标点符号的特殊情况"
    - 缩写中的点号（如 e.g., i.e., et al.）后仍需要加逗号时，只保留一个标点
    - 网址和文件路径中的标点不需要遵循一般规则
    - 数学公式、化学式中的标点遵循学科专业规范
    - 引用文献时的标点遵循所选用的引用格式规范（如 APA、MLA 等）


### 书名号与引号规范

!!! abstract "中英文在书名、文章标题等的标记方式上有很大差异，需要特别注意。"

=== "书名号的使用"
    !!! failure "错误用法"
        ```markdown
        We published our results in 《Nature》.
        The paper 《Gene Expression in E. coli》 shows that...
        ```

    !!! success "正确用法"
        ```markdown
        We published our results in *Nature*.
        The paper "Gene Expression in E. coli" shows that...
        ```

        !!! note "规则说明"
            - 英文中没有书名号《》
            - 期刊名使用斜体 *斜体*
            - 文章标题使用引号 "引号"

=== "不同级别标题的表示"
    | 内容类型 | 中文表示 | 英文表示 | 示例 |
    |:---------|:---------|:---------|:-----|
    | 期刊名   | 《》     | *斜体*   | 《自然》/ *Nature* |
    | 文章标题 | 《》     | "引号"   | 《基因表达研究》/ "Study on Gene Expression" |
    | 章节名   | 〈〉     | "引号"   | 〈实验方法〉/ "Methods" |
    | 书名     | 《》     | *斜体*   | 《分子生物学》/ *Molecular Biology* |

=== "混排情况处理"
    !!! failure "错误用法"
        ```markdown
        According to 《分子生物学》, the mechanism...
        在 *Nature* 上发表的《Gene Regulation》显示...
        ```

    !!! success "正确用法"
        ```markdown
        According to *Molecular Biology*, the mechanism...
        在 *Nature* 上发表的"Gene Regulation"显示...
        在《自然》上发表的《基因调控》显示...
        ```

???+ tip "注意事项"
    - 在纯英文句子中，使用英文的标记方式
    - 在纯中文句子中，使用中文的标记方式
    - 引用英文文献时，需要遵循英文的格式规范
    - Markdown 中使用 * 表示斜体，** 表示加粗
