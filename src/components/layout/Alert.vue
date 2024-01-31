<script setup lang="ts">
import DotIcon from '@/assets/icons/DotIcon.vue'
import XIcon from '@/assets/icons/XIcon.vue'
import alert_back from '@/assets/imgs/alert-back.png'
</script>
<template>
  <nav>
    <div class="wrapper">
      <!-- IMAGE CONTAINER -->
      <div class="alert-image">
        <img :src="alert_back" alt="" />
      </div>
      <div class="alert-header">
        <h3><b>Black Friday</b>, 24-27 Nov</h3>
        <DotIcon class="alert-icon" />
        <span>10FRIDAY</span>
        <DotIcon class="alert-icon" />
        <h3>Use code <span>10FRIDAY</span> at checkout</h3>
      </div>
      <div class="alert-actions">
        <button class="btn-primary">Shop now</button>
        <button class="btn-ghost">
          <XIcon />
        </button>
      </div>
    </div>
    <div class="alert-shape">
      <div class="alert-bg"></div>
    </div>
  </nav>
</template>
<style scoped>
nav {
  position: absolute;

  left: 0;
  top: 54px;

  width: 100%;
  height: 54px;
  background-color: #000;
  color: #fff;

  overflow: hidden;

  z-index: 100;
}

.wrapper {
  position: relative;

  display: flex;
  align-items: center;
  justify-content: space-between;
  max-width: 1880px;
  height: 100%;
  margin: 0 auto;
  padding: 0 32px;

  z-index: 110;
}

.alert-image {
  user-select: none;
}

.alert-header {
  display: flex;
  column-gap: 12px;
}

.alert-icon {
  opacity: 0.3;
}

.alert-actions {
  display: flex;
  align-items: center;
  column-gap: 8px;
}

.alert-shape {
  position: absolute;

  left: 800px;
  top: -1250px;
}

.alert-bg {
  width: 1408px;
  height: 1408px;
  border-radius: 50%;
  background: radial-gradient(50% 50% at 50% 50%, #fae571 0%, rgba(11, 14, 23, 0) 100%);
  filter: blur(92px);
}
</style>
