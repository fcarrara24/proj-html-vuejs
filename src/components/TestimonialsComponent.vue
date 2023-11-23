<template>
    <div class=" position-relative w-100">
        <div class=" position-absolute w-100 " style="left: 0px; bottom: 50%; height: auto;">
            <img width="100%" src="img/maxcoach-shape-03.png" alt="">
        </div>
        <div class="d-flex flex-column justify-content-center bg-testimonials">
            <div class="specialItalic text-center ">
                Testimonials
            </div>
            <div class="text-center my-title">
                Why do people love me?
            </div>
            <div class="d-flex flex-row justify-content-center container gap-3 ">
                <div class="userCardContainer" v-for="(card, index ) in userCards">
                    <UserCardComponent :cardSpecifics="card" />
                </div>
            </div>
            <div
                class="elipsis-choise container d-flex flex-row align-items-center justify-content-center gap-4 pt-2 pb-5  ">
                <div class="dot-container" v-for="dotNum in 4">
                    <i class=" fa-circle" :class="(store.indexSelected === dotNum - 1) ? 'fa-solid' : 'fa-regular'"
                        @click="selectImage(dotNum - 1)"></i>
                </div>
            </div>
        </div>

    </div>
</template>

<script>
import UserCardComponent from './UserCardComponent.vue';
import { store } from "../data/store.js"

export default {
    name: "TestimonialsComponent",
    data() {
        return {
            userCards: [
                {
                    index: 0,
                    title: "Professional team of specialists and passionate mentors at reach ",
                    description: "I need to get a certification for English proficiency and MaxCoach is my best choice. Their tutors are smart and professional when dealing with students.\t\t\t\t",
                    user: {
                        name: "Madley Pondor",
                        job: "IT Specialist",
                        imgPosition: "1"
                    }
                },
                {
                    index: 1,
                    title: "The MaxCoach team works really hard to ensure high quality",
                    description: "I am happy with their arrangement of lessons and subjects. They reflect a scientific  investigation into effective methods to be adopted for learners of all levels.\t\t\t\t",
                    user: {
                        name: "Ludvic Dubble",
                        job: "Private Tutor",
                        imgPosition: "2"
                    }
                },
                {
                    index: 2,
                    title: "It's a choice of quality for people with special needs",
                    description: "I'm a very strict person so I require everything to be organized and neat. Then, I'll be able to make things right and shine. MaxCoach guys just got me.",
                    user: {
                        name: "Florence Themes",
                        job: "Multimedia Admin",
                        imgPosition: "3"
                    }
                },
                {
                    index: 3,
                    title: "High level of efficiency and scientific teaching methods",
                    description: "I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from the syllabus. Great study portal for people like me.",
                    user: {
                        name: "Mina Hollance",
                        job: "Freelancer",
                        imgPosition: "4"
                    }
                },
            ],
            store,

        };
    },
    methods: {
        selectImage(number) {
            store.indexSelected = number;
        }
    },
    components: { UserCardComponent }
}
</script>

<style lang="scss" scoped>
@use '../assets/style/main' as *;
@use '../assets/style/partials/variables' as *;

.my-title {
    font-size: 2em;
}

.bg-testimonials {
    background: rgb(255, 255, 255);
    background: linear-gradient(180deg, rgba(255, 255, 255, 1) 0%, rgba(250, 248, 246, 1) 100%);
}


.dot-container {
    height: 20px;
    width: 20px;
}

.dot-container>i {
    width: 100%;
    height: 100%;
}
</style>