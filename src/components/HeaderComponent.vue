<template>
    <div class="w-100 container">
        <div class=" d-flex flex-row justify-content-between py-4">
            <div class="img-container">
                <img class="header-height" src="../assets/img/dark-logo.png" alt="">
            </div>
            <div>

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
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
.social-icons {
    font-size: 1.5em;
}

.header-height {
    max-height: 40px;
}
</style>