<template>
    <div class="footer">
        <ul>
            <li class="github">
                <a href="https://github.com/sejin6" target="_blank"></a>
            </li>
            <li class="instagram">
                <a href="https://www.instagram.com/jinaria079" target="_blank"></a>
            </li>
        </ul>
    </div>
</template>
<script lang="ts">
import {Options, Vue} from 'vue-class-component';

@Options({

})

export default class Footer extends Vue {
    
}
</script>
<style lang="scss" scoped>
    .footer {
        padding: 20px 16px;
        height: 80px;
        text-align: center;
        ul {
            list-style: none;

            li {
                display: inline-block;
                margin: 0 12px;
                a {
                    text-decoration: none;
                    display: inline-block;
                    width: 40px;
                    height: 40px;
                }
                &.github {
                    a {
                        background-image: url("../../static/github-mark.svg");
                        background-size: 100%;
                    }
                }
                &.instagram {
                    a {
                        background-image: url("../../static/instagram-logo-svgrepo-com.svg");
                        background-size: 100%;
                    }
                }
            }
        }
    }
</style>