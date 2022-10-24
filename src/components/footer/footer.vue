<template>
    <footer class="footer">
        <div class="container">
            <div class="footer_content">
                <p>© Copyright 2022</p>
                <a href="https://t.me/D_rose666" target="_blank">
                    <img src="@/assets/icon/telegram.svg">
                    Telegram
                </a>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'footer-vue'
}
</script>

<style lang="scss" scoped>
@import '@/assets/scss/variables.scss';
.footer {
    background: $grey-bg;
    padding: 30px 0;

    .footer_content {
        display: flex;
        justify-content: space-between;
        align-items: center;

        a {
            display: flex;
            align-items: center;
            &:hover {
                text-decoration: underline;
            }
            img {
                height: 20px;
                margin-right: 10px;
            }
        }
    }
}
</style>