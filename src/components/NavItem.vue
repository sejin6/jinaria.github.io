<template>
    <li class="nav-item">
        {{ msg }}
    </li>
</template>
<script lang="ts">
import {Options, Vue} from 'vue-class-component';

@Options({
    props: {
        msg: String
    }
})

export default class NavItem extends Vue {
    msg!: String
}
</script>
<style lang="scss" scoped>
@import '../../static/common.scss';
    .nav-item {
        list-style: none;
        height: 60px;
        border-bottom: 1px solid $border-color;
        text-align: center;
        line-height: 60px;
        
    }
</style>