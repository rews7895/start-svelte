<script>
  let name = 'world';
  let src = 'https://logos-world.net/wp-content/uploads/2020/05/Nirvana-Logo.png';
  let alt = 'nirvana logo';

  let string = `this string contains some <strong>HTML!!!</strong>`;

  let href = 'https://sveltesociety.dev/tools/#editor-support';
</script>

<div>
  <h1>01. Svelte란?</h1>
  <div>
    <p>Svelte는 빠른 웹 애플리케이션을 구축하기 위한 도구입니다.</p>
    <p>Svelte는 런타임 에 애플리케이션 코드를 해석하지 않고 빌드 시 앱을 이상적인 JavaScript로 변환합니다 .</p>
    <p>.svelte란 파일에 작성해야 한다.</p>
  </div>

  <h1>02. 기초</h1>
  <div>
    <p>중괄호 안에 원하는 Javascript 변수를 넣을 수 있다.</p>
    <p>또한 함수도 적용가능</p>
    <p>Hello {name}!</p>
    <p>Hello {name.toLocaleUpperCase()}!</p>
  </div>

  <h1>03. 동적 속성</h1>
  <div>
    <p>중괄호를 사용하여 요소 속성을 제어할 수 있다.</p>
    <p>또한 이름과 값이 동일할 경우 약칭으로 사용하는 것을 허용한다.</p>
    <img src={src} alt={alt}>
    <img {src} {alt}>
  </div>

  <h1>04. 스타일링</h1>
  <div>
    <p>HTML과 마찬가지로 style을 추가할 수 있다.</p>
    <p>또한 style은 해당 파일 내에서만 변경되며, 다른 곳에서는 스타일을 변경하지 않는다.</p>
    <p class="comic-line">This is a paragraph.</p>
  </div>

  <h1>05. 구성요소</h1>
  <div>
    <p>파일(구성 요소)을 앱으로 가져와서 사용할 수 있다.</p>
    <p>구성요소의 첫 글자는 대문자를 사용한다.(일반적인 HTML 태그와 구분하기 위해)</p>
    <p>ex) import Nested from './Nested.svelte'</p>
  </div>

  <h1>06. 문자열 HTML 처리</h1>
  <div>
    <p>HTML을 구성 요소에 직접 렌더링 해야할 때도 있다.</p>
    <p>이 기능을 사용하는 경우 신뢰할 수 없는 소스에서 가져온 HTML을 수동으로 이스케이프 처리하는 것이 중요!</p>
    <p>XSS 공격에 노출될 위험이 있다.</p>
    <p>{@html string}</p>
  </div>

  <h1>07. 확장 플러그인</h1>
  <div>
    <a {href}>확장 플러그인</a>
  </div>
</div>

<style>
  img {width: 150px;}
  .comic-line { color: purple; font-family: 'Comic Sans MS', cursive; font-size: 2em;}
</style>
