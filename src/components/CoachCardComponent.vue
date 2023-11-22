<template>
    <div class="p-3 m-2 w-100 d-flex flex-column justify-content-start card-height caochCard position-relative ">
        <div class="w-100 img-container">
            <img class="img-hoverable" :src="card.imageLink" alt="">
        </div>
        <div class="text-container p-2 flex-grow-1 d-flex flex-column justify-content-between cardWrites">
            <div class="price text-orange">
                $ {{ card.dollarPrice }}.00
            </div>
            <div class="caochCardTitle">
                {{ card.title }}
            </div>
            <div class="coachCardInfo">
                <!-- numero lezioni -->
                <span><i class="fa-light fa-file-lines"></i> {{ card.lessons }} Lessons </span>
                <!-- numero studenti -->
                <span><i class="fa-regular fa-user"></i>&nbsp; {{ card.capacity }} Studenti </span>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CoachCardComponent',
    props: {
        cardStyle: Object
    },
    data() {


        return {
            card: this.cardStyle,
        }
    }
}
</script>

<style lang="scss" scoped>
.caochCardTitle {
    font-size: 1.3em;
    font-weight: bold;

    &:hover {
        color: #EF6F31;
    }
}

.text-orange {
    color: #EF6F31;
    padding: 10px, 0;
    font-weight: 900;
}

.img-container {
    max-width: 100%;
    overflow: hidden;
}

img {
    width: 100%;
}

.card-height {
    min-height: 400px;
}

.coachCardInfo {
    font-size: 0.75em;
}

.caochCard:hover .cardWrites {
    position: absolute;
    top: 60%;
    background-color: white;
    border: 2px solid #EF6F31;
}
</style>