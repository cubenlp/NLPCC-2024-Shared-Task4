# Shared-Task-4 Chinese Essay Discourse Logic Evaluation and Integration


# 最新消息

| 时间 | 消息 |
| --- | --- |
| 4月15日 | 训练数据和guidelines已公布 |
| 3月25日 | 评测任务开放报名 |
| 4月15日 | 训练数据和guidelines公布 |
| 5月25日 | 报名截止 |
| 6月11日 | 测试数据通过邮件发布，公布[测试结果排行榜](https://github.com/cubenlp/NLPCC-2024-Shared-Task4/blob/main/Result.md) |
| 6月20日 | 比赛结果提交截止 |
| 6月30日 | 比赛结果成绩公布[最终结果排行榜](https://github.com/cubenlp/NLPCC-2024-Shared-Task4/blob/main/Result.md) |
# 评价标准

## Track 1. **Discourse Logic Error Detection (DLED)**.
&emsp;总分由语篇逻辑错误识别分数（包括精确率（Precision, P）、召回率（Recall, R）、（F1值（F1）））来评估语篇逻辑错误类型的识别效果，具体计算方式如下：
    $$Score_{track1} = F_{1}^{Fine-grained}$$


## Track 2. **Topic Coherence Modeling (TCM)**.

&emsp;采用段落间关系细粒度识别分数（包括粗粒度（Coarse-grained F1）、细粒度分类（Fine-grained F1）和准确率（Accuracy, Acc））、段落主题句识别准确率（Accuracy, Acc）来评估中小学作文主题连贯性建模的效果，具体计算方式如下：
    $$Score_{track2} = (0.3 \times Micro-F_{1}^{Coarse-grained} + 0.7 \times Micro-F_{1}^{Fine-grained} + 0.3 \times Macro-F_{1}^{Coarse-grained} + 0.7 \times Macro-F_{1}^{Fine-grained} + (Relation{\textunderscore}Acc + ParaTopic{\textunderscore}Acc)) / 4$$
    
## Track 3. **Discourse Coherence Feedback Generation (DCFG)**.
&emsp;由PPL(取对数处理)、BLEU、ROUGE-L、BERTScore和人工打分来评估中小学作文语篇连贯性评语生成的效果，具体计算方式如下：
    $$Score_{track3} = 0.15 \times PPL + 0.25 \times BLEU + 0.25 \times ROUGE-L + 0.3 \times BERTScore + 0.05 \times Human{\textunderscore}Expert{\textunderscore}Feedback$$
# Introduction
 
In the realm of middle and high school examination scoring, essay evaluation is notably challenging, time-consuming, and contentious. With skepticism surrounding the traditional methods' accuracy and efficiency, there's a growing interest in machine scoring as an alternative. While significant advancements in automatic essay assessment technology have been made, they predominantly focus on linguistic elements, often neglecting the crucial role of discourse logic in determining essay quality. Recognizing this gap, East China Normal University's CubeNLP laboratory and Microsoft Research Asia developed the CEDCC dataset to enrich automatic essay evaluation by emphasizing logical structure. The "Discourse Logic Evaluation and Integration Task" competition aims to enhance essay scoring's accuracy and efficiency by exploring essays' discourse logic, encouraging innovative approaches using the CEDCC dataset to advance automatic essay assessment technology.

This shared task includes three tracks:

Track 1. **Discourse Logic Error Detection (DLED)**. Given a middle school student's essay, annotators are required to identify whether each sentence contains logical errors, including improper use of connective words, lack of logical relation between contexts, unreasonable sentence breaks, deviation from the theme, etc. This task aims to uncover the impact of these fine-grained factors on the coherence of the essay.

Track 2. **Topic Coherence Modeling (TCM)**. The task involves identifying the topic sentence of each paragraph and evaluating the logical coherence between these topic sentences in a middle school student's essay. Annotators are required to identify the topic sentence of each paragraph and determine which sentence best represents the central idea of the entire text (the main topic sentence). Subsequently, they assess the logical relationship between adjacent topic sentences, analyzing how they interconnect to support the overall structure of the article.

Track 3: **Discourse Coherence Feedback Generation (DCFG)**. Annotators assess a middle school essay's discourse coherence, focusing on four key areas: understanding the essay's structure and flow (Discourse Analysis), identifying main arguments and details (Topic Extraction), evaluating argument logic and relevance (Logic Detection), and providing an overall coherence rating (Coherence Rating). The feedback should be specific, constructive, and aimed at guiding students to improve their writing skills.


数据声明：为了确保学生信息的妥善处理和保护，此次数据不可用于竞赛之外的商业用途；若有其他学术需求请进一步联系组织者。

