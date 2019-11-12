<template>
  <div class="main-content">
    <div class="card">
      <div class="card-body p-4">Item 1</div>
    </div>
    <div class="card">
      <div class="card-body p-4">Item 2</div>
    </div>
    <div class="card">
      <div class="card-body p-4">Item 3</div>
    </div>
    <div class="card">
      <div class="card-body p-4">Item 4</div>
    </div>
    <div class="card">
      <div class="card-body p-4">Item 5</div>
    </div>
    <div class="card">
      <div class="card-body p-4">Item 5</div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class MainContent extends Vue {}
</script>

<style scoped lang="css">
.main-content {
  display: grid;
  grid-gap: 1rem;
}

@media (max-width: 767px) {
  .main-content {
    grid-template-columns: repeat(2, 1fr);
  }
}
@media (min-width: 768px) {
  .main-content {
    grid-template-columns: repeat(3, 1fr);
  }
}
@media (min-width: 1200px) {
  .main-content {
    grid-template-columns: repeat(4, 1fr);
  }
}

.item {
  border: 1px solid black;
  background-color: #eaeaea;
  min-height: 250px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
