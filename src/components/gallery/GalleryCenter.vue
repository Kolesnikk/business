<template>
    <div class="gallery_center">
        <div class="gallery_center-left">
            <div class="gallery_center-text">
                <h2>The Gear cage</h2>
                <h1>The tools that we use.</h1>
                <p>The say that "no place is boring if you've had a good night's sleep and have a pocket full of unexposed film". While we don't shoot (a lot) of film these days — these are the tools that we actually use everyday to capture the amazing things around us.</p>
                <a href="#">Check it out</a>
            </div>
        </div>
        <div class="gallery_center-right">
            <Location time='0.8"' cyrcle="f/5,6" iso="100" location="Sweden" class="location"/>
        </div>
    </div>
</template>

<script>
import Location from '@/components/location.vue'
export default {
    name: 'gallery-center',
    components: {
        Location
    }
}
</script>

<style lang="scss" scoped>
@import '@/assets/scss/variables.scss';

.gallery_center {
    width: 100%;
    height: 540px;
    display: flex;
    flex-wrap: wrap;
    @media (max-width: 991px) {
        height: 800px;
    }
    @media (max-width: 575px) {
        height: 640px;
    }

    .gallery_center-left {
        flex: 0 0 50%;
        background: #000;
        display: flex;
        align-items: center;
        justify-content: center;
        @media (max-width: 991px) {
            text-align: center;
        }

        @media (max-width: 991px) {
            flex: 0 0 100%;
            height: 50%;
        }
        @media (max-width: 575px) {
            height: 320px;
        }

        .gallery_center-text {
            padding: 15px 10px;
            max-width: 60%;
            @media (max-width: 575px) {
                max-width: 100%;
            }

            h2 {
                font-size: 14px;
                line-height: 143%;
                letter-spacing: 2px;
                text-transform: uppercase;
                color: $grey-color;
                margin-bottom: 20px;
            }
            h1 {
                font-size: 28px;
                line-height: 114%;
                margin-bottom: 20px;
                
            }
            p {
                font-size: 16px;
                line-height: 143%;
                margin-bottom: 20px;
                @media (max-width: 575px) {
                    font-size: 14px;
                }
            }
            a {
                display: inline-block;
                background-color: #fff;
                color: #000;
                padding: 10px;
                border-radius: 14px;
            }
        }
    }
    .gallery_center-right {
        flex: 0 0 50%;
        background-image: url('@/assets/img/galleryCenter_bg.jpg');
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;
        position: relative;

        @media (max-width: 991px) {
            flex: 0 0 100%;
            height: 50%;
        }
        @media (max-width: 575px) {
            height: 320px;
        }

        .location {
            width: 300px;
            position: absolute;
            right: 60px;
            bottom: 60px;
            @media (max-width: 575px) {
                right: 0px;
                bottom: 40px;
                left: 50%;
                transform: translate(-50%);
            }
        }
    }
}
</style>