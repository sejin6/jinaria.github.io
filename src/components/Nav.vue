<template>
    <div class="nav">
        <ul>
           <NavItem v-for="page in pages" v-bind:key="page" :title="page.title" v-on:click="link($event, page)" :selected="currentPage.title === page.title"></NavItem>
        </ul>
    </div>
</template>

<script lang="ts">
import {Vue, Options} from 'vue-class-component';
import NavItem from './NavItem.vue';
import Page from './pages/Page';

@Options({
    components: {
        NavItem
    },
    props: ['pages', 'currentPage']
    
})

export default class Nav extends Vue {
    pages!: Array<Page>
    currentPage!: Page

    link(event: Event, l:Page)  {

        this.$emit('moveToLink', event, l);
    }
}

</script>

<style scoped lang="scss">
@import '../../static/common.scss';
    .nav {
        text-align: center;
        ul {
            padding: 0;
            margin: 0;
            color: $text-color;
            font-weight: bold;
        }
      
    }
</style>