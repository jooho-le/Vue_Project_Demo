# vue-demo

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

## 변경 요약 (Vue2 → Vue3 스타일 리팩터링)

- 핵심 변경점
  - Options API → Composition API + `<script setup>`로 전환
  - `data/computed/methods` → `ref/reactive/computed`와 함수로 치환
  - 라이프사이클(`mounted` 등) → `onMounted` 등 Composition 훅 사용
  - `props`/`emit` → `defineProps`/`defineEmits`로 명시(타입은 TS로 간단 표기)
  - `provide/inject` → `setup` 안에서 `provide()`/`inject()`로 사용

- 수정한 파일 목록
  - `src/components/example1/E-01-instance.vue`
  - `src/components/example1/E-02-reactive.vue`
  - `src/components/example1/E-03-binding.vue`
  - `src/components/example2/E-04-directives.vue`
  - `src/components/example3/ParentComponent.vue`, `src/components/example3/ChildComponent.vue`
  - `src/components/example4/ParentComponent.vue`, `src/components/example4/ChildComponent1.vue`, `src/components/example4/ChildComponent2.vue`
  - `src/components/example5/E-07-Options-API.vue`
  - `src/App.vue`

- 실행 방법(동작 확인)
  1) `npm install`
  2) `npm run serve` → `http://localhost:8080`

## 동작 스크린샷
`docs/vue.png`

