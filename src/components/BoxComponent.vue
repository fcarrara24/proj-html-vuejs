<template>
    <!-- costume bg -->

    <div class="height-box position-relative ">
        <div class="costume-bg overflow-hidden overflow-x-hidden position-absolute ">

            <img v-for="image in bgDataStructure" :src="image.url" alt=""
                class="position-absolute costume-min bg-transparent "
                :style="`z-index: ${image.z}; bottom: ${image.bottom}%; left: ${image.left}%; transform: rotate(${image.rotate}deg)`">

        </div>
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
            <div class=" w-100 d-flex flex-row justify-content-between align-items-center  ">
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
                        <div class="btn invertedBtn ">Get Started Today</div>
                    </div>
                </div>
            </div>

        </div>
        <div class="videoContainer d-flex flex-row justify-content-center my-5 py-3">
            <!--   ILWSp0m9G2U-->
            <iframe src="https://www.youtube.com/embed/ElFJ1qcl74U" frameborder="0" allowfullscreen
                allow="autoplay; encrypted-media"></iframe>
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
            ],
            bgDataStructure: [

                {
                    // V
                    url: '/img/maxcoach-shape-14-1536x343.png',
                    bottom: '85',
                    left: '0',
                    z: 100,
                },
                {
                    //punti
                    url: '/img/maxcoach-shape-13-150x150.png',
                    bottom: '80',
                    left: '90',
                    z: 200,
                    rotate: 0,

                },
                {
                    //forma blu
                    url: '/img/artist-shape-01-600x577.png',
                    bottom: '90',
                    left: '10',
                    z: 300,
                    rotate: 0,
                },
                {
                    //forma allungata
                    url: '/img/artist-shape-01.png',
                    bottom: '80',
                    left: '50',
                    z: 400,
                    rotate: 0,
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
    font-size: 3em;
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
    width: 20%;
    overflow-x: hidden;
}

.mid-cursive-size {
    font-size: 24px;
}

iframe {

    //560px
    width: 60vw;
    //315px
    height: 33vw;
}

.costume-bg {
    max-width: 100%;
    width: 100%;
    height: 3000px;
    overflow: hidden;
    z-index: 0;
}
</style>