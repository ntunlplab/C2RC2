# C2RC2 : The Dataset of the Classify Citation Relationships based on the Contributions of Cited papers



## 1 Introduction
C2RC2 dataset is collected by using arXiv and Semantic Scholar APIs, respectively. We divide
the dataset into the training, validation, and test sets. There are 2,594, 557, and 556 instances,
respectively. This dataset is provided in JSON format. We introduce various fields in the next
Section.
## 2 Field Description
The fields are divided into 3 types, general, cited paper, and citing paper.
### 2.1 General fields
* id: It is a unique identifier number of instance
* label: The index of the most related contribution to the citation sentence. If none are
related contributions, then label = 5.
### 2.2 Cited Paper’s Fields
* cited_arxiv_id: Cited paper’s arxiv_id

* cited_title: Cited paper’s title

* abstract: Cited paper’s abstract

* contributions_0: 1st contributions in contribution list.

* contributions_1: 2nd contributions in contribution list.

* contributions_2: 3rd contributions in contribution list.
* contributions_3: 4th contributions in contribution list.
* contributions_4: 5th contributions in contribution list.
### 2.3 Citing paper’s fields
* citing_paper_ssid: Citing paper’s Semantic Scholar ID
* citing_title: Citing paper title
* citing_context: Citation sentence. This field was collected from the Semantic Scholar
API, and we observed that sometimes it is not a complete sentence. Ideally, it is a citation
sentence.

## 3 Example of C2RC2 Dataset

```yaml
{
    "id":4693,
    "label":5,
    "cited_arxiv_id":"1801.04062",
    "cited_title":"MINE: Mutual Information Neural Estimation",
    "citing_paper_ssid":"549b43b1fef6294df0780da0d7ffb466aed545b5",
    "citing_title":"Neural Network Classifier as Mutual Information Evaluator",
    "citing_context":"The structure of proof is similar to the proof used in (Belghazi et al., 2018).",
    "contributions_0":"We introduce the Mutual Information Neural Estimator (MINE), which is scalable, flexible, and completely trainable via back-prop, as well as provide a thorough theoretical analysis.",
    "contributions_1":"We show that the utility of this estimator transcends the minimax objective as formalized in GANs, such that it can be used in mutual information estimation, maximization, and minimization.",
    "contributions_2":"We apply MINE to palliate mode-dropping in GANs and to improve reconstructions and inference in Adversarially Learned Inference\u00a0 on large scale datasets.",
    "contributions_3":"We use MINE to apply the Information Bottleneck method\u00a0 in a continuous setting, and show that this approach outperforms variational bottleneck methods\u00a0.",
    "contributions_4":"",
    "abstract":"We argue that the estimation of mutual information between high dimensional continuous random variables can be achieved by gradient descent over neural networks. We present a Mutual Information Neural Estimator (MINE) that is linearly scalable in dimensionality as well as in sample size, trainable through back-prop, and strongly consistent. We present a handful of applications on which MINE can be used to minimize or maximize mutual information. We apply MINE to improve adversarially trained generative models. We also use MINE to implement Information Bottleneck, applying it to supervised classification; our results demonstrate substantial improvement in flexibility and performance in these settings."
}
```
