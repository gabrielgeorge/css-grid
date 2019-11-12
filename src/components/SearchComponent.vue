<template>
  <div class="form-group p-2">
    <input type="text" name="searchControl" class="form-control" placeholder="Search item..." />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class SearchComponent extends Vue {}
</script>
