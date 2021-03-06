---
layout: post
title: 네이버 데뷰 2015 참가기 2일차 - 기계 번역을 이용한 검색어 수정 시스템
author: 박연오(bakyeono@gmail.com)
date: 2015-09-15
tags: 네이버 데뷰 검색 기계번역
---
* table of contents
{:toc}

> 내가 근무하고 있는 회사의 지원으로 네이버 데뷰 2015에 참가할 수 있었다. 매우 유익하고 즐거운 행사였다! 이런 행사에 참가할 수 있다니, 정말 서울에 와서 일하길 잘했다는 생각이 들었다. 몇가지 흥미로웠던 세션을 정리해 둔다.

## 2일차 세션 2. 기계 번역 모델 기반 질의 교정 시스템

발표자: 김태일(NAVER)

슬라이드: [http://www.slideshare.net/deview/242-52779038](http://www.slideshare.net/deview/242-52779038)

질의 교정 시스템은 네이버 검색 엔진에 입력된 검색어를 분석해 잘못 입력된 오타나 맞춤법 등을 자동 교정해주는 기능이다. 연사는 기계 번역 방식을 이용해 기존 방법보다 효율적인 교정 시스템을 만들었다고 한다.

### 질의 교정 유형과 방법

질의 교정 기능으로는 다음과 같은 것이 제공되고 있다.

* 스펠링 교정
* 한->영 / 영->한 변환
* 바른말 추천
* 축약어 추천

이건 맞춤법 검사기와는 다르다. 맞춤법 검사기는 한국어 문법을 우선시해 교정하는 것이지만, 질의어 교정 시스템은 검색 결과의 품질을 우선시한다. 사람들은 엄격한 맞춤법보다는 사회적으로 용인되는 표현을 더 많이 사용하며, 웹 문서 중에는 올바른 맞춤법으로 검색했을 때 오히려 검색 결과가 더 나쁜 경우도 존재하기 때문이다.

오탈자의 유형에는 다음과 같은 것이 있다.

* 단순 입력 실수 (70% 이상)
* 한->영 / 영->한 실수 (20% 이상)
* 맞춤법 실수 (9% 미만)
* 잘못된 지식 (1% 미만)

인간은 이런 오류를 교정하기 위해 형태적 특성(Signal), 앞뒤 문맥(Shallow Context), 지식과 개념(Deep Context)를 모두 활용한다. 컴퓨터가 이를 완전히 흉내낼 수 있는 알고리즘은 아직 존재하지 않는다.

이 중 단순 입력 실수와 맞춤법 실수 등은 Signa과 Shallow Context의 분석을 통해 상당히 해결할 수 있다. 하지만 잘못된 지식에 해당하는 교정은 Deep Context 모델링이 필요해 처리하기가 상당히 어렵다.

### 네이버 질의 교정 시스템의 개선

네이버의 기존 방식은 Noisy Channel 모델 기반이었는데, 단순한 방식이어서 학습 데이터를 많이 제공해도 정확도가 떨어졌다고 한다.

네이버는 번역 모델을 기반으로 질의 교정 시스템을 개선했다. 새로 도입한 방법은 통계학에 기반한 기계 번역 방법이다. 교정 시스템이 하는 일이 교정이 아니라 번역이라고 가정하고, 외국어를 한국어로 기계 번역하듯이 한국어를 한국어로 기계 번역하도록 한 것이다.

이 방법을 이용하면 새로운 질의가 입수될 때마다 자동 학습이 가능하며, 학습 데이터에 비례해 정확도도 높아지게 하기 위해 이 방법을 채택했다고 한다.

매일 대량의 데이터가 수집되고 엄청난 학습량을 처리해야 했는데, 오픈 소스 도구(GIZA++)는 느려서 사용할 수 없었고 교정 시스템을 직접 개발해야 했다고 한다.

새로 도입한 시스템은 성공적으로 개발됐고 품질이 검증됐다고 한다. 기존 시스템 대비 Recall이 2배~3배 향상됐고, 정확도 하락은 거의 없었으며, 속도 하락도 적었다고 한다. 학습량 증가에 따른 정확도 개선도 이뤄지고 있다. 현재 서비스를 실제 적용하고 있다고 한다.


