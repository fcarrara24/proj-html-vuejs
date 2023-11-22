<template>
    <div
        class="contactComponent d-flex flex-row align-items-center justify-content-center backgroundColor position-relative">
        <div class="absolute-image-container position-absolute top-0 left">

            <img src="/img/artist-shape-color-paint-top-left.png" alt="">
        </div>
        <div class="getContactTitle text-end elegantTitle z-hight pe-4 ">
            Newsletter to get in touch
        </div>
        <div class="inputWidth bottomLine d-flex flex-row justify-content-between align-items-center pb-1">
            <input type="text" class="textInput">
            <i class="fa-solid fa-arrow-right arrowContact"></i>
        </div>
        <div class="absolute-image-container position-absolute right">
            <img src="/img/artist-shape-color-paint-bottom-right.png" alt="">
        </div>
    </div>
</template>

<script>
export default {
    name: 'getContactComponent',
    data() {
        return {

        }
    }
}
</script>

<style lang="scss" scoped>
.contactComponent {
    overflow-y: hidden;
}

.backgroundColor {
    background-color: #244186;
    height: 200px;
}

.textInput {
    outline: none;
    border: 0;
    background-color: transparent;
    color: white;
    font-size: 1.2em;
}

.getContactTitle {
    font-size: 2em;
    font-weight: 600;
    color: white;
}

.arrowContact {
    color: white;
}

.inputWidth {
    width: 300px;
}

.bottomLine {
    border-bottom: 1px solid gray;
}

.absolute-image-container {
    height: 100%;
    top: 0;
    z-index: 0;
}

.z-hight {
    z-index: 1000;
}

.left {
    left: 0px;
    bottom: 0px;
}

.right {
    top: 20%;
    right: 0;
}
</style>