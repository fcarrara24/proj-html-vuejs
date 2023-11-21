<template>
    <div>
        <div class="container d-flex flex-column">
            <div class="specialItalic text-center ">
                Artist coaching
            </div>
            <div class="artistTitle text-center">
                Latest Online Courses
            </div>
            <div class="card-container d-flex flex-row flex-wrap justify-content-between ">
                <div class="coachingCard card-width " v-for="card in coachingCard">
                    <CoachCardComponent :cardStyle="card" />
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import CoachCardComponent from './CoachCardComponent.vue';

export default {
    name: "CourseComponent",
    data() {
        return {
            coachingCard: [
                {
                    title: "The Acrylic Painting Academy",
                    dollarPrice: 18,
                    lessons: 4,
                    capacity: 50,
                    //full link src/assets/img/artist-course-01-480x480.jpg
                    imageLink: "/img/artist-course-01-480x480.jpg"
                },
                {
                    title: "Drawing and Shading Complete Course",
                    dollarPrice: 21,
                    lessons: 14,
                    capacity: 50,
                    imageLink: "/img/artist-course-02-480x480.jpg"
                },
                {
                    title: "the Color Theory for Digital Artist",
                    dollarPrice: 19,
                    lessons: 7,
                    capacity: 50,
                    imageLink: "/img/artist-course-03-480x480.jpg"
                },
                {
                    title: "Ultimate Guide to Digital Sketching for Beginner",
                    dollarPrice: 35,
                    lessons: 14,
                    capacity: 50,
                    imageLink: "/img/artist-course-04-480x480.jpg"
                },
                {
                    title: "Portrait Drawing The Smart Way",
                    dollarPrice: 19,
                    lessons: 2,
                    capacity: 50,
                    imageLink: "/img/artist-course-05-480x480.jpg"
                },
                {
                    title: "Mastering Watercolor Painting from Beginner",
                    dollarPrice: 19,
                    lessons: 2,
                    capacity: 50,
                    imageLink: "/img/artist-course-06-480x480.jpg"
                },
                {
                    title: "The Art & Science of Drawing",
                    dollarPrice: 19,
                    lessons: 2,
                    capacity: 50,
                    imageLink: "/img/artist-course-07-480x480.jpg"
                },
                {
                    title: "The Colored Pencil Drawing Course",
                    dollarPrice: 22,
                    lessons: 6,
                    capacity: 50,
                    imageLink: "/img/artist-course-08-480x480.jpg"
                },
            ],
        };
    },
    components: { CoachCardComponent }
}
</script>

<style lang="scss" scoped>
@use '../assets/style/main' as *;
@use '../assets/style/partials/variables' as *;


.artistTitle {
    font-size: 2em;
    font-weight: bolder;
}

.card-width {
    max-width: 20vw;
}
</style>