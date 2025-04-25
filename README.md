# COVID-19 Vaccine Side Effect and Death Analysis (VAERS 2021)  
新型コロナワクチン副作用・死亡データ分析（VAERS 2021）

## 📌 Overview  
概要

This is the code for my **first-year data science project**.  
これは私の「一年目のデータサイエンスプロジェクト」です。  

I worked with real-world data from the VAERS database to explore the relationship between **COVID-19 vaccine side effects** and **death cases**.  
VAERS（アメリカのワクチン副反応報告システム）から取得したデータを使い、**ワクチン接種後の症状と死亡**の関係を分析しました。

### 🎯 Goals / 目的

- Identify common symptoms in death cases（死亡事例でよく見られる症状の特定）
- Compare gender and vaccine brands（性別・ワクチン会社の比較）
- Visualize symptom distributions（症状の可視化）

---

## 📂 Data Source  
データソース

- Website: [https://vaers.hhs.gov/data/datasets.html](https://vaers.hhs.gov/data/datasets.html)
- Dataset: VAERS 2021 CSV
- Extracted vaccine types: **Moderna**, **Pfizer**, **Janssen**  
  （対象ワクチン：モデルナ、ファイザー、ヤンセン）

I focused on reports related to COVID-19 vaccines only.  
COVID-19ワクチンに関するデータのみ抽出しました。

---

## 🧰 Tools Used  
使用ツール

- Python
  - `pandas`（データ処理）
  - `matplotlib`, `seaborn`（グラフ・可視化）
- Jupyter Notebook（ノートブックで分析を実行）

---

## 📊 What I Did  
分析内容

### 1. Vaccine Doses and Deaths  
ワクチン接種数と死亡者数

- Compared death counts by **vaccine brand** and **gender**  
  ワクチンの種類・性別別の死亡件数を比較しました。
- Found that death reports were higher among **males**  
  男性の方が死亡報告数が多い傾向がありました。

### 2. Symptoms Found in Death Cases  
死亡者に見られた症状の分析

| Symptom             | 日本語訳           |
|---------------------|-------------------|
| Fatigue             | 倦怠感              |
| Pyrexia             | 発熱               |
| Dyspnoea            | 呼吸困難            |
| Cardiac arrest      | 心停止              |
| Acute kidney injury | 急性腎障害          |

Mild symptoms like fatigue or fever were common but rarely fatal.  
軽い症状（発熱や倦怠感など）はよく見られましたが、死亡にはつながりにくい傾向がありました。

Severe symptoms like **dyspnoea** or **organ failure** were often present in death cases.  
呼吸困難や臓器系の異常は、死亡事例で多く見られました。

### 3. Gender and Brand Comparison  
性別・ワクチン会社別の比較

- 女性の報告数は多いが、男性の死亡率が高い  
- 症状の出現傾向はブランドごとに大差なし  
- Janssenのデータは件数が少なく慎重に扱う必要あり

---

## 📈 Visualizations  
グラフ可視化

- Death counts by gender and vaccine brand（性別×ワクチンの死亡数）
- Top symptoms in death reports（死亡例で多い症状）
- Symptom ratios by gender（性別による症状分布）

Graphs are saved in the `/figures/` folder.  
可視化した図は `/figures/` フォルダに保存されています。

---

## 🧠 Key Insights  
主な発見

- Mild symptoms = low risk（軽度の症状はリスクが低い）
- Organ/respiratory symptoms = high fatality risk（臓器や呼吸の異常は死亡率が高い）
- Male deaths higher, but cause unclear（男性の死亡率は高いが、原因は不明）

---

## ❗ Limitations  
課題と限界

- Age and medical history not included（年齢や持病の分析は未対応）
- Causation not proven, only correlation（因果関係ではなく相関）
- Janssen data is limited（ヤンセンのデータが少ない）

---

## 🚀 Future Work  
今後の展望

- Try statistical testing（統計的検定の導入）
- Use machine learning models for prediction（機械学習による予測モデルの構築）
- Include age and health data（年齢や健康情報の組み込み）

---

## 📝 Disclaimer  
免責事項

This project is for educational purposes only.  
本プロジェクトは学習・研究目的で行ったものであり、  
医学的なアドバイスや結論を提供するものではありません。



