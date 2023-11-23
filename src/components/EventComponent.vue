<template>
    <div class=" py-5 ">
        <div class="specialItalic text-center">
            Upcoming Events
        </div>
        <div class="eventTitle text-center">
            Let's Work Together
        </div>
        <div class="card-wrapper d-flex flex-row justify-content-start flex-wrap">
            <div v-for="card in eventCards" class="w-50 cardHeight p-5  ">
                <!-- dinamic class for card position in the page -->
                <div class="d-flex  justify-content-center gap-4 "
                    :class="card.isTxtRight ? 'flex-row' : 'flex-row-reverse'">
                    <div class="image-container card-height">
                        <img class="img-hoverable overflow-hidden " :src="card.image" :alt="card.title">
                    </div>
                    <div class="text-container d-flex flex-column align-items-start justify-content-center ">
                        <div class="date">
                            {{ card.date }}
                        </div>
                        <div class="title">
                            {{ card.title }}
                        </div>
                        <div class="position">
                            <i class="fa-solid fa-location-dot"></i>&nbsp;{{ card.date }}
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'EventComponent',
    data() {
        return {
            eventCards: [
                {
                    isTxtRight: true,
                    date: 'NOV 22, 2020',
                    title: 'Storytelling Workshop',
                    position: 'Textas US',
                    image: '/img/artist_event_1.jpg'
                },
                {
                    isTxtRight: true,
                    date: 'NOV 22, 2020',
                    title: 'Storytelling Workshop',
                    position: 'Textas US',
                    image: '/img/artist_event_2.jpg'
                },
                {
                    isTxtRight: false,
                    date: 'NOV 22, 2020',
                    title: 'Storytelling Workshop',
                    position: 'Textas US',
                    image: '/img/artist_event_3.jpg'
                },
                {

                    isTxtRight: false,
                    date: 'NOV 22, 2020',
                    title: 'Storytelling Workshop',
                    position: 'Textas US',
                    image: '/img/artist_event_4.jpg'
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
.cardHeight {
    height: 400px;

}

.image-container {
    max-width: 300px;
    min-width: 300px;
}

.specialItalic {
    font-size: 2em;
}

.eventTitle {
    font-size: 2.5em;
    font-weight: bolder;
}
</style>