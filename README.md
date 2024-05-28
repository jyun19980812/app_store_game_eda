# App Store Game Dataset EDA

## 프로젝트 소개
이 프로젝트는 [Kaggle의 App Store Game dataset](https://www.kaggle.com/datasets/kanchana1990/gamesphere-2000-app-store-insights-and-ratings)을 활용하여 EDA(Exploratory Data Analysis)를 수행한 결과를 공유합니다. 본 데이터 분석 프로젝트는 게임 애플리케이션의 마케팅 전략을 수립하는 데 중점을 두고 있으며, 다음과 같은 긍정적인 효과를 기대해 볼 수 있습니다:

1. **사용자 참여 증진**: 게임 설명 및 게임 센터 연동 여부가 사용자 참여도와 평점에 미치는 영향을 분석함으로써, 사용자 참여를 극대화할 수 있는 요소를 파악합니다.
2. **시장 트렌드 파악**: 출시 연도별 및 월별 게임 출시 패턴을 분석하여, 특정 시기에 인기 있는 게임 유형을 파악합니다.
3. **마케팅 전략 최적화**: 다양한 게임의 특성(파일 크기, 가격, 연령 적합성 등)이 평점과 사용자 반응에 미치는 영향을 분석함으로써, 마케팅 전략을 더욱 효과적으로 설계할 수 있습니다.

이 프로젝트는 EDA를 통해 모바일 게임 개발자와 마케터들에게 유용한 인사이트를 제공하고, 경쟁력 있는 게임 개발 및 마케팅 전략을 수립하는 데 기여할 것입니다.

## 팀원 및 담당 분석 주제
- **윤장원** - 주요 분석: **게임 카테고리화 및 출시 패턴, 게임 설명 텍스트와 평점 연관성 분석**
- **박서연** - 주요 분석: **사용자 평점 수와 평균 평점의 상관관계, 파일 크기와 평균 평점 관계**
- **윤정희** - 주요 분석: **연령 적합성, 최소 요구 OS 버전, 출시 날짜가 평점 개수에 미치는 영향**
- **백승훈** - 주요 분석: **애플 로그인 Game Center 연동 여부와 사용자 평점 수 관계 분석**

## 사용된 툴
- **Google BigQuery**: 대용량 데이터셋을 저장하고 쿼리하는 데 사용되었습니다.
- **Google Colab**: 데이터 분석 및 시각화를 수행하는 데 사용되었습니다.
- **Excel**: 데이터 분석 및 시각화를 수행하는 데 사용되었습니다.

## 프로젝트 구조
1. **데이터 준비**
    - Kaggle에서 데이터를 다운로드하여 Google BigQuery에 업로드합니다.
    - Google Colab에서 BigQuery와 연동하여 데이터를 불러옵니다.
2. **데이터 분석**
    - 주제별로 데이터를 분석하고 시각화합니다.
3. **결과 도출**
    - 분석 결과를 바탕으로 마케팅 전략 또는 가설을 수립합니다.

## 프로젝트 리포트 & 코드
저희 EDA에 대한 리포트는 **[리포트](./리포트/)** 폴더에 포함되어 있습니다. 이 리포트에서는 프로젝트 소개 및 선정 이유, 데이터 전처리 및 파악, 프로젝트 세부 분석, 결론 및 마케팅 전략 등을 다루고 있습니다.
또한, 이 EDA를 진행한 코드는 **[Google Colab](https://colab.research.google.com/drive/1FY7b-i0CSM4RsyANYZWApFM0oB0Ta6L5?usp=sharing)** 에서 확인 가능합니다.

## 설치 및 사용 방법
1. Kaggle에서 [App Store Game dataset](https://www.kaggle.com/datasets/kanchana1990/gamesphere-2000-app-store-insights-and-ratings)을 다운로드합니다.
2. 데이터를 Google BigQuery에 업로드합니다.
3. Google Colab 노트북을 열고, BigQuery와 Colab을 연동합니다.
4. Colab 노트북에서 아래 코드를 실행하여 데이터를 불러옵니다:
    ```python
    from google.colab import auth
    auth.authenticate_user()

    from google.cloud import bigquery
    os.environ["GOOGLE_CLOUD_PROJECT"]=project_id

    %%bigquery example
    SELECT * 
    FROM `your-dataset-id.your-table-id`
    ```
5. 분석을 진행합니다.

