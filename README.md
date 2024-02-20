# [Air Quality Data Web Application with Django](https://github.com/jwchoi622/aqproj)
## Overview
This project is a Django-based web application designed to provide up to date air quality information for any city in the world. I used the AQICN API to get the air quality data and Leaflet to get the map on the website. Lastly I used PythonAnywhere to deploy the application. The application is accessible at [https://jwchoi622.pythonanywhere.com](https://jwchoi622.pythonanywhere.com). 
## Features
- **Air Quality Information:** The first table will give the current air quality information for the city that the user inputs. It also includes a widget 
  that has a concise summary of current air quality for that city. Not all cities will get a widget because the API seems to only return a widget for major cities. 
  It also may not have information on all of the different types of pollutants such as CO or O3. 
- **Interactive Map:** The map will be centered on the queried city and also have tiles that indicate the AQI index for different neighborhoods within the city. 
  Smaller cities may not have as many tiles because they do not have as many air quality sensors. The user can also zoom in or zoom out to look at neighboring cities. 
- **PM 2.5 Forecast:** The forecast focuses on PM 2.5 because it is the most harmful of pollutants and also a big problem in Korea. The forecast will usually show 
  the PM 2.5 forecast for the next couple days in the week and have color coded dates according to the average level for that date. 
- **Calendar:** The calendar will indicate which days are safe for outdoor activity by looking at the PM 2.5 index. 

## Future Improvements
- Adding a forecast for PM10 would also be helpful in determining what the air quality would be like for future days.
- The calendar could also include markers for good, average and poor air quality.
- Including different language options.

## External APIs Used
### AQICN API
- **Description:** I used this AQICN to get the air quality data, widget, forecast data and also the map tiles.
- **Documentation:** [https://aqicn.org/api/](https://aqicn.org/api/)
### Leaflet API
- **Description:** I used the Leaflet API to get an interactive map of the queried city.
- **Documentation:** [https://leafletjs.com/reference.html](https://leafletjs.com/reference.html)
### OpenCage Geocoding API
- **Description:** I used the OpenCage API to get the latitude and longitude of the city and fed those coordinates into the Leaflet map. 
- **Documentation:** [https://opencagedata.com/api](https://opencagedata.com/api)
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

