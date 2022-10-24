<template>
    <section class="about">
        <div class="container">
            <h1>What we do</h1>
            <p>The areas that we're specialized in.</p>

            <div class="about_gallery">
                <div class="about_gallery-item">
                    <div class="about_gallery-item_text">
                        <h2>Product Photography</h2>
                        <p>Cras commodo consequat orci, in convallis risus egestas non. Nulla efficitur auctor hendrerit. Etiam ut orci varius, faucibus libero ac, cursus quam.</p>
                        <a href="#">Read more</a>
                    </div>
                </div>
                <div class="about_gallery-item">
                    <div class="about_gallery-item_text">
                        <h2>Product Photography</h2>
                        <p>Cras commodo consequat orci, in convallis risus egestas non. Nulla efficitur auctor hendrerit. Etiam ut orci varius, faucibus libero ac, cursus quam.</p>
                        <a href="#">Read more</a>
                    </div>
                </div>
                <div class="about_gallery-item">
                    <div class="about_gallery-item_text">
                        <h2>Product Photography</h2>
                        <p>Cras commodo consequat orci, in convallis risus egestas non. Nulla efficitur auctor hendrerit. Etiam ut orci varius, faucibus libero ac, cursus quam.</p>
                        <a href="#">Read more</a>
                    </div>
                </div>
                <div class="about_gallery-item">
                    <div class="about_gallery-item_text">
                        <h2>Product Photography</h2>
                        <p>Cras commodo consequat orci, in convallis risus egestas non. Nulla efficitur auctor hendrerit. Etiam ut orci varius, faucibus libero ac, cursus quam.</p>
                        <a href="#">Read more</a>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'about-vue'
}
</script>

<style lang="scss" scoped>
@import '@/assets/scss/variables.scss';

.about {
    background: #000;
    padding: 120px 0;
    @media (max-width: 991px) {
        padding: 90px 0;
    }
    @media (max-width: 575px) {
        padding: 50px 0;
    }

    h1 {
        text-align: center;
        font-size: 40px;
        margin-bottom: 15px;
        @media (max-width: 575px) {
            font-size: 32px;
        }
    }
    p {
        color: $grey-color;
        font-size: 23px;
        text-align: center;

        @media (max-width: 575px) {
            font-size: 16px;
        }
    }

    .about_gallery {
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        padding-top: 40px;


        .about_gallery-item {
            flex: 0 0 49.5%;
            height: 600px;
            margin-bottom: 15px;
            background-position: center;
            background-size: 100%;
            background-repeat: no-repeat;
            position: relative;
            transition: background-size .3s ease-in;

            @media (max-width: 1199px) {
                height: 400px;
            }
            @media (max-width: 991px) {
                height: 380px;
                margin-bottom: 10px;
            }
            @media (max-width: 767px) {
                flex: 0 0 100%;
            }
            @media (max-width: 420px) {
                height: 320px;
            }

            &:hover {
                background-size: 105%;
            }

            &:nth-child(1) {
                background-image: url('@/assets/img/about1.jpg');
            }
            &:nth-child(2) {
                background-image: url('@/assets/img/about2.jpg');
            }
            &:nth-child(3) {
                background-image: url('@/assets/img/about3.jpg');
            }
            &:nth-child(4) {
                background-image: url('@/assets/img/about4.jpg');
            }

            .about_gallery-item_text {
                position: absolute;
                left: 30px;
                bottom: 30px;
                right: 30px;

                h2 {
                    font-size: 14px;
                    line-height: 1.3;
                    letter-spacing: 2px;
                    text-transform: uppercase;
                    margin-bottom: 10px;
                }
                p {
                    font-size: 14px;
                    color: $grey-color;
                    text-align-last: left;
                    line-height: 143%;
                    margin-bottom: 10px;

                    @media (max-width: 991px) {
                        overflow: hidden;
                        text-overflow: ellipsis;
                        display: -webkit-box;
                        -webkit-line-clamp: 1;
                        -webkit-box-orient: vertical;
                    }
                }
                a {
                    display: inline-block;
                    background-color: #fff;
                    color: #000;
                    padding: 10px;
                    border-radius: 14px;
                    font-size: 15px;
                    letter-spacing: .4px;
                    @media (max-width: 575px) {
                        font-size: 12px;
                    }
                }
            }
        }
    }
}
</style>