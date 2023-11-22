<template >
    <div class="heroHeigth position-relative">
        <div class="costume-bg overflow-hidden overflow-x-hidden ">

            <img v-for="image in bgDataStructure" :src="image.url" alt=""
                class="position-absolute costume-min bg-transparent "
                :style="`z-index: ${image.z}; bottom: ${image.bottom}%; left: ${image.left}%; transform: rotate(${image.rotate}deg)`">

        </div>
        <div class="hero-content heroHeigth h-100 d-flex flex-column justify-content-center ">
            <div class="d-flex flex-column justify-content-center gap-2 ">
                <div class="specialItalic text-center hero-content bg-transparent">
                    Hello, Im Martin
                </div>
                <div class="text-center text-my hero-content bg-transparent">Artist Coaching And Mentoring <br> Might Be for
                    You</div>
                <div class="btn my-btn-orange text-center align-self-center text-light hero-content ">
                    Get started today
                </div>
            </div>
        </div>
    </div>
    <!-- background to be added -->
</template>

<script>
export default {
    name: 'HeroComponent',
    data() {
        return {
            bgDataStructure: [

                {
                    //macchia
                    url: '/img/artist-shape-02.png',
                    bottom: '30',
                    left: '0',
                    z: 100,
                },
                {
                    //punti
                    url: '/img/maxcoach-shape-05.png',
                    bottom: '50',
                    left: '80',
                    z: 200,
                    rotate: 0,

                },
                {
                    //forma blu
                    url: '/img/maxcoach-shape-05.png',
                    bottom: '0',
                    left: '10',
                    z: 300,
                    rotate: 0,
                },
                {
                    //forma allungata
                    url: '/img/artist-shape-05.png',
                    bottom: '10',
                    left: '60',
                    z: 400,
                    rotate: 0,
                },
                {
                    //penna
                    url: '/img/artist-shape-04.png',
                    bottom: '0',
                    left: '85',
                    z: 500,
                    rotate: 0,
                },
                {
                    //penna
                    url: '/img/artist-shape-02.png',
                    bottom: '0',
                    left: '20',
                    z: 600,
                    rotate: 180,
                },

            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/style/main' as *;
@use '../assets/style/partials/variables' as *;

* {
    background-color: #fbf9f6;
}

.costume-bg {
    max-width: 100%;
    width: 100%;
    height: 100%;
    overflow: hidden;
}

.heroHeigth {
    min-height: 600px;
}

.hero-content {
    z-index: 2000;
}

.btn {
    width: max-content;
}

.text-my {
    font-size: 3em;
}

.costume-min {}
</style>