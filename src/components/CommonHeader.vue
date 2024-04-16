<template>
  <header>
    <div class="header-wrap">
      <img src="../assets/softbridge_c.png" alt="softbridgeLogo" class="logo" />
      <nav class="header-menu">
        <ul>
          <li>메뉴1</li>
          <li>메뉴2</li>
          <li>메뉴3</li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "CommonHeader",
};
</script>

<style scoped>
header {
  border-bottom: 1px solid #eee;
  height: 60px;
  line-height: 60px;
  font-family: SUITE;
}
.header-wrap {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  gap: 5rem;
}
.logo {
  width: 120px;
  height: 20px;
}
.header-wrap .header-menu > ul {
  display: flex;
  align-items: center;
}
.header-wrap .header-menu > ul li {
  cursor: pointer;
}
.header-wrap .header-menu > ul li + li {
  margin-left: 4rem;
}
</style>