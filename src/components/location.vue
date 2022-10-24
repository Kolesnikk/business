<template>
    <div class="location">
        <ul>
            <li><img src="@/assets/icon/clock.svg">{{time}}</li>
            <li><img src="@/assets/icon/cyrcle.svg">{{cyrcle}}</li>
            <li><img src="@/assets/icon/iso.svg">{{iso}}</li>
            <li><img src="@/assets/icon/location.svg">{{location}}</li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'location-vue',
    props: {
        time: String,
        cyrcle: String,
        iso: String, 
        location: String
    }
}
</script>

<style lang="scss" scoped>
.location {
    ul {
        display: flex;
        align-items: center;
        justify-content: space-between;

        li{
            display: flex;
            align-items: center;

            &:not(:last-child) {
                margin-right: 16px;
            }

            img {
                display: inline-block;
                margin-right: 6px;
            }
        }
    }
}
</style>