
# IR - Information retrieval 

구조화되지 않은 자연상태 ( 일반적으로 텍스트 )의 자료를 찾고 큰 컬렉션으로부터 정보 필요를 만족시키는 것

# 검색 문서의 퀄리티 판별

● 정확도(Precision) : 사용자 정보 필요와 관계있는 정보 문서들의 집합

● 재현율(Recall) : 검색되는 컬렉션 안에 관계 있는 문서들의 집합

# Boolean retrieval ( 불리언 검색 )

● 불리언 모델은 정보 검색 시스템을 기초로 한 가장 간단한 모델

● 쿼리는 불리언 표현식이다 e.g., CAESAR AND BRUTUS

# Google이 Boolean Model을 사용할까?

● Google에서 쿼리 [w1 w2 ... wn] 의 기본적인 해서은 w1 AND w2 AND ... AND wn이다.

● wi 중 하나를 포함하지 않는 케이스들

- 앵커 테스트 ( 링크를 걸 때 '이곳을 클릭하세요' 등과 같이 기입하는 텍스트를 뜻 )
- wi의 변수를 포함하는 페이지 ( morphology - 형태소, 스펠링 오류, 동의어 )
- 긴 쿼리

# Inverted Index

<img src="https://user-images.githubusercontent.com/13411738/64319431-4b608800-cff7-11e9-874c-ad8f2381f157.png" width="800">

# Inverted Index Construction

1. 색인할 문서 수집
2. 텍스트를 토크나이즈 하고, 각 문서를 토큰들의 리스트로 변환
3. 언어 전처리 하고, 정규화된 토근 리스트를 생산하고, 색인화된 용어 생성
4. 역순 인덱스를 만들어서 각 용어에서 나타나는 문서들을 색인화하고, 딕셔너리와 포스팅으로 구성한다.

<img src="https://user-images.githubusercontent.com/13411738/64320880-608ae600-cffa-11e9-8c2e-7dfc0b4634e4.png">



