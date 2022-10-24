<template>
    <div class="gallery_top">
        <div class="gallery_top-text">
            <h1>Sunset at Mount Fuji</h1>
            <p>Duis tristique sed lorem a vestibulum. Cras commodo consequat orci, in convallis risus egestas non.</p>
        </div>
        <Location class="location" time='1"' cyrcle="f/16" iso="400" location="Japan"/>
    </div>
</template>

<script>
import Location from '@/components/location.vue'
export default {
    name: 'gallery-top',
    components: {
        Location
    },
}


</script>

<style lang="scss" scoped>
@import '@/assets/scss/variables.scss';

.gallery_top {
    width: 100%;
    height: 600px;
    background-image: url('@/assets/img/galleryTop_bg.jpg');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    position: relative;
    display: flex;
    justify-content: flex-end;
    align-items: center;
    padding-right: 5%;

    @media (max-width: 767px) {
        height: 400px;
    }
    @media (max-width: 575px) {
        justify-content: center;
        text-align: center;
    }

    .gallery_top-text {
        max-width: 320px;

        h1 {
            font-size: 18px;
            line-height: 143%;
            letter-spacing: 2px;
            text-transform: uppercase;
        }
        p {
            font-size: 14px;
            line-height: 143%;
            color: $grey-color;
        }
    }

    .location {
        width: 280px;
        position: absolute;
        right: 100px;
        bottom: 60px;

        @media (max-width: 575px) {
            right: 0;
            left: 50%;
            transform: translate(-50%);
            bottom: 40px;
        }
    }
}
</style>