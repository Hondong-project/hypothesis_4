가설 4. 이미지(image, image_count)가 적거나, 텍스트 내용(description) 과 불일치할 경우 허위 매물일 가능성이 높다.

-> 텍스트 내용과 불일치의 경우 어떤 텍스트를 이미지와 매치해야 하는지 몰라 이미지에 변형이 일어났는지 탐지하기로 함

여러장의 매물 이미지를 불러와 특징을 추출해 그 패턴이 정상과 얼마나 다른지 image_anomaly_score로 새 컬럼 생성, image_anomaly_score는 0~1로 정규화

정생 패턴으로부터 벗어난 정도를 계산하는 이상치 탐지 알고리즘 Isolation Forest 사용
