<script setup lang="ts">
import XIcon from '@/assets/icons/XIcon.vue'
import banner_back from '@/assets/imgs/banner-back.png'
import { ref } from 'vue'
import { useWindowScroll } from '@vueuse/core'

const { y } = useWindowScroll()

const isVisible = ref(true)
</script>
<template>
  <div :class="y > 108 ? 'banner' : 'banner hide-banner'" v-if="isVisible">
    <div class="banner-img">
      <img :src="banner_back" alt="" />
    </div>
    <div class="banner-content">
      <h4>Black Friday</h4>
      <h5>10% OFF</h5>
      <p>Use code <span>10FRIDAY</span> at checkout</p>
      <div class="banner-btn">
        <button class="btn-secondary">Shop now through Monday</button>
      </div>
    </div>
    <div class="banner-action">
      <button class="btn-ghost" @click="isVisible = false">
        <XIcon />
      </button>
    </div>
  </div>
</template>
<style scoped>
.banner {
  position: fixed;
  right: 36px;
  bottom: 36px;

  width: 600px;
  height: 349px;

  transition: all 0.4s;

  display: flex;

  border-radius: 16px;
  background-color: #0e0e0d;
  box-shadow: 0px 4px 34px 0px rgba(0, 0, 0, 0.45);
}

.hide-banner {
  transform: translateY(calc(100% + 72px));
}

.banner-img {
  width: 280px;
  display: flex;
  align-items: center;
  justify-content: center;

  margin-left: 20px;

  img {
    width: 100%;
  }
}

.banner-content {
  color: #fff;

  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

  height: 100%;
}

h4 {
  text-align: center;
  font-size: 46px;
  font-style: normal;
  font-weight: 500;
  line-height: 110%;
  letter-spacing: -1.84px;

  margin-bottom: 25px;
}

h5 {
  background: linear-gradient(to right, #7d5317, #eddf95);
  background: -webkit-linear-gradient(to right, #7d5317, #eddf95);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;

  text-align: center;
  font-size: 40px;
  font-style: normal;
  font-weight: 500;
  line-height: 110%;
  letter-spacing: -1.6px;

  margin-bottom: 14px;
}

p {
  color: #6c6c70;
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: 130%;
  letter-spacing: 0.08px;

  margin-bottom: 40px;
}

.banner-action {
  position: absolute;

  right: 16px;
  top: 16px;
}
</style>
