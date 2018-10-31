# javascript
## TIPS
- scrollTop의 최대값은 scrollHeight가 아니라 (scrollHeight - clientHeight)
- scrollTop은 브라우저에 따라 다르게 동작 될 수 있음 window.pageYOffset이 동일하게 동작 된다고 함. viewport 적용시 window.scrollY 사용가능
  - Window sizes and scrolling(https://javascript.info/size-and-scroll-window)
  - window.scrollY(https://developer.mozilla.org/ko/docs/Web/API/Window/scrollY)
- Chrome Devtolls를 이용한 web memory 분석법(http://sculove.github.io/blog/2016/10/06/memory/)
  - Shallow Size는 작지만, Retained Size가 굉장히 많다면? Memory leak을 의심하라
```
Shallow Size
array, string와 같이 직접적으로 메모리를 점유하고 있는 JavaScript 객체들의 크기 실제 데이터가 있는 영역

Retained Size
GC이후 남겨진 메모리의 크기. 즉, 실제 사용중인 JS Heap의 크기  
```
  - Timeline(현재 Performance panel) JS Heap이 계단형, Nodes가 계단형 JS Heap이 Memory Leak, Nodes가 Memory Leak
