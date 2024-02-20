# [Project 1: Air Quality Data Web Application](https://github.com/jwchoi622/aqproj)
# **대기질 지수 웹 애플리케이션**
## **개요**
이 프로젝트는 세계 어느 도시의 최신 대기질 정보를 제공하기 위해 Django 기반으로 설계된 웹 응용 프로그램입니다. AQICN API를 사용하여 대기질 데이터를 가져오고, 웹사이트에 지도를 표시하기 위해 Leaflet를 사용했습니다. 마지막으로 PythonAnywhere를 사용하여 응용 프로그램을 배포했습니다. 이 응용 프로그램은 https://jwchoi622.pythonanywhere.com에서 접근할 수 있습니다.

## **기능***
**대기질 정보:** 첫 번째 표는 사용자가 입력한 도시의 현재 대기질 정보를 제공합니다. 또한 해당 도시의 현재 대기질에 대한 간결한 요약이 포함된 위젯도 포함되어 있습니다. API는 주요 도시에 대해서만 위젯을 반환하는 것 같아 모든 도시에 위젯이 제공되지는 않습니다. 또한 CO나 O3과 같은 다양한 종류의 오염 물질에 대한 정보가 없을 수도 있습니다.

**인터랙티브 지도:** 지도는 조회된 도시를 중심으로 표시되며, 도시 내 다른 지역의 AQI 지수를 나타내는 타일도 있습니다. 작은 도시는 대기질 센서가 많지 않아 타일이 적을 수 있습니다. 사용자는 인접 도시를 살펴보기 위해 확대하거나 축소할 수도 있습니다.

**PM 2.5 예보:** 예보는 PM 2.5가 가장 해로운 오염 물질이며 한국에서도 큰 문제이기 때문에 PM 2.5에 초점을 맞춥니다. 예보는 보통 다음 며칠 동안의 PM 2.5 예보를 보여주며, 해당 날짜의 평균 수준에 따라 색상이 코드화된 날짜를 표시합니다.
달력: 달력은 PM 2.5 지수를 보고 야외 활동에 안전한 날을 표시합니다.

## **개선사항**
-PM10에 대한 예보를 추가하는 것도 향후 대기질을 판단하는 데 도움이 될 것입니다.   
-달력에도 좋음, 보통, 나쁨 대기질에 대한 표시를 포함할 수 있습니다.  
-다양한 언어 옵션을 포함시킵니다.  

## **사용된 API**
**AQICN API**  
설명: AQICN API를 사용하여 대기질 데이터, 위젯, 예보 데이터 및 지도 타일을 가져왔습니다.  
문서: https://aqicn.org/api/  

**Leaflet API**  
설명: Leaflet API를 사용하여 조회된 도시의 인터랙티브 지도를 가져왔습니다.  
문서: https://leafletjs.com/reference.html  

**OpenCage 지오코딩 API**  
설명: OpenCage API를 사용하여 도시의 위도와 경도를 가져오고 이 좌표를 Leaflet 지도에 입력했습니다.  
문서: https://opencagedata.com/api  
![](/images/pic2.png)

# [End-to-End Azure Data Engineering Project](https://github.com/jwchoi622/TokyoOlympics)
## Overview
This project is an Azure-based data engineering project, focusing on the entire data pipeline from ingestion to visualization. It starts with data preprocessing, leveraging Azure Data Factory for ingestion and Databricks for transformation. The project demonstrates effective use of Azure's ecosystem, emphasizing learning and skill development within Azure services. Key components include handling Kaggle datasets, data transformation, analytics with Azure Synapse, and visualization with Tableau due to compatibility considerations. This project serves as an introductory exploration into Azure platform capabilities, data pipeline design, and data insight generation.
![](/images/pipeline.png)

## Technologies Used
- Azure Data Factory
- Azure Databricks
- Azure SQL Database
- Azure Data Lake
- Tableau

## Additional Resources
- **Project Walkthrough on Medium**: A comprehensive overview of the project's data engineering process on Azure. [Read the article here](https://medium.com/@jwchoi622/end-to-end-azure-data-engineering-project-73ade8163e91).
- **Tokyo Olympics Dashboard on Tableau**: Interactive visualizations showcasing insights derived from the Tokyo Olympics dataset. [View the dashboard here](https://public.tableau.com/app/profile/james.choi1221/viz/TokyoOlympics_17022794668810/TokyoOlympicsDashboard?publish=yes).
![](/images/dashboard.png)


# [Project 3: UFC Fighter Image Classification](https://github.com/jwchoi622/fighterClassification)
# **UFC 파이터 이미지 분류 프로젝트**
## **개요**
이 프로젝트는 파이터의 이미지를 정확하게 식별하고 분류할 수 있는 이미지 분류 모델을 개발하는 것을 목표로 합니다. 본 모델은 컨볼루션 신경망(CNN)을 사용하여 준비된 데이터셋에서 파이터들의 시각적 특징을 바탕으로 서로 다른 파이터들을 구별하도록 학습합니다.

파이터 이미지를 정확하게 분류하는 것은 포즈, 조명, 배경, 장비 등의 다양성으로 인해 도전적입니다. 이러한 변이성은 같은 파이터의 다른 이미지들 간에 일관된 특징을 식별하는 복잡성을 도입하며, 다른 파이터들의 이미지와 구별합니다.

## **해결책**
이 도전과제를 해결하기 위해, 우리는 파이터의 이미지에서 미묘한 시각적 패턴을 포착하도록 맞춤화된 CNN 기반 모델을 개발했습니다. 해결책은 몇 가지 주요 단계를 포함합니다:

**데이터 준비:** 파이터 클래스에 해당하는 라벨이 붙은 이미지를 수집합니다. 이 데이터셋은 모델이 새로운, 보지 못한 이미지에 잘 일반화할 수 있도록 훈련 및 검증 세트로 분할됩니다.

**모델 구조:** CNN 모델은 이미지의 계층적 패턴에서 추출하고 배우도록 설계된 여러 레이어로 구성됩니다. 저수준 기능들을 포착하는 컨볼루션 레이어로 시작하여, 모델은 점진적으로 각 파이터의 독특한 시각적 서명을 정의하는 더 추상적인 기능들로 발전합니다.

**훈련 및 평가:** 모델은 분류 오류를 최소화하는 데 중점을 두고 훈련 데이터셋을 사용하여 훈련됩니다. 성능은 검증 세트에서 평가되어 정확성과 일반화 능력을 보장합니다.

## **구현 세부사항**
**데이터 증강:** 모델의 견고성을 향상시키기 위해 회전, 크기 조정, 수평 뒤집기와 같은 데이터 증강 기술이 사용됩니다.

**최적화:** 모델은 최상의 성능을 달성하기 위해 세밀하게 조정된 이진 교차 엔트로피 손실 함수와 함께 Adam 최적화기를 사용합니다.

**메트릭:** 모델 성능 평가에는 정확도가 주요 메트릭으로 사용됩니다. 이외에도 정밀도와 재현율과 같은 다른 메트릭들이 통찰력을 제공하는 데 사용됩니다.

![](/images/fightergraph.png)

