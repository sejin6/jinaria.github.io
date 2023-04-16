<template>
    <div class="nav">
        <ul>
           <NavItem v-for="a in pages" v-bind:key="a" :msg="a" v-on:click="link()"></NavItem>
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
        pages:[]
    },
    methods: {
        link: function() {
            alert('clicked!');
        }
    }
    
})

export default class Nav extends Vue {
    pages!: []
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