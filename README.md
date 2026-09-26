# Jeehun Han — Data Engineer | Analytics Engineer

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=flat-square&logo=snowflake&logoColor=white)
![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat-square&logo=dbt&logoColor=white)

데이터를 안정적으로 만들고, 분석 가능한 형태로 제공하는 **Data Engineer / Analytics Engineer**를 목표로 하고 있습니다.

Python과 SQL을 기반으로 데이터 수집·적재·변환·모델링까지 연결하는 파이프라인을 구현하고 있습니다. Airflow, Snowflake, dbt, Databricks를 활용해 재현 가능한 실행 환경과 분석용 데이터마트를 설계하는 역량을 강화하고 있습니다.

## What I Build

- 다양한 원천 데이터를 수집하고 재실행 가능한 배치 파이프라인으로 적재합니다.
- Raw / Stage / Mart 또는 Bronze / Silver / Gold 계층으로 데이터를 분리합니다.
- 데이터의 grain, unique key, 중복 처리 기준을 정의해 분석에 사용할 수 있는 모델을 만듭니다.
- SQL과 dbt를 활용해 분석가와 대시보드가 신뢰할 수 있는 데이터마트를 제공합니다.

## Core Strengths

### Data Engineering

- Python·SQL 기반 데이터 수집 및 ETL 파이프라인
- Airflow DAG 오케스트레이션
- Snowflake·Databricks 기반 데이터 적재 및 변환
- Docker 기반 재현 가능한 실행 환경
- 멱등성, 증분 적재, 재처리 구조에 대한 이해
- 데이터 품질과 파이프라인 실행 흐름을 고려한 설계

### Analytics Engineering

- 모호한 사용자·비즈니스 니즈를 관측 가능한 데이터와 지표, 검증 기준으로 구체화
- dbt 기반 Raw / Stage / Mart 모델링
- 데이터 grain과 unique key를 고려한 SQL 설계
- 분석용 데이터마트 및 교차 브랜드 데이터 모델 구축
- 중복·결측·스키마를 확인하는 데이터 품질 검증

## Featured Projects

### [OTT Data Pipeline by Databricks](https://github.com/meanresult/ott_data_pipeline_by_Databricks)

> Databricks에서 OTT 데이터를 적재·정제·집계하고, 분석에 사용할 수 있는 Gold 데이터를 구축한 프로젝트

- **Data Engineering:** 원본 CSV를 명시적 스키마로 적재하고 Bronze → Silver → Gold 구조로 변환
- **Analytics Engineering:** 정제 데이터를 분석 목적에 맞게 집계하고 Gold 레이어로 제공
- 중복 데이터를 `*_dup` 테이블로 분리해 적재 흐름과 품질 점검을 구분
- `DeltaTable API + DataFrame merge` 방식으로 Silver 적재 시간을 **22초에서 4초로 개선**
- **Stack:** Databricks · PySpark · Spark SQL · Delta Lake

### [Celebrity Recommend](https://github.com/meanresult/celebrity-recommend)

> Instagram 브랜드 태그 데이터를 수집해 함께 태그된 브랜드와 계정을 분석하는 데이터 파이프라인

- **Data Engineering:** Playwright 기반 수집기와 브랜드별 Airflow DAG를 구성하고 Snowflake에 적재
- **Analytics Engineering:** Snowflake의 Raw → Staging → Mart 계층과 dbt 모델을 구성
- “인스타 패션 유저의 취향은 무엇인가?”라는 질문을 팔로잉 데이터가 아닌 게시물의 브랜드 태그와 공동 태그 패턴으로 정의
- 브랜드별 작업을 분리해 파이프라인 장애 범위를 줄이고 재실행 가능한 흐름을 설계
- `cross_brand_accounts` Mart를 통해 교차 브랜드 계정 분석이 가능하도록 데이터 제공
- Streamlit 대시보드와 연결해 수집 데이터와 분석 결과를 조회
- **Stack:** Playwright · Airflow · Snowflake · dbt · Streamlit · Docker

### [Data Pipeline Training](https://github.com/meanresult/data-pipeline-traning)

> 데이터 수집부터 적재·변환까지의 기본적인 운영 흐름을 반복 구현하며 정리한 프로젝트

- **Data Engineering:** Airflow와 Docker Compose를 사용해 로컬에서 재현 가능한 배치 환경 구성
- **Analytics Engineering:** Raw / Staging / Mart 레이어를 분리해 분석용 데이터 흐름을 구성
- Snowflake `MERGE`를 활용해 동일 데이터가 재처리되어도 중복 적재되지 않는 upsert 구현
- DAG 작업을 단계별로 분리해 수집, 적재, 변환 흐름을 확인할 수 있도록 구성
- **Stack:** Airflow · Snowflake · Docker · Python · SQL

## Engineering Focus

```text
Source Data
    ↓
Ingestion & Validation
    ↓
Raw Layer
    ↓
Transformation & Modeling
    ↓
Stage / Silver Layer
    ↓
Mart / Gold Layer
    ↓
Dashboard & Analysis
```

현재는 다음 주제를 중심으로 프로젝트를 개선하고 있습니다.

- 멱등성 있는 배치와 증분 적재
- 데이터 품질 검증과 실패 원인 추적
- 분석 목적에 맞는 grain과 데이터 모델 설계
- Airflow 재실행 및 backfill 상황을 고려한 파이프라인 구성
- 파이프라인 결과를 분석가와 대시보드가 쉽게 사용할 수 있는 Mart로 제공

## Tech Stack

**Data Engineering**

![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=flat&logo=apacheairflow&logoColor=white)
![Spark](https://img.shields.io/badge/Spark-E25A1C?style=flat&logo=apachespark&logoColor=white)
![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=flat&logo=databricks&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

**Analytics Engineering & Data Platform**

![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=flat&logo=snowflake&logoColor=white)
![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat&logo=dbt&logoColor=white)
![Delta Lake](https://img.shields.io/badge/Delta%20Lake-0A84FF?style=flat&logo=databricks&logoColor=white)

**Language & Visualization**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=mysql&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat&logo=streamlit&logoColor=white)

## Currently Strengthening

- Airflow, Spark, Snowflake, dbt 기반 파이프라인의 실행 흐름과 데이터 모델을 반복적으로 개선하고 있습니다.
- 증분 적재, 멱등성, 데이터 품질 검증을 실제 프로젝트에 적용하고 있습니다.
- 분석가가 바로 사용할 수 있는 데이터마트와 지표 구조를 설계하는 연습을 하고 있습니다.
- Databricks와 Delta Lake 환경에서 처리 성능과 저장 구조를 함께 개선하고 있습니다.

## Contact

- Email: jeehunhan0420@gmail.com
- GitHub: [github.com/meanresult](https://github.com/meanresult)
