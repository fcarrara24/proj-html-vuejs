<template >
    <div class="heroHeigth">
        <div class="hero-content heroHeigth h-100 d-flex flex-column justify-content-center ">
            <div class="d-flex flex-column justify-content-center gap-2 ">
                <div class="specialItalic text-center">
                    Hello, Im Martin
                </div>
                <div class="text-center text-my">Artist Coaching And Mentoring <br> Might Be for You</div>
                <div class="btn my-btn-orange text-center align-self-center text-light ">
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
        return {}
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/style/main' as *;
@use '../assets/style/partials/variables' as *;

.heroHeigth {
    min-height: 600px;
}

.hero-content {
    z-index: 1000;
}

.btn {
    width: max-content;
}

.text-my {
    font-size: 3em;
}
</style>