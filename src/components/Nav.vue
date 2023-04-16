<template>
    <div class="nav">
        <ul>
           <NavItem v-for="page in pages" v-bind:key="page" :msg="page" v-on:click="link($event, page)"></NavItem>
        </ul>
    </div>
</template>

<script lang="ts">
import {Vue, Options} from 'vue-class-component';
import NavItem from './NavItem.vue';

@Options({
    components: {
        NavItem
    },
    props: {
        pages: Array
    }
    
})

export default class Nav extends Vue {
    pages!: Array<String>

    link(event: Event, l:String)  {
        console.log('clicked!');
        this.$emit('moveToLink', event, l);
    }
}

</script>

<style scoped lang="scss">
@import '../../static/common.scss';
    .nav {
        width: 240px;
        height:100%;
        border-right: $border-color 1px solid;
        ul {
            padding: 0;
            margin: 0;
            color: $text-color;
            font-weight: bold;
        }
      
    }
</style>