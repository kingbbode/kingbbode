# **GDG WebTech Web**
## **측정하는 놈, 그리는 놈,   로딩하는 놈**
>2016년 8월 17일
---

## 랜더링 퍼포먼스

### GPU가 잘하는 것
 - 텍스텨 이미지 출력
 - 이미 가진 텍스쳐 재활용
 - 회전, 확대, 축소, 기울임, 반투명 처리
 - 위 기능 동시 처리

### GPU가 못하는 것
 - 비디오 메모리로의 데이터 전송 느림
 - GPU의 데이터는 CPU에서 생성 후 전송

**데이터 전송 최소화 필요**

### 이슈
 - Reflow & Repaint 발생 요인
    * DOM 노드의 동적인 crud
    * DOM 노드의 감춤/표시
    * DOM 노드의 이동, 애니메이션
    * 스타일시트의 추가 혹은 스타일 속성의 변경
    * 브라우저 사이즈 변경
    * 폰트 변경
    * 스크롤

---

## 로딩 퍼포먼스

#### JavaScript
 - defer : exec는 돔 그린 후에
 - async : load 후에 돔 정지하고 exec 후 돔 시작

#### Defer iFrames
 - data-src="" 활용

## 유용한 기능

#### Adding User-timing
window.performance.mark()
window.performnce.measure()

#### Chrome Dev Tool
- TimeLine, Profiles -> 자바스크립트API로 실행 가능.

#### performance Timing
- window.performance
