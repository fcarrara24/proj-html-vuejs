<template style="width: 100vw!important; z-index: 10000; " >
    <!-- adding timer component for layout choises here and its spacing -->

    <TimerComponent @removeSpacing="removeSpaces" />
    <div class="timerHeight" ref="timerHeightSpacing"></div>


    <div
        class="  position-fixed bg-white bg-white w-100  my-0 p-5 z-hight Header-height d-flex flex-row justify-content-between align-items-center shadow ">

        <div class=" d-flex flex-row justify-content-between py-4 h-100 w-100">
            <div class="img-container h-100">
                <img class="header-height" src="../assets/img/dark-logo.png" alt="">
            </div>
            <!-- traslabile immagine -->
            <div class="background-image">

            </div>
            <!-- navbar components  -->
            <div class="d-flex flex-row justify-content-center gap-3 align-items-center position-relative">
                <div v-for="section in HeaderArray" class="dropdown h-100">
                    <div class="dropbtn h-100 pe-3 ">
                        {{ section.name }}
                        <i class="fa-solid fa-chevron-down fa-2xs"></i>
                        <!-- underline-effect -->
                        <div class="underline-progressive">
                            <div class="underline-filler"></div>
                        </div>
                    </div>
                    <!-- sezione senza immagine -->
                    <div class="dropdown-content bg-white position-absolute shadow" v-if="!section.img">
                        <div class="dropdown-section d-flex flex-column flex-wrap overflow-hidden ">
                            <div class="reference-container d-flex flex-row justify-content-start align-items-start  pe-3 h-100 "
                                v-for="(reference, ind) in section.categories">
                                <a :href="reference.link" class="text-secondary">
                                    {{ reference.title }} &nbsp;&nbsp;&nbsp;
                                </a>
                                <div v-if="reference.relevance !== 'none'" class=" bg-relevance card ">
                                    {{ reference.relevance }}
                                </div>
                            </div>
                        </div>

                    </div>
                    <!-- sezione con immgine da completare -->
                    <div v-else-if="section.img" class=" bg-white dropdown-with-image shadow">
                        <div class="dropdown-section d-flex flex-column flex-wrap overflow-hidden  ">
                            <div class="reference-container d-flex flex-row justify-content-start align-items-start  h-100"
                                v-for="(reference, ind) in section.categories">
                                <a :href="reference.link" class=" text-secondary">
                                    {{ reference.title }} &nbsp;&nbsp;&nbsp;
                                </a>
                                <div v-if="reference.relevance !== 'none'" class="bg-relevance card">
                                    {{ reference.relevance }}
                                </div>

                            </div>
                            <div class="image">
                                <img width="200" height="100" :src="section.img" alt="">
                            </div>
                        </div>

                        <!-- transition group -->

                    </div>
                </div>
            </div>

            <div class="header-Socials d-flex flex-row justify-content-end  gap-3 align-items-center">
                <!-- implementing socials dinamically -->
                <div class=" d-flex flex-row align-items-center justify-content-end h-100 px-2 position-relative social"
                    v-for="social in socials">
                    <i :class="social.icon" :href="social.link" class="social-icons" style="color: gray;"></i>
                    <div class="socialName">
                        {{ social.name }}
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { navbarCoponents } from '@/data/navbarComponents.js'
import TimerComponent from './TimerComponent.vue';
export default {
    name: "HeaderComponent",
    data() {
        return {
            socials: [
                {
                    name: "twitter",
                    link: "#",
                    icon: "fa-brands fa-twitter"
                },
                {
                    name: "facebook",
                    link: "#",
                    icon: "fa-brands fa-facebook-f"
                },
                {
                    name: "instagram",
                    link: "#",
                    icon: "fa-brands fa-instagram"
                },
                {
                    name: "linkedin",
                    link: "#",
                    icon: "fa-brands fa-linkedin"
                },
            ],
            HeaderArray: navbarCoponents,
        };
    },
    methods:
    {
        removeSpaces() {
            this.$refs.timerHeightSpacing.classList.add('d-none');
        }
    },
    components: { TimerComponent }
}
</script>


<style lang="scss" scoped>
@use '../assets/style/main' as *;
@use '../assets/style/partials/variables' as *;

.z-hight {
    z-index: 11000;
}

.social-icons {
    font-size: 1.5em;
}

.header-height {
    max-height: 40px;
}

* {
    z-index: 1000;
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

.reference-container {
    padding: 5px;
}

.dropdown-content {
    display: none;
    min-width: 15vw;
    border-bottom: 3px solid $backgroundBtnOrange;

}

.dropdown-section {
    max-height: 400px;
}

.dropdown-with-image {
    display: none;
    position: absolute;
    min-width: 60vw;
    transform: translate(-50%, 0);
}

.dropbtn {
    justify-content: center;
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 10px;

    &:hover {
        color: #EF6F31;
    }
}


a {
    text-decoration: none;
    color: black;
}

.social:hover .socialName {
    display: block;
}

.socialName {
    position: absolute;
    top: 100%;
    right: 20%;
    color: white;
    background-color: #333333;
    padding: 5px;
    border-radius: 10px;
    display: none;
}

.Header-height {
    max-height: 50px;
}

.underline-progressive {
    display: none;
    width: 100%;
    height: 2px;

    &:hover .underline-filler {
        animation: grow 1s linear;
        width: 100%;
    }

}

.underline-filler {
    width: 0px;
    height: 100%;
    background-color: #EF6F31;
}

.text-secondary {
    color: gray;
}

.bg-relevance {
    font-size: 0.2em;
    color: white;
    font-size: larger;
    background: rgb(180, 58, 140);
    background: linear-gradient(90deg, rgba(180, 58, 140, 1) 0%, rgba(253, 29, 29, 1) 50%, rgba(252, 176, 69, 1) 100%);
}
</style>