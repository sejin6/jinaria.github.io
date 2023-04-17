<template>
    <li :class="'nav-item' + (selected ? ' selected' : '')">
        {{ title }}
    </li>
</template>
<script lang="ts">
import {Options, Vue} from 'vue-class-component';

@Options({
    props: ['title', 'selected']
})

export default class NavItem extends Vue {
    title!: String
    selected!: boolean
}
</script>
<style lang="scss" scoped>
@import '../../static/common.scss';
    .nav-item {
        list-style: none;
        height: 60px;
        text-align: center;
        line-height: 60px;
        display: inline-block;
        width: 200px;
        margin: 0 50px 0 50px;
        &:hover {
            background: linear-gradient(to bottom, white 70%, rgb(179, 214, 238));
            cursor:pointer;
        }
        &::after {
            content:"";
            position: relative;
            width: 180px;
            display: block;
            border-bottom: 1px solid rgb(179, 214, 238);
            margin-left: 10px;
            top: -1px;
        }
    }
    .selected {
        background: linear-gradient(to bottom, white 80%, rgb(179, 214, 238));
    }
</style>