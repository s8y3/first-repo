<!-- src/components/MyComponent.vue -->
<template>
  <div>
    <p>これは追加したコンポーネントです。</p>
  </div>
</template>

<script lang="ts">
// Vue 3のComposition APIを使用する場合、script setup内でインポートすれば、特別な登録なしにテンプレートで利用できます。
</script>
<!-- src/App.vue -->
<template>
  <div>
    <h1>メインアプリです</h1>
    <!-- 作成したコンポーネントをタグとして使用 -->
    <MyComponent />
  </div>
</template>

<script lang="ts">
// コンポーネントをインポート
import MyComponent from './components/MyComponent.vue'
</script>
