<template>
    <div>
        <section class="clients">
            <div class="container">
                <h1>Past clients</h1>
                <p>Trusted by your favourite companies</p>
                <div class="client_logo">
                    <div><img src="@/assets/icon/client1.svg" ></div>
                    <div><img src="@/assets/icon/client2.svg" ></div>
                    <div><img src="@/assets/icon/client3.svg" ></div>
                    <div><img src="@/assets/icon/client4.svg" ></div>
                    <div><img src="@/assets/icon/client5.svg" ></div>
                </div>
            </div>
        </section>
        <ClientsBg/>
    </div>
</template>

<script>
import ClientsBg from './ClientsBg.vue';
export default {
    name: 'clients-vue',
    components: {
        ClientsBg
    }
}
</script>

<style lang="scss" scoped>
@import '@/assets/scss/variables.scss';

.clients {
    background: #000;
    padding: 120px 0;
    @media (max-width: 991px) {
        padding: 90px 0;
    }
    @media (max-width: 575px) {
        padding: 60px 0;
    }

    h1 {
        text-align: center;
        font-size: 42px;
        line-height: 105%;
        @media (max-width: 575px) {
            font-size: 28px;
        }
    }
    p {
        text-align: center;
        font-size: 24px;
        line-height: 125%;
        color: $grey-color;
        @media (max-width: 575px) {
            font-size: 16px;
        }
    }
    .client_logo {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-top: 60px;
        flex-wrap: wrap;

        @media (max-width: 575px) {
            margin-top: 30px;
        }

        div {
            flex: 0 0 20%;
            display: flex;
            justify-content: center;

            @media (max-width: 991px) {
                flex: 0 0 50%;
                margin-bottom: 50px;

                &:last-child {
                    flex: 0 0 100%;
                    margin-bottom: 0;
                }
            }
        }
    }
}
</style>