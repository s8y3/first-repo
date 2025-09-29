<template>
  <div class="start-screen">
    <!-- 背景アニメーション -->
    <div class="background"></div>

    <!-- 中央コンテンツ -->
    <div class="content">
      <h1 class="title">しりとりゲーム</h1>
      <button class="btn start">スタート</button>
      <button class="btn rules">ルール</button>
      <button class="btn settings">設定</button>

      <!-- 音関連のUI -->
      <div class="sound-controls">
        <button class="btn bgm">🎵 BGM ON/OFF</button>
        <button class="btn se">🔊 効果音 ON/OFF</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'StartScreen',
}
</script>

<style scoped>
.start-screen {
  position: relative;
  height: 100vh;
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #fff;
}

/* 背景アニメーション */
.background {
  position: absolute;
  width: 100%;
  height: 100%;
  background: linear-gradient(-45deg, #74ebd5, #acb6e5, #fbc2eb, #a6c0fe);
  background-size: 400% 400%;
  animation: gradientBG 15s ease infinite;
  z-index: -1;
}
@keyframes gradientBG {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}

/* 中央 */
.content {
  text-align: center;
  width: 90%;
  max-width: 500px;
}
.title {
  font-size: 2.5rem;
  margin-bottom: 2rem;
  text-shadow: 2px 2px 6px rgba(0, 0, 0, 0.6);
}

/* ボタン */
.btn {
  display: block;
  width: 100%;
  margin: 0.8rem auto;
  padding: 1rem;
  font-size: 1.4rem;
  border: none;
  border-radius: 15px;
  cursor: pointer;
  transition:
    transform 0.2s,
    background 0.3s;
}
.btn.start {
  background: #ffeb3b;
  color: #333;
}
.btn.rules {
  background: #4caf50;
  color: #fff;
}
.btn.settings {
  background: #2196f3;
  color: #fff;
}
.btn.bgm {
  background: #9c27b0;
  color: #fff;
}
.btn.se {
  background: #ff5722;
  color: #fff;
}

.btn:hover {
  transform: scale(1.05);
  opacity: 0.9;
}

/* 音のUIまとめ */
.sound-controls {
  display: flex;
  gap: 1rem;
  margin-top: 1rem;
}
</style>
