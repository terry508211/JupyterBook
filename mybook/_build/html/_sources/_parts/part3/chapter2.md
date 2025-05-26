# 因子分析
分析因子對未來報酬之預測能力（IC）、區分未來股票高低報酬區間的能力（分組單調性）與因子值變動的頻率與持續性（分組週轉率）。

<!-- :::{contents}
:local:
:depth: 2
::: -->

## IC資訊係數檢定

檢驗t日因子值與t+N日期間報酬的相關性，相關性絕對值越高代表因子預測個股未來報酬能力越好。由於Pearson要求資料為常態分布，若非常態分布容易失準，因此均使用Spearman相關係數進行計算，公式如下：

$$
\text{Rank IC}_t = \text{Corr}\left(x_{\text{rank}}^t,\ \text{ret}_{\text{rank}}^{t+N} \right)
$$

其中因子在t日的IC值，使用t日排序後因子值與t日至t+N日的排序後個股報酬連乘的共變異數，除以t日排序後因子值標準差和t+N日的排序後個股報酬標準差。
N日依照使用者前面選擇的投組再平衡頻率各有不同，若選擇每月初再平衡則N為21日；每週初再平衡為5日；每日初再平衡為1日。

![alt text](image-4.png)

上圖各數值公式整理如下：
- IC平均值：回測期間所有t日的RankIC總和取平均，判斷因子預測能力顯著與否，公式如下：

    $$
    \text{RankIC} = \frac{1}{N} \sum_{t=1}^{N} \text{RankIC}_t
    $$

    其中N為總樣本期間。
    <br>

- IC標準差：回測期間所有t日的RankIC值取標準差，判斷因子預測能力穩定與否，公式如下：

    $$
    \sigma(\text{RankIC}) = \text{Std}(\text{RankIC}_t), \quad t \in [0, N]
    $$

    其中N為總樣本期間。
    <br>

- 風險調整後IC（IR）：將IC平均值除以同期間IC標準差，判斷因子預測能力有效性，公式如下：

    $$
    \text{IR} = \frac{\text{RankIC}}{\sigma(\text{RankIC})}
    $$

    <br>

- IC統計T、P值：計算IC平均值是否顯著異於0，判斷因子預測能力是否統計上顯著，公式如下：

    $$
    t = \frac{\text{RankIC} - \mu_0}{s / \sqrt{n}}
    $$

    $$
    p = P(T \geq |t| \mid H_0^a)
    $$

    其中$μ_0$為虛無假設下之檢定值，此處為0；s為樣本標準差；n為樣本大小。$P(T \geq |t| \mid H_0^a)$則為t統計量的累積機率。

    <br>

- IC偏度、峰度：計算IC值分布的對稱性與集中程度，公式如下：

    $$
    IC_{\text{skew}} = \frac{1}{n} \sum_{i=1}^{n} \frac{(x_i - \bar{x})^3}{s^3}
    $$

    $$
    IC_{\text{kurt}} = \frac{1}{n} \sum_{i=1}^{n} \frac{(x_i - \bar{x})^4}{s^4}
    $$

    其中$x_i$為第i日的RankIC值；x為整個樣本期間的RankIC平均值；n為總樣本期間。
    <br>

- IC大於0%比例：統計每一個t日IC值高於0%占整個樣本期間比例，判斷因子預測能力方向穩定性。
<br>

- 每月IC值：為該月份每一個t日IC值總和取平均。
<br>

- 累加IC值：回測期間每一個t日IC值累加，判斷因子預測能力在時序列上是否具有單調性。


## 分組報酬單調性


## 分組週轉率


