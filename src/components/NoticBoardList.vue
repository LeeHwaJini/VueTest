<template>
  <ul class="notic-board-list">
    <li v-for="(item, index) in items" :key="item">
      <div class="main-title-area" @click="toggleDropDown(index)">
        <span>{{ item.message }}</span>
        <i
          class="ico arrow-down"
          :class="{ active: targetIndex === index }"
        ></i>
      </div>
      <transition name="display">
        <div class="detail-area" v-show="targetIndex === index">
          {{ item.detail }}
        </div>
      </transition>
    </li>
  </ul>
</template>

<script>
// import { ref } from "vue";
export default {
  name: "NoticBoardList",
  data() {
    return {
      items: [
        {
          message: "Q&A 첫 번째 글 입니다.",
          detail: "상세내용1",
        },
        {
          message: "Q&A 두 번째 글 입니다.",
          detail: "상세내용2",
        },
      ],
      targetIndex: false,
    };
  },
  methods: {
    toggleDropDown(index) {
      console.log(this.targetIndex);
      if (this.targetIndex === index) {
        this.targetIndex = false;
      } else {
        this.targetIndex = index;
      }

      this.items[index].isVisible = !this.items[index].isVisible;
    },
  },
};
</script>

<style scoped>
.notic-board-list > li {
  border-bottom: 1px solid #eee;
}
.main-title-area > span {
  display: block;
  width: calc(100% - 24px);
}
.main-title-area {
  padding: 1rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

/* .display-enter-active,
.display-leave-active {
  transition: opacity 0.5s ease;
}

.display-enter-from,
.display-leave-to {
  opacity: 0;
} */

.detail-area {
  padding: 1rem;
  min-height: 150px;
  background: #f8f8f8;
}
.ico.arrow-down.active {
  transform: rotate(180deg);
}
</style>