<template>
    <div class="w-100 container">
        <div class=" d-flex flex-row justify-content-between py-4">
            <div class="img-container">
                <img class="header-height" src="../assets/img/dark-logo.png" alt="">
            </div>
            <!-- navbar components  -->
            <div class="d-flex flex-row justify-content-center gap-3 align-items-start position-relative ">
                <div v-for="section in HeaderArray" class="dropdown h-100">
                    <div class="dropbtn h-100 ">
                        {{ section.name }}
                    </div>
                    <!-- sezione senza immagine -->
                    <div class="dropdown-content bg-white position-absolute " v-if="!section.img">
                        <div class="dropdown-section d-flex flex-column flex-wrap overflow-hidden ">
                            <div class="reference-container d-flex flex-row justify-content-start align-items-start  pe-3 h-100"
                                v-for="(reference, ind) in section.categories">
                                <a :href="reference.link">
                                    {{ reference.title }}
                                </a>
                                <div v-if="reference.relevance !== 'none'">
                                    {{ reference.relevance }}
                                </div>
                            </div>
                        </div>

                    </div>
                    <!-- sezione con immgine da completare -->
                    <div v-else-if="section.img" class=" bg-white dropdown-with-image">
                        <div class="dropdown-section d-flex flex-column flex-wrap overflow-hidden ">
                            <div class="reference-container d-flex flex-row justify-content-start align-items-start  p-3 h-100"
                                v-for="(reference, ind) in section.categories">
                                <a :href="reference.link">
                                    {{ reference.title }}
                                </a>
                                <div v-if="reference.relevance !== 'none'">
                                    {{ reference.relevance }}
                                </div>

                            </div>
                            <div class="image">
                                <img width="200" height="100" :src="section.img" alt="">
                            </div>
                        </div>


                    </div>
                </div>
            </div>

            <div class="header-Socials d-flex flex-row justify-content-end  gap-3 align-items-center">
                <!-- implementing socials dinamically -->
                <div class=" d-flex flex-row align-items-center justify-content-end h-100 px-2 " v-for="social in socials">
                    <i :class="social.icon" :href="social.link" class="social-icons" style="color: gray;"></i>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { navbarCoponents } from '@/data/navbarComponents.js'
export default {
    name: 'HeaderComponent',
    data() {
        return {
            socials: [
                {
                    name: 'twitter',
                    link: '#',
                    icon: 'fa-brands fa-twitter'
                },
                {
                    name: 'facebook',
                    link: '#',
                    icon: 'fa-brands fa-facebook-f'
                },
                {
                    name: 'instagram',
                    link: '#',
                    icon: 'fa-brands fa-instagram'
                },
                {
                    name: 'linkedin',
                    link: '#',
                    icon: 'fa-brands fa-linkedin'
                },

            ],
            HeaderArray: navbarCoponents,
        }
    }
}
</script>


<style lang="scss" scoped>
@use '../assets/style/main' as *;
@use '../assets/style/partials/variables' as *;

.social-icons {
    font-size: 1.5em;
}

.header-height {
    max-height: 40px;
}

.dropdown {
    position: relative;
    display: inline-block;

    &:hover>.dropdown-content {
        display: block;
        padding: 20px;
        padding-left: 0;
        padding-bottom: 20px;
        min-width: 15vw;
    }

    &:hover>.dropdown-with-image {
        display: block;
    }
}

.dropdown-content {
    display: none;
    min-width: 15vw;

}

.dropdown-section {
    max-height: 300px;
    border-bottom: 3px solid $backgroundBtnOrange;
}

.dropdown-with-image {
    display: none;
    position: absolute;
    min-width: 60vw;
    transform: translate(-50%, 0);
}

.dropbtn:hover {

    color: #EF6F31;

}

a {
    text-decoration: none;
    color: black;
}
</style>