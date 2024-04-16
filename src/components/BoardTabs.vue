<template>
  <ul class="tab">
    <li class="active">공지사항</li>
    <li>문의사항</li>
    <li>자유게시판</li>
  </ul>
</template>

<script>
export default {
  name: "BoardTabs",
};
</script>

<style scoped>
.tab {
  margin-top: 3rem;
  display: flex;
  align-items: center;
}
.tab li {
  padding: 1rem;
  width: calc(100% / 3);
  text-align: center;
  background: #fff;
  border: 1px solid #eee;
}
.tab li + li {
  border-left: none;
  cursor: pointer;
}
.tab li.active {
  background: #08182f;
  color: #fff;
  font-weight: bold;
}
</style>
