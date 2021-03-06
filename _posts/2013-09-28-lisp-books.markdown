---
layout: post
title: "리스프 입문자를 위한 학습서"
author: 박연오(bakyeono@gmail.com)
date: 2013-09-28 18:46 +0900
tags: 함수형-프로그래밍 커먼-리스프 클로저 스킴 서평
---
* table of contents
{:toc}

리스프에 관심을 갖는 사람들은 이미 다른 프로그래밍 언어를 접해 본 사람이 대부분일 것이다. 기초적인 프로그래밍 지식이 있는 사람은 새로운 프로그래밍 언어를 공부할 때 처음만큼 많은 노력이 들지는 않는다.

하지만 함수형 프로그래밍 패러다임은 주류 프로그래밍 방법과 많이 달라서 그냥 언어 정의 문서 한 번 훑어보고 바로 사용할 수 있지는 못하다.

리스프에는 흔한 for-loop조차 없다. 함수형 프로그래밍을 처음 공부한다면 서둘지 말고 차근차근 익히는 게 좋은 것 같다.

프로그래밍 공부를 할 때 각종 온라인 문서만으로는 정리가 잘 안 되어 있고 정보들을 검색하는 데 시간이 많이 걸려 불편하다. 프로그래밍 입문자이든, 리스프 입문자이든 좋은 교재를 곁에 두고 공부하는 것이 좋다. 리스프를 다룬 책은 국내에 거의 없었는데, 근래에 번역서가 몇 권 출판되었다. 그 책들을 비롯해서 내가 도움을 받은 책들을 소개해 본다.

리스프 계열의 언어는 매우 다양한 종류가 있는데 그 중 가장 많이 쓰이는 스킴(Scheme), 커먼 리스프(Common Lisp), 클로저(Clojure)에 관련된 책만 다뤘다.

## 스킴을 다룬 책들

![컴퓨터 프로그램의 구조와 해석(SICP)][img-book-sicp]

### [컴퓨터 프로그램의 구조와 해석(SICP)][컴퓨터 프로그램의 구조와 해석(SICP)]

SICP는 컴퓨터 프로그래밍 도서의 고전이며 아마 리스프 관련 책 중에 가장 이름 난 책일 것이다.

이 책은 리스프의 한 종류인 스킴의 문법을 간단히 알려주고, 실습에도 이 언어를 이용한다. 스킴 언어에 관해 설명하긴 하지만 스킴이나 리스프 자체보다는 함수형 프로그래밍의 일반적인 방법과 전산학의 주요 과제들을 다루고 있다.

이 책은 함수형 프로그래밍을 기초부터 가르치기는 하지만 내용을 다루는 방식이 깊이 우선 탐색 방식이어서 조금 읽다보면 곧 만만치 않은 내용들이 등장한다. 그리고 모든 것을 친절히 설명하기보다는 독자가 연습문제를 통해 스스로 탐구하고 깨닫게 하고 있다. 그래서 이론적으로는 입문자도 열심히 학습하면 익힐 수 있겠지만 중간에 포기할 가능성이 높은 책이다. 마치 초등학생이 수학의 정석으로 수학 공부하는 느낌이랄까. 천재가 아닌 이상 입문서로 사용하기에는 비효율적일 듯하다.

리스프 학습의 목적이 무엇이냐에 따라서도 이 책에 대한 호불호가 갈릴 수 있다. 리스프 계열 언어들은 언어 자체의 문법은 매우 간단하지만 각종 자료구조(주로, 리스트)를 다루는 함수들을 아주 다양하게 지원하기 때문에 이것들을 익히고 활용하는 데 어느 정도 시간을 들여야 한다. 그런데 SICP는 이와 같은 실용 함수들을 알려주는 책이 아니다. 그보다는 독자가 그런 함수와 알고리즘들을 필요에 따라 직접 만들어내고 골치아픈 문제를 해결할 수 있게끔 내공을 길러주려 한다. 그래서 장기적으로는 리스프 활용에 큰 도움을 주겠지만, 당장 리스프를 빠르게 익혀서 실생활에 써보려는 사람에게는 별로 맞지 않다.

이 책이 다루는 내용의 수준 높음과는 별개로 책의 학습을 곤란하게 하는 요소도 있다. 책을 읽다보면 이 책이 적어도 고등학교 이과 학생 정도 수준의 수학 지식을 전제하고 있다는 것을 알게 된다. (MIT 1학년 학생을 대상으로 쓴 책이니 그럴 만하다.) 나처럼 그런 수준에 못 미치는 사람들은 수학 용어와 개념들을 수학 참고서나 위키백과를 뒤져가며 학습해야 하기 때문에 좀 더 어렵게 느껴진다. 또, 몇몇 주요 용어들에 대한 다소 과하게 느껴지는 순우리말 번역으로 인해 이미 프로그래밍 지식이 있는 사람들에게 불편을 주기도 한다.

여러가지로 따져 봤을 때, 리스프 언어나 함수형 프로그래밍을 처음 공부하는 사람이라면 다른 책을 보는 것이 더 좋을 것 같다.

하지만 리스프 사용자들에게 이 책이 주는 매력은 매우 커서, 리스프를 사용하다 보면 결국 언젠가는 이 책을 학습하게 될 것이다. 리스프에는 관심 없지만 이 책만을 익히는 프로그래머들도 있다. 나도 전에 한 번 학습을 포기했다가, 얼마전부터 다시 틈틈이 학습하고 있다. 리스프에 관해 전혀 모를 때 학습했던 것보다는 리스프를 어느 정도 써본 후에 학습하니 역시 좀더 쉽게 느껴지긴 한다.

이 책의 원서는 [공식 사이트][sicp]에 전문 공개(CCL 3.0)되어 있다.

![프로그램 디자인, 어떻게 할 것인가][img-book-how-to-design-programs]

### [프로그램 디자인, 어떻게 할 것인가][프로그램 디자인, 어떻게 할 것인가]

SICP가 너무 어려워서 좀 더 쉽게 가르치고자 나온 책이라고 알려져 있다. 프로그래밍 입문서를 표방하는 책이다. 스킴의 한 변종으로 저자가 만든 래킷(Racket)이라는 언어를 이용해 가르친다.

SICP와는 달리 기초부터 천천히 차근차근 진행해 나가고, 그때그때 적절한 난이도의 과제를 제시하며, 초반부부터 GUI 환경을 이용하여 입문자가 어려워하거나 흥미를 잃지 않도록 배려해 구성했다. 그래서 차근차근 꾸준히 학습한다면 함수형 프로그래밍 방법과 문제 해결 방법을 잘 배울 수 있을 것 같다.

다만 나는 분량이 너무 많아서(850페이지인데 연습문제가 많아서 시간이 꽤 걸린다.) 끝까지 학습하지는 못했다. 시간 여유가 있을 떄 한번쯤 다시 학습해보고 싶은 책이다. (특히, SICP를 공부하고 있으면 점점 더 이 책을 공부하고 싶어진다.)

프로그래밍을 처음 배우거나, 시간이 많아서 함수형 프로그래밍을 차근차근 공부하고 싶거나, SICP를 익히고 싶은데 너무 어려워서 뭔가 선행 학습을 하고 싶다면 이 책을 강추!

이 책의 원서도 [공식 사이트][htdp]에 전문 공개되어 있다.

## 커먼 리스프를 다룬 책들

![만들면서 배우는 리스프 프로그래밍: Land of Lisp][img-book-land-of-lisp]

### [만들면서 배우는 리스프 프로그래밍: Land of Lisp][만들면서 배우는 리스프 프로그래밍: Land of Lisp]

내가 알기론 커먼 리스프를 다룬 유일한 국내 번역서다.

이 책은 입문서를 표방하고 있지만 '진짜' 입문서로 보기에는 약간 무리가 있다. 기초 문법에 대한 설명이 간결한 편이어서 입문자에 대한 배려가 부족하고, 책에서 다루는 예제들도 그래프 자료구조, repl 구현, http 서버 구현, 인공지능 프로그래밍 등으로 되어 있어 제법 난이도가 있는 편이기 때문이다.

한편, 모든 예제들이 게임 제작과 관련된 내용이어서 흥미롭고 중간 중간 등장하는 작가의 만화도 재미있다는 장점이 있다. 커먼 리스프를 다룬 유일한 번역서이므로 한 권쯤 구입해서 읽어보는 것도 나쁘지 않다. 다만 이 책으로만 커먼 리스프를 공부하려 하면 조금 어려울 것이다.

참, 이 [책(원서)의 공식 사이트][landoflisp.com]에서 저자의 혼이 담긴 뮤직비디오와 재미나고 흥미로운 만화도 있으니 꼭 보자!

![ANSI Common Lisp][img-book-ansi-common-lisp]

### [ANSI Common Lisp][ANSI Common Lisp]

만일 영문서를 읽는게 부담이 되지 않는다면 대학 도서관에서 커먼 리스프 관련 도서를 이용할 수 있다. 대학 도서관에는 커먼 리스프 관련 도서가 많이 구비돼 있는 편인데, 커먼 리스프가 발표된지 꽤 시간이 지났고 대학 인공지능 연구소에서 많이 이용하는 언어이기 때문인 것 같다.

나는 그 중 폴 그레이엄의 《ANSI Common Lisp》를 추천한다. 내가 이 책을 리스프 입문서로써 학습했는데 친절하고 짜임새있고 연습문제들도 점증적인 난이도로 구성돼 있어서 수월하게 배울 수 있었다. 이 책의 저자는 '야후! 쇼핑'을 개발한 유명한 리스프 해커이자 리스프 옹호자인데, 함수형 프로그래밍 방법론을 옹호할 때 아주 설득력있게 논지를 전개하기 때문에 프로그래밍에 대해 새롭게 생각해보는 기회도 제공한다.

다만 이 책도 독자가 c 언어 등의 기존 프로그래밍 지식이 있다고 가정하고 쓰여졌기 때문에 프로그래밍을 정말 처음 공부하는 사람이라면 커먼 리스프 책은 아니지만 앞서 소개한 《프로그램 디자인, 어떻게 할 것인가》를 학습하는 것이 더 좋을 것이다.

저자의 책 가운데 주로 매크로 고급 활용법을 다룬 《On Lisp》라는 책도 있는데 저자의 사이트에 무료로 공개되어 있으니 관심 있으면 참고하자. 《On Lisp》는 커먼 리스프 중~상급자용이다.

![Practical Common Lisp][img-book-practical-common-lisp]

### [Practical Common Lisp][Practical Common Lisp]

이 책도 영문서로, 국내에 번역본이 출판되지는 않았다.《ANSI Common Lisp》가 언어에 대한 내용만을 다뤘다면 이 책은 커먼 리스프를 실제 환경에서(주로 웹 환경) 활용하는 방법을 많이 다루고 있다. 커먼 리스프 입문서로 이용해도 좋고, 커먼 리스프 문법을 익힌 후 중급용으로도 도움이 된다.

맥용 커먼 리스프 인터프리터인 [Clozure Common Lisp(CCL)][clozure-common-lisp](매우 강추함)를 개발한 회사에서 "우리 회사에 입사하고 싶으면 이 책부터 보고 와라!"라며 추천하는 책이기도 하다.

이 책은 [저자의 웹사이트][Practical Common Lisp]에 전문 공개되어 있다.

## 클로저를 다룬 책들

![프로그래밍 클로저][img-book-programming-clojure]

### [프로그래밍 클로저][프로그래밍 클로저]

몇 해 전 발표되어 많은 주목을 받고 있는 [클로저][clojure.org]를 다룬 국내 유일의 번역서다. 이 책은 기초 프로그래밍 지식이 있는 독자를 대상으로 클로저의 특징을 빠르게 파악할 수 있도록 구성되어 있다. 특히 자바 프로그래밍의 기초가 있는 사람이 읽을 경우 2~3일 정도면 클로저를 당장 활용할 수 있을 정도로 익힐 수 있다.

다만 분량이 적다보니 리스프 입문자가 함수형 프로그래밍 방법을 충분히 이해하고 적용하기는 어려울 수 있다. 그리고 비교적 일찍 나온 책이라서 클로저 초기 버전(1.1)을 기준으로 했는데, 그래서 지금은 안 쓰이는 자료구조에 대한 설명도 있고 대체된 내용에 대한 설명은 없다는 단점이 있다. 그러나 클로저를 처음 익히는 사람에게는 큰 문제는 아닐 것이다.

번역서로 클로저를 공부하고자 한다면 이 책밖에 없고, 책 내용도 괜찮다.

![Clojure Programming - Practical Lisp for the Java World][img-book-clojure-programming]

### [Clojure Programming - Practical Lisp for the Java World][Clojure Programming - Practical Lisp for the Java World]

영문서를 읽는 데 부담이 많지 않다면 클로저를 익히는데 가장 좋은 책이라고 생각한다. 2012년에 나온 책으로 클로저 최신 버전을 다루고 있으며 클로저의 특징들을 체계적이고 꼼꼼하게 설명하고 있다. 한 예로 클로저의 각종 자료구조를 설명할 때는 개념적 자료구조와 실제 구현을 구분해서 설명하며, 각 자료구조에 대응하는 함수들도 충분히 설명한다. 또 클로저를 실용적으로 활용하는 방안에 대해서도 여러 모로 설명하고 있다. 다만 등장하는 예제나 개념들이 난이도가 있는 편이어서 프로그래밍 지식이 전혀 없는 사람이 읽기는 쉽지 않을 것이다.

## 리스프 고르기

어떤 리스프가 좋을까? 나는 클로저를 추천한다. 왜냐하면 ...

- 단일 코어에서의 성능은 네이티브 코드를 생성하는 커먼 리스프가 클로저보다 뛰어나지만, 클로저는 병렬처리에 특화되어 멀티코어 환경에서 유리하다. 그리고 병렬처리는 앞으로 점점 더 중요해질 것이다.

- 클로저는 자바 가상머신에서 동작하기 때문에 자바의 풍부한 라이브러리를 사용할 수 있어 신생 언어임에도 커먼 리스프보다 라이브러리 가용성이 높다.

- 모든 데이터를 상수로 취급하는 클로저가 상수와 변수를 분리해 다루는 커먼 리스프에 비해 함수형 언어로서의 특성이 더 강하다.

- 스킴이 커먼 리스프보다 코드가 깔끔한 편이라고 하는데 클로저도 코드가 상당히 깔끔하다. (다만 리더 매크로들을 남발하면 좀 지저분해진다.)

> SICP를 스킴이 아니라 클로저로 학습하려고 시도하는 사람들이 있다. [SICP in Clojure 사이트][sicp-in-clojure]에서 이를 지원한다. 아쉽게도 아직 사이트가 완성되지는 않았다.

여러 모로 클로저를 선택하는 게 유리하지만 클로저는 고급 활용을 위해서는 어느 정도의 자바 지식을 요구한다는 점 때문에 리스프 입문자가 아닌 순수 프로그래밍 입문자에게는 맞지 않을 수도 있다.

당장 활용할 수 있는 것을 배우고 싶다면 '프로그래밍 클로저'를 통해 클로저를 익히길 권한다. 반면에 기초부터 꼼꼼히 익히고 싶고 시간과 인내심이 있는 사람이라면 '프로그램 디자인, 어떻게 할 것인가'를 학습하는 것도 좋다. 하지만 이 책을 학습한 후 교육용 스킴인 '래킷'으로 뭔가를 하려고 하기보다는 함수형 프로그래밍 방법을 배우는 용도로만 사용하고 즉시 클로저로 갈아탈 것을 권한다.

[컴퓨터 프로그램의 구조와 해석(SICP)]: http://www.insightbook.co.kr/books/ppp/%EC%BB%B4%ED%93%A8%ED%84%B0-%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%A8%EC%9D%98-%EA%B5%AC%EC%A1%B0%EC%99%80-%ED%95%B4%EC%84%9D
[프로그램 디자인, 어떻게 할 것인가]: http://www.insightbook.co.kr/books/individual/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%A8-%EB%94%94%EC%9E%90%EC%9D%B8-%EC%96%B4%EB%96%BB%EA%B2%8C-%ED%95%A0-%EA%B2%83%EC%9D%B8%EA%B0%80
[만들면서 배우는 리스프 프로그래밍: Land of Lisp]: http://www.hanb.co.kr/book/look.html?isbn=978-89-7914-875-6
[Land of Lisp video]: http://www.youtube.com/watch?v=HM1Zb3xmvMc
[ANSI Common Lisp]: http://www.paulgraham.com/acl.html
[Practical Common Lisp]: http://www.gigamonkeys.com/book
[프로그래밍 클로저]: http://www.insightbook.co.kr/books/programming-insight/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D-%ED%81%B4%EB%A1%9C%EC%A0%80lisp
[Clojure Programming - Practical Lisp for the Java World]: http://www.clojurebook.com
[clojure.org]: http://clojure.org
[landoflisp.com]: http://landoflisp.com
[sicp]: http://mitpress.mit.edu/sicp
[htdp]: http://www.htdp.org
[sicp-in-clojure]: http://sicpinclojure.com
[clozure-common-lisp]: http://www.clozure.com

[img-book-ansi-common-lisp]: {{ site.url }}/img/book-ansi-common-lisp.png
[img-book-clojure-programming]: {{ site.url }}/img/book-clojure-programming.png
[img-book-how-to-design-programs]: {{ site.url }}/img/book-how-to-design-programs.png
[img-book-land-of-lisp]: {{ site.url }}/img/book-land-of-lisp.png
[img-book-practical-common-lisp]: {{ site.url }}/img/book-practical-common-lisp.png
[img-book-programming-clojure]: {{ site.url }}/img/book-programming-clojure.png
[img-book-sicp]: {{ site.url }}/img/book-sicp.png

