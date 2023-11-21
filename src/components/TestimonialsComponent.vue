<template>
    <div>
        <div class="d-flex flex-column justify-content-center">
            <div class="specialItalic text-center ">
                Testimonials
            </div>
            <div class="text-center my-title">
                Why do people love me?
            </div>
            <div class="d-flex flex-row justify-content-center container gap-3 ">
                <div class="userCardContainer" v-for="(card, index) in userCards">
                    <UserCardComponent :cardSpecifics="card" :selected="index === 1" :ignored="index === 3" />
                </div>
            </div>
            <i class="fa-solid fa-ellipsis text-center"></i>

        </div>

    </div>
</template>

<script>
import UserCardComponent from './UserCardComponent.vue';

export default {
    name: "TestimonialsComponent",
    data() {
        return {
            userCards: [
                {
                    title: "Professional team of specialists and passionate mentors at reach ",
                    description: "I need to get a certification for English proficiency and MaxCoach is my best choice. Their tutors are smart and professional when dealing with students.\t\t\t\t",
                    user: {
                        name: "Madley Pondor",
                        job: "IT Specialist",
                        imgPosition: "1"
                    }
                },
                {
                    title: "The MaxCoach team works really hard to ensure high quality",
                    description: "I am happy with their arrangement of lessons and subjects. They reflect a scientific  investigation into effective methods to be adopted for learners of all levels.\t\t\t\t",
                    user: {
                        name: "Ludvic Dubble",
                        job: "Private Tutor",
                        imgPosition: "2"
                    }
                },
                {
                    title: "It's a choice of quality for people with special needs",
                    description: "I'm a very strict person so I require everything to be organized and neat. Then, I'll be able to make things right and shine. MaxCoach guys just got me.",
                    user: {
                        name: "Florence Themes",
                        job: "Multimedia Admin",
                        imgPosition: "3"
                    }
                },
                {
                    title: "High level of efficiency and scientific teaching methods",
                    description: "I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from the syllabus. Great study portal for people like me.",
                    user: {
                        name: "Mina Hollance",
                        job: "Freelancer",
                        imgPosition: "4"
                    }
                },
            ],
        };
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
</style>