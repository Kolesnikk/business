<template>
    <section class="gallery">
        <GalleryTop/>
        <GalleryCenter/>
        <GalleryBottom/>
    </section>
</template>

<script>
import GalleryTop from './GalleryTop.vue'
import GalleryCenter from './GalleryCenter.vue'
import GalleryBottom from './GalleryBottom.vue'
export default {
    name: 'gallery-vue',
    components: {
        GalleryTop,
        GalleryCenter,
        GalleryBottom
    }
}
</script>

<style>

</style>