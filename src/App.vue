<template>
  <div class="container">
    <div class="header">
      <h1>AI体验馆</h1>
    </div>
    <div class="btn-group">
      <button class="btn gpt" @click="showGPT">GPT助手</button>
      <button class="btn ai" @click="showAI">AI绘画</button>
    </div>
    <div class="footnote">版权所有 &copy; 2021 AI体验馆</div>
  </div>
</template>

<script>

import router from "@/router/index.js";
export default {
  methods: {
    showGPT() {
     router.push("/chat");
    },
    showAI() {
      // TODO: AI绘画按钮被点击后的逻辑
    }
  }
}
</script>

<style>
.container {
  width: 100%;
  height: 100%;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: #101522;
  background-image: url('https://cdn.pixabay.com/photo/2015/05/15/14/38/computer-767983_960_720.jpg');
  background-size: cover;
}

.header {
  font-size: 4vw;
  font-weight: bold;
  margin-bottom: 5%;
  color: #fff;
  text-shadow: 0 0 10px #2196f3;
}

.footnote {
  position: absolute;
  bottom: 2%;
  color: #ccc;
}

.btn-group {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.btn {
  display: inline-block;
  padding: 3vw 5vw;
  margin: 2vw;
  border-radius: 2.5vw;
  font-size: 4vw;
  font-weight: bold;
  color: #fff;
  text-decoration: none;
  background-color: #2196f3;
  box-shadow: 0 2vw 2vw rgba(0, 0, 0, 0.2);
  cursor: pointer;
  transition: all 0.3s ease-in-out;
}

.btn:hover {
  transform: scale(1.1);
  background-color: #1976d2;
}

.gpt {
  background-color: #f44336;
  box-shadow: 0 2vw 2vw rgba(0, 0, 0, 0.2);
}

.gpt:hover {
  background-color: #c62828;
}

.ai {
  background-color: #4caf50;
  box-shadow: 0 2vw 2vw rgba(0, 0, 0, 0.2);
}

.ai:hover {
  background-color: #388e3c;
}

@media screen and (min-width: 768px) {
  .header {
    font-size: 4em;
  }

  .btn {
    padding: 20px 40px;
    margin-right: 20px;
    border-radius: 50px;
    font-size: 24px;
  }
}
</style>
