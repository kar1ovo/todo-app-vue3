<template>
  <main>
    <div class="container">
      <div class="title">
        <span class="title2">欢迎使用</span>
        <span class="title1">KAR1OVO</span>
        <span class="title2">待办事项</span>
      </div>
      <div class="input-add">
        <input type="text" name="todo" />
        <button>
          <i class="plus"></i>
        </button>
      </div>
      <div class="filters">
        <span class="filter active">全部</span>
        <span class="filter">已完成</span>
        <span class="filter">未完成</span>
      </div>
      <div class="todo-list">
        <div class="todo-item">
          <label>
            <input type="checkbox" />
            Todo1
            <span class="check-button"></span>
          </label>
        </div>
        <div class="todo-item done">
          <label>
            <input type="checkbox" />
            Todo2
            <span class="check-button"></span>
          </label>
        </div>
        <div class="todo-item">
          <label>
            <input type="checkbox" />
            Todo3
            <span class="check-button"></span>
          </label>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: "App",
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  /* font-family: Helvetica, "PingFang SC", "Miscrosoft Yahei", sans-serif; */
}

main {
  width: 100vw;
  min-height: 100vh;
  display: grid;
  align-items: center;
  justify-items: center;
  background: rgb(203, 210, 240);
}

.container {
  width: 60%;
  max-width: 400px;
  box-shadow: 0 0 24px rgba(0, 0, 0, 0.15);
  border-radius: 24px;
  padding: 48px 28px;
  background: rgb(245, 246, 252);
}

/* h1 {
  margin: 24px 0;
  font-size: 26px;
  color: #414873;
}

h2 {
} */
.title {
  margin: 24px 0;
  color: #414873;
  font-weight: bold;
}

.title1 {
  font-size: 44px;
}
.title2 {
  font-size: 20px;
}

.input-add {
  position: relative;
  display: flex;
  align-items: center;
  /* border: #414873 solid 1px; */
}

.input-add input {
  padding: 16px 52px 16px 18px;
  border-radius: 48px;
  outline: none;
  border: none;
  box-shadow: 0 0 24px rgba(0, 0, 0, 0.08);
  width: 100%;
  font-size: 16px;
  color: #626262;
}

.input-add button {
  width: 46px;
  height: 46px;
  border-radius: 50%;
  background: linear-gradient(#c0a5f3, #7f85f7);
  border: none;
  color: white;
  position: absolute;
  right: 0px;
  cursor: pointer;
  outline: none;
}

.input-add .plus {
  display: block;
  width: 100%;
  height: 100%;
  background: linear-gradient(#fff, #fff), linear-gradient(#fff, #fff);
  background-size: 50% 2px, 2px 50%;
  background-position: center;
  background-repeat: no-repeat;
}

.filters {
  display: flex;
  margin: 24px 2px;
  color: #c0c2ce;
  font-size: 14px;
  cursor: pointer;
}
.filters .filter {
  margin-right: 14px;
  transition: 0.8s;
}
.filters .filter.active {
  color: #6b729c;
  transform: scale(1.2);
}

.todo-list {
  display: grid;
  row-gap: 14px;
}

.todo-item {
  background: white;
  padding: 16px;
  border-radius: 8px;
  color: #626262;
}
.todo-item label {
  position: relative;
  display: flex;
  align-items: center;
  cursor: pointer;
}
.todo-item.done label {
  text-decoration: line-through;
  font-style: italic;
}
.todo-item label span.check-button {
  position: absolute;
  top: 0;
}
.todo-item label span.check-button::before,
.todo-item label span.check-button::after {
  content: "";
  display: block;
  position: absolute;
  width: 18px;
  height: 18px;
  border-radius: 50%;
}
.todo-item label span.check-button::before {
  border: 1px solid #b382f9;
}
.todo-item label span.check-button::after {
  transition: 0.4s;
  background: #b382f9;
  transform: translate(1px, 1px) scale(0.8);
  opacity: 0;
}
.todo-item input {
  margin-right: 16px;
  opacity: 0;
}
.todo-item input:checked + span.check-button::after {
  opacity: 1;
}
</style>
