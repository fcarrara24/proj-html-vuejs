<template>
    <div v-if="!ignored">
        <div class="card-height m-2 p-5 d-flex flex-column justify-content-evenly "
            :class="selected ? 'bg-white' : 'bg-grey'">
            <div class="card-title">
                {{ card.title }}
            </div>
            <div class="card-description">
                {{ card.description }}
            </div>
            <div class="card-user d-flex flex-row justify-content-start">
                <div class="img-container">
                    <img :src="`/img/artist-testimonial-avatar-0${card.user.imgPosition}.jpg`" class=" circled " alt="">
                </div>
                <div class="userInfo d-flex flex-column justify-content-start ">
                    <div class="title">
                        {{ card.user.name }}
                    </div>
                    <div>
                        {{ card.user.job }}
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'UserCardCompnent',
    props: {
        cardSpecifics: Object,
        selected: Boolean,
        ignored: Boolean,
    },
    data() {
        return {
            card: this.cardSpecifics,
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/style/main' as *;
@use '../assets/style/partials/variables' as *;

.bg-grey {
    background-color: #fcfbfa;
}

.circled {
    width: 50%;
    border-radius: 50%;
}

.card-title {
    color: black;
    font-weight: 800;
}

.card-description {
    color: gray;
}

.img-container {
    width: fit-content;
}
</style>