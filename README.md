# Eco-Predict_2050
## Wildfire damage analysis and carbon recovery simulation for Pine vs. Eucalyptus forests using Python & QGIS.
## Biological Insight: 유칼립투스 특유의 "휘발성 유기화합물(Terpenes)"에 의한 과포화 연소 현상과, 한국 소나무의 낮은 맹아 갱신(Sprouting) 능력에 따른 회복 리스크 비교 분석 포함.


## 🧬 핵심 분석 및 생명공학적 해석 (Key Insight)
본 프로젝트는 단순히 산불 피해 면적을 집계하는 것을 넘어, 수종별 **생리적 회복 탄력성(Resilience)**의 차이가 2050 탄소 중립 달성에 미치는 영향을 정량적으로 입증하였습니다.

* **Biological Insight (Australia)**: 유칼립투스림은 **피해 비율 145.45%**라는 중첩 피해를 기록했습니다. 이는 휘발성 유기화합물(Terpenes)에 의한 화력 증폭 및 고온 연소의 결과이나, 강력한 에피코믹 싹(Epicormic buds) 발달로 인해 약 18.3년 내에 탄소 흡수원 기능을 복구할 수 있음을 확인했습니다.

* **Biological Insight (Korea)**: 한국 소나무림은 피해율이 8.72%로 낮았으나, 유칼립투스 대비 맹아 갱신(Sprouting) 능력이 낮아 완전 복구에 30.0년이 소요됩니다. 이는 2050년 데드라인(남은 기간 24년)을 초과하는 수치로, 생물학적으로 더 치명적인 탄소 리스크를 안고 있음을 시사합니다.

🛠 Tech Stack
Tools: QGIS (v3.x), Google Colab

Language: Python 3.x

Libraries: Pandas, Matplotlib, Seaborn, NumPy

📊 핵심 데이터 분석 결과 (Data Analysis)
1. 수종별 탄소 손실량 비교 (Carbon Loss)
산불로 인해 대기 중으로 방출된 총 탄소량을 산출한 결과, 호주 유칼립투스림이 약 6,091만 톤으로 한국 소나무림(89만 톤) 대비 압도적인 배출량을 보였습니다.

2. 2050 탄소 중립 회복 시뮬레이션 (Recovery Prediction)
각 수종의 생장률을 기반으로 분석한 결과, 한국 소나무는 현재의 낮은 회복 탄력성으로 인해 2050년 목표 달성 선(그린 가이드라인)을 초과하는 것으로 나타났습니다.

🚀 기술적 워크플로우 (Technical Workflow)
이기종 식생 데이터 통합 및 전처리: 한국 임상도(Vector)와 호주 SVTM(Raster) 데이터를 EPSG:3857 좌표계로 통일하고 속성 정보를 복구하였습니다.

산불 영향권 모델링: FIRMS 산불 데이터를 기반으로 500m 반경의 버퍼를 생성하여 공간 교차 분석을 수행하였습니다.

Troubleshooting: 래스터 재투영 시 발생하는 속성 유실 문제를 폴리곤화(Vectorization) 및 DBF 결합 공법으로 해결하여 데이터 무결성을 확보하였습니다.
