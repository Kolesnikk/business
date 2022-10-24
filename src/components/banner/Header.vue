<template>
    <header class="header">
        <div class="container">
            <div class="header-flex">
                <a class="logo">
                    <img src="@/assets/icon/logo.svg" alt="">
                </a>
                <ul class="nav" :class="{open: isOpen}">
                    <li><a href="#">Business areas</a></li>
                    <li><a href="#">Featured images</a></li>
                    <li><a href="#">Gear cage</a></li>
                    <li><a href="#">Contact</a></li>
                    <li><a href="#">Get template</a></li>
                </ul>

                <div class="hamburger-lines" @click="isOpen=!isOpen" :class="{open: isOpen}">
                    <span class="line line1"></span>
                    <span class="line line2" ></span>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: 'header-vue',
    data() {
        return {
            isOpen: false
        }
    }
}
</script>

<style lang="scss" scoped>
@import '@/assets/scss/variables.scss';

.header {
    position: fixed;
    left: 0;right: 0;top: 0;
    background: $grey-bg;
    padding: 24px 0;

    .header-flex {
        display: flex;
        justify-content: space-between;
        align-items: center;

        .logo {
            display: inline-block;
            cursor: pointer;
            transition: .3s;
            &:hover {
                opacity: .7;
            }
        }

        .nav {
            display: flex;
            align-items: center;

            li {
                &:not(:last-child) {
                    margin-right: 30px;
                    position: relative;
                    &::before {
                        content: '';
                        display: block;
                        position: absolute;
                        bottom: -10px;left: 0;
                        width: 0;
                        height: 2px;
                        background-color: #fff;
                        transform: skew(-45deg);
                        transition: .3s ease-in-out;
                    }
                    &:hover::before {
                        width: 100%;
                    }

                    
                    @media (max-width: 991px) {
                        margin-right: 15px;
                    }
                }

                &:last-child {
                    padding: 10px 20px;
                    background-color: #fff;
                    border-radius: $btn-radius;
                    a {
                        color: #000;
                    }
                }
            }
        }

        .hamburger-lines {
            display: block;
            z-index: 3;
            display: none;

            &.open {
                .line2 {
                    width: 30px;
                    margin-left: 0;
                }
            }

            .line {
                background-color: #fff;
                display: block;
            }
            .line1 {
                width: 30px;
                height: 2px;
                margin-bottom: 5px;
            }
            .line2 {
                width: 15px;
                height: 2px;
                margin-left: 15px;
                transition: .3s;
            }
        }
    }
}

@media (max-width: 840px) {
    .nav {
        position: absolute;
        right: -100%;top: 0;
        width: 320px;
        height: 100vh;
        background-color: $grey-bg;
        flex-direction: column;
        padding-top: 100px;
        transition: .3s ease-in-out;
        &.open {
            right: 0;
        }

        li {
            margin-right: 0;

            &:not(:last-child) {
                margin: 0px 0px 30px 0 !important;
                text-align: center;
            }
        }
    }
    .hamburger-lines {
        display: block !important;
    }

}

</style>