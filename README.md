# 스타벅스와 이디야 매장 간 거리 관계 분석

## 주제 선정 이유

<img width="725" alt="스크린샷 2022-10-13 오후 5 41 06" src="https://user-images.githubusercontent.com/76437951/195547455-1bed6518-08df-42c0-ad73-f1058ce6d11e.png">

- http://www.iconsumer.or.kr/news/articleView.html?idxno=10133 
- '스타벅스 옆에 이디야가 있다', '설빙은 2층에 있다' 라는 말을 사람들이 하곤했던걸 생각해 그렇다면 과연 기사까지 난 스타벅스는 정말 이디야 옆매장을 많이 냈을까? 에 관해 ELK를 이용해 수집 처리 저장 분석 시각화를 해 볼 예정이다.

## 사용기술
- Python (3.9)
- Ubuntu
- ElasticSearch
- Logstash
- Kibana

## 구현 기능
- Map
- Metric
- Pie Chart
- Vertical Chart

## 시스템 흐름도

![elk diagram](https://user-images.githubusercontent.com/76437951/195549246-c70b1cce-63a5-4e07-be48-f0aed2794c4c.png)

## 결과
1. 서울 총 매장수 

![스크린샷 2022-10-13 오후 5 23 26](https://user-images.githubusercontent.com/76437951/195546020-2aed5bce-4656-4587-8b27-317b7f983a51.png)

2. 각 매장 점유율

![스크린샷 2022-10-13 오후 5 23 22](https://user-images.githubusercontent.com/76437951/195546140-151772a9-c166-4e3a-bf62-9b7896e1117f.png)

3. 스타벅스와 이디야 위치정보 

![스크린샷 2022-10-13 오후 5 23 18](https://user-images.githubusercontent.com/76437951/195546297-30789f56-f290-4837-be13-de19908bf42c.png)

- 갈색 원이 두 매장 간의 거리가 100m 이하인 지점

## 결론
- 앞서 보았던 내용에서 이디야가 스타벅스를 따라다녔다는 말을 이디야 대표가 하였는데 앞서 사업 초기의 전략이라 그런지 현재에 와서는 크게 의미가 없는 수의 매장만이 100m 내에 존재 하였다.
- 사업초기 데이터가 많이 없어서 정말 그런 전략을 취했느지는 알 수 없지만, 이디야는 스타벅스 옆에있다 라는 비공식 슬로건을 많은 사람들이 알고 있다는 것만으로도 바이럴에 성공했다고 볼 수 있다.

## 보완할 내용
871 개의 위치정보를 서로의 위치관계를 알기 위해 for 문을 중첩해서 사용하여 n(n^2) 의 시간이 걸려 데이터가 많으면 (전국으로 확대시) 무겁고 비효율적인 코드가 될 가능성이 매우 높음, 수정이 필요함.

