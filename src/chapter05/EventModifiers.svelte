<script>
	function handleClick() {
		alert('clicked')
	}
</script>

<div>
  <h1>05-3. Event Modifiers</h1>
  <p>Dom 이벤트 핸들러는 동작을 변경하는 수정자를 가질 수 있다.</p>
  <p><b>preventDefault</b>: event.preventDefault()— 핸들러를 실행하기 전에 호출 합니다. 예를 들어 클라이언트 측 양식 처리에 유용</p>
  <p><b>stopPropagation</b>: event.stopPropagation(), 이벤트가 다음 요소에 도달하는 것을 방지</p>
  <p><b>passive</b>: 터치/휠 이벤트에 대한 스크롤 성능 향상(Svelte는 안전한 위치에 자동으로 추가)</p>
  <p><b>nonpassive</b>: 명시적으로 설정 passive: false</p>
  <p><b>capture</b>: 버블링 단계 대신 캡처 단계 에서 핸들러를 시작합니다</p>
  <p><b>once</b>: 핸들러가 처음 실행된 후 제거</p>
  <p><b>self</b>: event.target이 요소 자체인 경우에만 트리거 핸들러</p>
  <p><b>trusted</b>: trusted인 경우에만 트리거, event.isTrusted = true. 즉, 이벤트가 사용자 작업에 의해 트리거된 경우</p>
  <p>on:click|once|capture 와 같이 연결하여 사용</p>
  <button on:click|once={handleClick}>
    Click me
  </button>
</div>