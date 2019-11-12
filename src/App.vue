<template>
  <div id="app">
    <div class="grid-container">
      <header>
        <HeaderComponent title="Your beloved shop" />
      </header>
      <aside>
        <SearchComponent />
      </aside>
      <main>
        <MainContent />
      </main>
      <footer>
        <FooterComponent />
      </footer>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import SearchComponent from "./components/SearchComponent.vue";
import HeaderComponent from "./components/HeaderComponent.vue";
import FooterComponent from "./components/FooterComponent.vue";
import MainContent from "./components/MainContent.vue";

@Component({
  components: {
    HeaderComponent,
    SearchComponent,
    FooterComponent,
    MainContent
  }
})
export default class App extends Vue {}
</script>
<style scoped>
.grid-container {
  display: grid;
  height: 100vh;
  width: 100vw;
}

@media (max-width: 767px) {
  .grid-container {
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: 100px 50px 1fr 50px;

    grid-template-areas:
      "header header header"
      "aside aside aside"
      "main   main   main"
      "footer footer footer";
  }
}

@media (min-width: 768px) {
  .grid-container {
    grid-template-columns: repeat(5, 1fr);
    grid-template-rows: 100px 3fr 50px;

    grid-template-areas:
      "header header header header header"
      "aside  main   main   main   main"
      "aside  footer footer footer footer";
  }
}

header {
  background-color: rgba(223, 52, 52, 0.6);
  grid-area: header;
  display: flex;
  align-items: center;
  justify-content: center;
}

aside {
  background-color: rgba(226, 233, 128, 0.685);
  grid-area: aside;
}

main {
  background-color: rgba(80, 208, 240, 0.6);
  grid-area: main;
}

footer {
  background-color: rgba(237, 218, 255, 0.6);
  grid-area: footer;
  display: flex;
  align-items: flex-end;
}
</style>