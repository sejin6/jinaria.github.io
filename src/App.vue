<template>
  <Header></Header>
  <Nav :pages="pages" @moveToLink="moveToLink" :currentPage="currentPage"></Nav>
  <Main :currentPage="currentPage"></Main>
  <Footer></Footer>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Main from './components/Main.vue';
import Nav from './components/Nav.vue';
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import Page from './components/pages/Page';
import menus from './components/pages/menus.json';


@Options({
  components: {
    Header,
    Main,
    Nav,
    Footer
  },
  data() {
    return {
      pages: getPageList(),
      currentPage: menus.intro
    }
  }
})
export default class App extends Vue {
  pages!: Array<Page>
  currentPage!: Page
  moveToLink(event: Event, link: Page) {
    console.log(`say ${link.title}`);
    this.currentPage = link;
  }
  
}

function getPageList(): any {
  return menus;
}

</script>

<style lang="scss">
@import '../static/common.scss';

#app {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  font-size: 14px;
  position: relative;
  height:100%;
  
  
  
}
</style>
