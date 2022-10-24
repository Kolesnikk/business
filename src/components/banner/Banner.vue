<template>
    <section class="banner">
        <div class="container">
            <div class="banner-text">
                <h3>Photographer & Filmmaker</h3>
                <h1>Aperture Studios</h1>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse varius enim in eros elementum tristique. Duis cursus, mi quis viverra ornare, eros dolor interdum nulla, ut commodo diam libero vitae erat. Aenean faucibus nibh et justo cursus id rutrum lorem imperdiet. Nunc ut sem vitae risus tristique posuere.</p>
            </div>

            <Location class="location" time="1/2000s" cyrcle="f/11" iso="100" location="Iceland"/>
        </div>
    </section>
</template>

<script>
import Location from '../location.vue'

export default {
    name: 'banner-vue',
    components: {
        Location
    }
}
</script>

<style lang="scss" scoped>
@import '@/assets/scss/variables.scss';

.banner {
    height: 100vh;
    background-image: url('@/assets/img/banner-bg.jpg');
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    position: relative;

    .container {
        height: 100%;
    }

    .banner-text {
        position: absolute;
        bottom: 100px;
        max-width: 780px;
        left: 50%;
        transform: translateX(-50%);
        text-align: center;
        
        @media (max-width: 1199px) {
            width: 780px;
        }
        @media (max-width: 991px) {
            width: 580px;
        }
        @media (max-width: 767px) {
            width: 520px;
        }
        @media (max-width: 575px) {
            width: 90%;
        }
        
        h3 {
            letter-spacing: 2px;
            text-transform: uppercase;
            color: $grey-color;
            font-size: 18px;
            line-height: 143%;
            margin-bottom: 10px;
            @media (max-width: 575px) {
                font-size: 16px;
                margin-bottom: 10px;
            }
        }
        h1 {
            font-size: 54px;
            line-height: 110%;
            margin-bottom: 18px;

            @media (max-width: 575px) {
                font-size: 32px;
                margin-bottom: 10px;
            }
        }
        p {
            font-size: 18px;
            color: $grey-color;
            line-height: 143%;

            
            @media (max-width: 1199px) {
                font-size: 16px;
            }
            @media (max-width: 991px) {
                overflow: hidden;
                text-overflow: ellipsis;
                display: -webkit-box;
                -webkit-line-clamp: 3;
                -webkit-box-orient: vertical;
            }
            @media (max-width: 575px) {
                font-size: 14px;
            }
        }
    }

    .location {
        position: absolute;
        right: 60px;
        bottom: 60px;

        
        @media (max-width: 1199px) {
            right: 40px;
            bottom: 40px;
        }
        @media (max-width: 575px) {
            width: 300px;
            right: 0px;
            bottom: 20px;
            left: 50%;
            transform: translate(-50%);
        }
    }
}
</style>