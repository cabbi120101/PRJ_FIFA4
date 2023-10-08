# PRJ_FIFA4
넥슨 피파온라인 API를 활용한 프로젝트 기록
디스코드로 서비스 제공

### 기능 - 아이디어
#### 닉네임 검색시 나오는 정보
1. 자주 득점하는 선수 TOP3 : 선수 이미지
   - 마크 해야하는 선수 알려주기
   - 선수의 최근 이적시장 가격 추가
2. 자주 득점하는 위치(어시->골 루트) : 경기장 이미지에 표시
   - 자주 사용하는 공격루트 파악
   - 자주 사용하는 슛팅 방법 및 골 결정력(성공률)
3. 자주 득점 당하는 위치 : 경기장 이미지에 표시
   - 자주 당하는 공격루트 제공
4. 득점 당한 선수 TOP 3 : 선수 이미지
   - 약한 팀을 유추할 수 있게 or 가능하면 자주진 팀의 스쿼드 정보, 포메이션 정보 제공
   - 선수의 최근 이적시장 가격 추가
5. 승률 예측
    - 최근 10경기의 평균 데이터를 가지고 승률 예측

### 개발 일지
1. 10월 06일 : 
    - 2번 기능 시험 제작 성공
    - 최근 10 경기 합해서 자동화하여 제공 예정
2. 10월 07일 :
    - 2번 기능 자동화 성공
    - 닉네임 입력시 최근 10경기의 어시->골 경로를 표시 (골 넣은 것, 먹힌 것 모두)
    - 기능 1,4의 자주 득점하는 선수 목록 예정
3. 10월 08일 :
    - 승률 예측 모델 제작 중
    - 기능 1,4 선수 이미지 추가하여 제작 예정
4. 10월 09일 :
    - 데이터를 추가하여 모델 제작 (현재 시즌 상위 60명의 최근 100경기 데이터 사용)
    - 최종 lightgbm로 모델 제작 : R^2=0.8676
    - 경기평점, 짧은 패스, 점유율, 침투 패스가 주요 Feature인 것을 알 수 있음
    