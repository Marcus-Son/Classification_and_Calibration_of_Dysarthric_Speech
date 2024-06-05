# Classification_and_Calibration_of_Dysarthric_Speech

## 소개
청각+뇌신경장애, 언어+뇌신경장애 여부를 음성 데이터의 Log Mel-Spectrogram과 Convolutional Neural Network를 사용해 분류하기 위한 프로젝트입니다. 
## 사회적 배경
- 대한후두음성언어의학회(이하 학회)의 최신 보고에 따르면, 최근 10년간 전 연령대에 걸쳐 음성 질환 환자들이 늘고 있으며, 특히 60세 이후의 환자들의 큰 폭으로 증가한 것으로 확인되었다고 합니다. 아래의 표를 보시면 60세 이상의 환자군이 큰 폭으로 상승하였습니다. 그렇기 때문에 저희는 음성 데이터 통해 구음장애(뇌신경장애, 언어청각장애, 후두장애)를 조기에 진단하여 빠른 치료를 지원하고 의료 비용 절감의 효과를 얻기 위하여 해당 주제를 선정하게 되었습니다.(https://www.medipana.com/article/view.php?news_idx=294663&sch_cate=G)
- 구음장애 데이터 중 하나인 뇌신경장애를 일으킬 수 있는 뇌종양은 전두엽 부위에 생기면 언어장애, 기억력 장애와 인지기능이 낮아지기도 하여 조기 발견이 매우 중요하다고 합니다.(https://www.100ssd.co.kr/news/articleView.html?idxno=108856)

## 기술적 배경
- 구음장애 판별은 언어 병리학자나 임상의의 청각지각에 의해 진단되는 경우가 많았습니다. 하지만 이러한 진단 방법은 전문가의 기량과 경험 그리고 환자와의 관계의 친밀도에 따라 결과가 달라질 수 있으며, 기관 방문을 위한 시간 소모와 간헐적인 대면 치료라는 한계점이 존재합니다. 그래서 이를 보완하기 위해 구음장애 발화 데이터를 딥러닝의 CNN 구조를 활용하여 질환을 가지고 있는 환자를 보다 높은 정확도로 분류하고자 시작하게 되었습니다.
- 한국인 구음장애 환자의 발화 데이터 기반 질병 예측을 위한 모바일 애플리케이션 개발 (하창진, 고태식 2023) KCI 논문의 연구에서는 원본 음성 데이터를 log-mel spectrogram으로 변환하여 구음장애의 원인 질환을 예측할 수 있는 CNN 구조의 딥러닝 모델을 구축한 선행 연구가 있는 것을 확인하였습니다.
## Dataset
-AI Hub(https://www.aihub.or.kr/)에서 배포되는 구음장애 음성인식 데이터를 사용해 학습하였습니다. 
![img](https://github.com/Marcus-Son/Classification_and_Calibration_of_Dysarthric_Speech/assets/137815765/1a581a17-8d5c-4ef2-b393-5aeec3fba967)

- 해당 데이터셋은 구음장애 중재 시 진전 과정을 모니터링하거나 여러 중재 방법들을 비교하는데 유용하게 사용하거나 병증 진단의 목표 수준을 제시하는데 활용할 수 있도록 구음장애 환자를 대상으로 1200명(5,000시간 이상 5250시간 이하)의 발화 데이터로 구축되었습니다.

<원천 데이터>
- 단어, 문장, 문단, 준 자유발화 스크립트를 대상자에게 반복하여 읽게 하여 특정 단어나 문장을 발음할 때 측정되는 within-subject variability를 포함한 데이터를 구축하였습니다.
- - Wav음성데이터 5,000시간과 쌍을 이루는 Json 데이터로 구축되어있습니다．
- Json데이터에는 생성시간, ID, 나이, 성별, 지역, 음원 파일명, Sampling Rate, 시작 위치, 종료 위치, 재생 시간, 데이터 크기가 포함되어 있습니다.
![Untitled](https://github.com/Marcus-Son/Classification_and_Calibration_of_Dysarthric_Speech/assets/137815765/aa1a8615-d4e7-4685-9f36-362d66fd0934)


## 데이터 전처리
![image](https://github.com/Marcus-Son/Classification_and_Calibration_of_Dysarthric_Speech/assets/137815765/87aea8c5-38c0-41f6-a4fd-2644240ecb72)

## 학습 및 모델 생성
![image](https://github.com/Marcus-Son/Classification_and_Calibration_of_Dysarthric_Speech/assets/137815765/7d20d9b9-95e5-41d5-aa78-4e16743c12a3)
