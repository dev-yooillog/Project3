# Mercedes-Benz Sales Analysis
**Machine Learning & EDA approach for Luxury EV Market Strategy**

---

## Problem Statement

Mercedes-Benz 판매 데이터(2020–2025)를 분석하여 가격 탄력성과 EV 전환 추이를 도출하고,
이를 바탕으로 제네시스 EV 라인업의 북미/유럽 시장 진입 전략을 제안합니다.

---

## Tech Stack

`Python 3.10` · `Pandas` · `NumPy` · `Scikit-learn` · `Matplotlib` · `Seaborn` · `SciPy`

---

## Project Structure

```
mercedes-ev-analysis/
├── data/
│   ├── raw/                         # 원본 데이터
│   └── processed/
│       ├── mercedes_processed.parquet
│       ├── eq_series.parquet
│       └── price_elasticity.csv
├── notebooks/
│   ├── 01_eda.ipynb                 # 판매량 탐색 및 분포 분석
│   ├── 02_ev_analysis.ipynb         # EV 전환 추이 분석
│   ├── 03_price_elasticity.ipynb    # 가격 탄력성(PED) 분석
│   └── 04_genesis_strategy.ipynb    # 제네시스 진입 전략 도출
├── src/
│   ├── preprocess.py                # 전처리 모듈
│   ├── elasticity.py                # PED 계산 모듈
│   └── visualize.py                 # 시각화 모듈
├── outputs/
│   └── figures/                     # 생성된 차트 이미지
├── Report.md                        # 상세 분석 보고서
└── README.md
```

---

## Analysis Pipeline

```
Raw Data
  → EDA (판매량 분포, 연도별 추이)
  → EV 전환 추이 분석 (세그먼트별 침투율)
  → PED 계산 (모델×연도 집계 → 탄력성 분류)
  → 가격 포지셔닝 맵 (Mercedes vs Genesis)
  → 전략 제언 도출
```

---

## Key Results

| 분석 항목 | 결과 |
|---|---|
| 최다 판매 모델 | GLC (약 2,100,000대) |
| 전체 판매 정점 | 2023년 (2,301,289대) |
| EV 비중 (2025) | 30.0% |
| EV 세그먼트 PED | 비탄력적 (중앙값 -0.3 ~ -0.5) |
| EV 가격 CAGR | 평균 3.5% / yr |

---

## Business Insights

- EV 세그먼트는 가격 비탄력적 — 브랜드 구축 후 점진적 가격 인상 전략 유효
- 2023년 EV 비중 10% 돌파 — 제네시스 진입 적기
- 제네시스는 엔트리~중형 구간에서 벤츠 대비 $2K~$14K 저렴한 가격으로 경쟁력 확보 가능

자세한 내용은 [Report.md](./Report.md)를 참고하세요.

---

## Quickstart

```bash
pip install pandas numpy scikit-learn matplotlib seaborn scipy pyarrow
jupyter notebook notebooks/01_eda.ipynb
```