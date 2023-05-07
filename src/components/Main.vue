<template>
    <div class="main">
        <h1>{{ currentPage.title }}</h1>
        <div class="contents">
            {{ currentPage.contents }}
        </div>
    </div>
</template>

<script lang="ts">
import Page from './pages/Page';
import {Vue, Options} from 'vue-class-component';

@Options({
  props: ['currentPage']
})

export default class Main extends Vue {

    currentPage!: Page
}
</script>

<style scoped>
    .main {
        text-align: center;
        height: 800px;
        margin-top: 48px;
        border-bottom: 1px solid #eee;
    }
</style>