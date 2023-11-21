<template>
    <div class="height-box">
        <div class="container box-separator ">
            <div class="specialItalic text-center ">
                Artist coaching
            </div>
            <div class="text-center my-title ">
                I understand what it takes to create <br>
                I can help you with
            </div>
            <div class="card-container w-100 d-flex flex-row justify-content-between flex-wrap py-5 ">
                <div v-for="card in cards" class="my-small-card ">
                    <div class="img-container">
                        <img :src="card.img" :alt="card.title">
                    </div>
                    <div class="card-title py-2">
                        {{ card.title }}
                    </div>
                    <div class="card-text">
                        {{ card.description }}
                    </div>
                </div>
            </div>

            <!-- intermediate section -->
            <div class="img-conteiner">
                <img src="../assets/img/artist-quote-icon.png" alt="quote">
            </div>
            <div class=" w-100 d-flex flex-row justify-content-between ">
                <!-- intermediate left -->
                <div class="intermediate-left d-flex flex-column justify-content-start">

                    <div class="big-left-title text-center pb-2 ">
                        I coach and mentor visual artists, like you, to Create Like You Mean It
                    </div>
                    <div class="specialItalic mid-cursive-size text-center">
                        Martin Garrix
                    </div>
                </div>
                <!-- intermediate-right -->
                <div class="intermediate-right">
                    <div class="intermediate-right">
                        <div class="pb-2">
                            As a coach and mentor, my ultimate goal is to motivate visual artists toward inspired action.
                            I help you get you back on track to being the productive, creative, meaningful and authentic
                            artist you truly want to be.I support artists in crafting and living a creative life as well as
                            feeling good about themselves and their art.
                        </div>
                        <div class="pb-2">
                            As an artist and an educator for nearly 30 years, I understand what it takes to create.
                        </div>
                        <div class="btn btn-warning ">Get Started Today</div>
                    </div>
                </div>
            </div>

        </div>

    </div>
</template>

<script>
export default {
    name: 'BoxComponent',
    data() {


        return {
            cards: [
                {
                    img: '/img/artist-box-image-01.png',
                    title: 'Online Coures',
                    description: 'Online art coaching now offers you a very powerfuò way to redesign your artist mind'
                },
                {
                    img: '/img/artist-box-image-02.png',
                    title: 'One to One',
                    description: 'Getting the necessary clarity about the current state to help you improve your ability.'
                },
                {
                    img: '/img/artist-box-image-03.png',
                    title: 'Anywhere',
                    description: 'Access to valuable and portable program which allow you to setup and live anywhere you want.'
                },
                {
                    img: '/img/artist-box-image-04.png',
                    title: 'On Time',
                    description: 'Punctuality is our top priority because it\'s an essential criteria to assess a program quality.'
                },
            ]
        }
    },

}
</script>

<style lang="scss" scoped>
@use '../assets/style/main' as *;
@use '../assets/style/partials/variables' as *;

.my-title {
    font-size: 2em;
    font-weight: bolder;
}

.big-left-title {
    font-size: 2em;
    font-weight: bolder;
}

.intermediate-left {
    max-width: 40%;
    margin-right: 100px;
}

.box-separator {
    margin: 0, 1000px;
}

.my-small-card {
    width: 25%;
    overflow-x: hidden;
}

.mid-cursive-size {
    font-size: 24px;
}
</style>