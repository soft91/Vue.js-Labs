---
description: 'Vuetify Thrid Party Libaray를 사용하면서 발생한 HTML, CSS 이슈.'
---

# Vuetify HTML Tag overflow-y:scroll Issue

## 문제 발생

Vuetify Third Party Libaray를 사용하는 도중 정말 황당한 경험을 겪었다.

![&#xC774;&#xC720;&#xB97C; &#xC54C; &#xC218; &#xC5C6;&#xB294; &#xC2A4;&#xD06C;&#xB864;&#xC774; &#xC0DD;&#xACA8;&#xBC84;&#xB9AC;&#xB294; &#xD669;&#xB2F9;&#xD55C; &#xBB38;&#xC81C;;;](../.gitbook/assets/image%20%284%29.png)

전혀 원하지도 않는 페이지에 알 수 없는 스크롤이 생겨버려서 도저히 어느쪽에서 해결을 해야할 지 모르는 상황에 알고보니 HTML Style에 'overflow-y: scroll'이 적용되어 있었다.

![overflow-y: scroll;&#xC774; &#xC801;&#xC6A9;&#xB418;&#xC5B4; &#xC788;&#xC5C8;&#xC74C;.](../.gitbook/assets/image%20%285%29.png)

Stackoverflow에서 간신히 찾은 결과였고 이 문제를 해결하기 위해서는 직접 Main이 되는 HTML\(예: index.html\)에 HTML Style을 적용 시키는 방법 이였다.

## 해결 방법

**주의 해야 할 점은 'overflow-y: auto'로 변경해주는 방법 대신에 꼭 !important를 사용하여 강제적으로 적용을 시켜야만 한다.**

```text
html {
  overflow-y: auto !important;
}
```

이 문제는 예전 버전부터 발생한 이슈로 아직도 고쳐지지 않은 이슈라고 한다.😑😑😑😑

