# App Store Game Dataset EDA

## 프로젝트 소개
이 프로젝트는 [Kaggle의 App Store Game dataset](https://www.kaggle.com/datasets/kanchana1990/gamesphere-2000-app-store-insights-and-ratings)을 활용하여 EDA(Exploratory Data Analysis)를 수행한 결과를 공유합니다. 데이터 분석을 통해 게임 어플 마케팅 전략을 수립하는 것이 이 프로젝트의 목표입니다.

## 팀원
- 윤장원
- 윤정희
- 백승훈
- 박서연

## 분석 주제
이 프로젝트는 다음 5가지 주제로 구성되었습니다:
1. **게임 카테고리화 하여 출시 연도별 또는 월별 게임 출시 패턴 분석**
    - 어떤 시기에 주로 어떤 게임이 출시되는지, 그리고 그 게임들의 평점은 어떤지 분석합니다.
2. **게임 설명 텍스트에서 어떤 테마 또는 특징이 평점과 연관이 있는가?**
    - 게임 설명과 릴리스 노트 안 어떤 특징이나 테마가 사용자들에게 더 만족감을 선사했는지, 평점 수가 많아졌는지 분석합니다.
3. **사용자 평점 수(userRatingCount)가 많을수록 averageUserRating이 높을까?**
    - 사용자 평점 수와 평균 사용자 평점 사이의 상관관계를 조사합니다.
4. **연령 적합성(contentAdvisoryRating), 최소 요구 버전(minimumOsVersion), 출시 날짜(releaseDate), 가격(price)이 낮을수록 평점 개수(userRatingCount)가 높을까?**
    - 다양한 요인들이 사용자 평점 수에 미치는 영향을 분석합니다.
5. **애플 로그인 연동 여부(isGameCenterEnabled)가 true이면 평점 개수(userRatingCount)가 높을까?**
    - 애플 로그인 연동 여부와 사용자 평점 수 사이의 관계를 조사합니다.

## 사용된 툴
- **Google BigQuery**: 대용량 데이터셋을 저장하고 쿼리하는 데 사용되었습니다.
- **Google Colab**: 데이터 분석 및 시각화를 수행하는 데 사용되었습니다.

## 프로젝트 구조
1. **데이터 준비**
    - Kaggle에서 데이터를 다운로드하여 Google BigQuery에 업로드합니다.
    - Google Colab에서 BigQuery와 연동하여 데이터를 불러옵니다.
2. **데이터 분석**
    - 주제별로 데이터를 분석하고 시각화합니다.
3. **결과 도출**
    - 분석 결과를 바탕으로 마케팅 전략 또는 가설을 수립합니다.

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

