# CodeStates Project 2 _ Movie Recommendation System
Team.K </br>
Teammate: Hyejin Oh(@nryeo), Youngjo Choi(@stebechoi)

---
### Project Background
- 국내 유명 영화 사이트 '네이버 영화' 운영 종료
- 해외에는 TMDB등 거대 영화 평점 사이트가 존재하나, 네이버 영화의 종료로 국내 공백 발생
- 넷플릭스, 디즈니 등의 OTT서비스가 영화 평점 및 랭킹 기반 추천을 제공하나 자사 보유 영화 대상
- 단순히 가입한 서비스에 존재하는 영화가 아닌, 보고 싶은 영화를 위해 서비스에 가입하는 고객의 니즈 존재

### Project Goal
- Broad: 특정 제작사, 배급사에 구애되지 않는 일반적인 영화 추천이라는 비즈니스 기회 발굴
- less broad: 프로젝트 역량 발굴 및 강화
- Specific: 영화 추천 시스템 개발

### Team
- Hyejin : EDA, RecSys(CB, CF, SVD), PPT
- Youngjo : RecSys(MF, FM, DeepFM)

### Data
- MovieLens 100K 이용
- 결측치 삭제
- rating 분포 파악, 지역(zipcode기반), 월별(timestamp기반), 성별 분포 확인
- 성별, 직업, 지역 등의 데이터 수가 차이가 많이 나서 사용자 프로필 기반 추천이 어려움

### RecSystem
- CB / CF / SVD
- MF / FM / DeepFM

### Application
- Hybrid Filtering
  - 비회원/신규회원/복귀회원의 경우 rating이 적거나, 과거와 동일한 취향으로 단정할 수 없다.: CB+CF 적용
    → 좋아하는 영화가 주어지면, 내용 기반 추천 5개, CF_KNN기반 추천 5개로 총 10개의 영화 추천리스트 반환
    
