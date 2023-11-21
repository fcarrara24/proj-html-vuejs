<template>
    <div class="outerTimer w-100 d-flex justify-content-center ">
        <div class=" w-75  d-flex flex-row justify-content-center align-items-center gap-3 py-1 px-3  ">
            <div class="timerDescription">Starts TOMORROW! Our biggest event of the year...</div>
            <div class="timerClock d-flex flex-row justify-content-center gap-1 align-items-center  ">
                <i class="fa-regular fa-clock"></i>
                <div>
                    {{ getDays }}
                    :
                </div>
                <div>
                    {{ String(getHours).padStart(2, '0') }}
                    :
                </div>
                <div>
                    {{ String(getMinutes).padStart(2, '0') }}
                    :
                </div>
                <div>
                    {{ String(getSeconds).padStart(2, '0') }}
                </div>

            </div>
            <div class="timerButton btn my-btn-orange text-white ">Get Ticket</div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'TimerComponent',
    data() {
        return {
            time: 0,

        }
    },
    methods: {

    },
    created() {
        const timeInterval = setInterval(() => {
            this.time++
        }, 1000);
    },
    computed: {
        getSeconds() {
            return (this.time) % 60
        },
        getMinutes() {
            return (Math.floor(this.time / 60)) % 60
        },
        getHours() {
            return (Math.floor(this.time / 3600)) % 24
        },
        getDays() {
            return (Math.floor(this.time / 86400))
        }
    }

}
</script>

<style lang="scss" scoped>
@use '../assets/style/main' as *;
@use '../assets/style/partials/variables' as *;

.outerTimer {
    background-color: $backgroundgray;
}

.timerDescription {
    font-size: 0.7em;
}
</style>