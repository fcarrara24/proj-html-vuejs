<template>
    <div class="px-5 pt-5 d-flex flex-row justify-content-between bg-alert">
        <div v-for="part in footerData">

            <div :class="part.isLarge ? 'largeCard' : 'SmallCard'" class="w-100 d-flex flex-column">
                <div class="footerTitle">
                    {{ part.section }}&nbsp;
                    <!-- tag -->
                    <span class="text-orange">{{ part.tag }}</span>
                </div>
                <div v-for="link in part.links">
                    <a :href="link.url">{{ link.name }}</a>
                </div>
                <!-- socials -->
                <div class="d-flex flex-row pt-4 ">
                    <div v-for="social in part.socials" class="d-flex flex-row justify-content-start ">
                        <div class="px-2">
                            <i :class="social.class"></i>
                        </div>
                    </div>
                </div>
                <!-- image -->
                <div class="d-flex flex-row pt-4 ">
                    <div v-for="image in part.images" class="d-flex flex-row justify-content-start p-2 ">
                        <div class=" footer-image-container">
                            <img :src="image.urlImg" />
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="w-100 d-flex justify-content-center flex-row py-5 text-secondary ">
        © 2020 Maxcoach. All Rights Reserved
    </div>
</template>

<script>
import { footbarComponent } from '@/data/footbarComponent.js'
export default {
    name: 'FooterComponent',
    data() {
        return {
            footerData: footbarComponent,
        }
    }
}
</script>

<style lang="scss" scoped>
.largeCard {
    width: 300px;
}

.SmallCard {
    width: auto;
}

.footer-img-dimensions {
    max-width: 100px;
    max-height: 100px;
}

a {
    color: black;
    text-decoration: none;
}

.footerTitle {
    font-size: 1.5em;
    font-weight: 500;
    padding-bottom: 10px;
}

.footer-image-container {
    width: 100px;
    height: 100px;
}

img {
    width: 100%;
    height: 100%;
}
</style>