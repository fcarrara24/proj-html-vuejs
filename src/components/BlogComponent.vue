<template>
    <div
        class="bg-blog d-flex flex-column justify-content-center align-items-center blog-background py-3 position-relative ">
        <img src="/img/public/img/maxcoach-shape-14-1536x343.png" alt="" class=" position-absolute img-back w-100">
        <div class="specialItalic">
            Articels and Tips
        </div>
        <div class="blog-title">
            Latest From The Blog
        </div>
        <div class="d-flex flex-row justify-content-center card-container position-relative ">
            <!-- I'll create this card locally so I can Manage Better the propierties -->
            <div class="" v-for="card in blogCards">
                <!-- spacekeepercomponent will sllow card to be on different height levels -->
                <div class="spaceKeeper" :style="`height:${card.top}px;`"></div>
                <div :class="card.bigCard ? 'cardBig' : 'cardSmall'" class="bg-white m-3 shadow">
                    <div class="d-flex flex-column justify-content-end">
                        <div class="image-container">
                            <img class="img-hoverable" :src="card.backGroundImg" :alt="card.title">
                        </div>
                        <div class="card-description p-1" :class="card.bigCard ? 'position-absolute p-4 text-white' : ''">
                            <div class="role-text">{{ card.role }}</div>
                            <div class="BlogCardtitle">{{ card.title }}</div>
                            <span class="role-text"><i class="fa-regular fa-calendar"></i> {{ card.date }} &nbsp;</span>
                            <span class="role-text"><i class="fa-regular fa-eye"></i> {{ card.views }} &nbsp;</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="blogbottom d-flex flex-row justify-content-center pt-5">
            <div>Get into details now? </div>
            <div class="text-orange">&nbsp;View all posts <i class="fa-solid fa-arrow-right"></i></div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'BlogComponent',
    data() {


        return {
            blogCards: [
                {
                    title: 'Brush Strokes Energize Trees in Painting',
                    role: 'ARTIST',
                    selected: false,
                    date: 'May 15, 2020',
                    views: 688,
                    bigCard: false,
                    top: 100,
                    //full link src/assets/img/artist-blog-1.jpg
                    backGroundImg: '/img/artist-blog-1.jpg',
                },
                {
                    title: 'Connection Between Self-POrtraits and Identity',
                    role: 'ARTIST',
                    selected: true,
                    date: 'May 15, 2020',
                    views: 307,
                    bigCard: true,
                    top: 0,
                    backGroundImg: '/img/artist-blog-2.jpg',
                },
                {
                    title: 'Pocket-Sized Notebooks Hold Miniature paintings',
                    role: 'ARTIST',
                    selected: false,
                    date: 'May 15, 2020',
                    views: 603,
                    bigCard: false,
                    top: 200,
                    backGroundImg: '/img/artist-blog-3.jpg',
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
.role-text {
    font-size: 0.7em;
}

.blog-background {
    background: rgb(255, 255, 255);
    background: linear-gradient(180deg, rgba(255, 255, 255, 1) 0%, rgba(245, 247, 250, 1) 10%, rgba(245, 247, 250, 1) 90%, rgba(255, 255, 255, 1) 100%);
}

.blog-title {
    font-size: 1.5em;
    font-weight: bolder;
}

.image-container {
    width: 100%;
    height: auto;
}

.card-container {
    max-width: 1200px;

}

.BlogCardtitle {
    font-size: 1em;
    font-weight: bolder;
    text-overflow: clip;
}

.cardBig {
    max-width: 400px;
    height: auto;
}

.img-back {
    top: 50%;
    left: 0%;
    z-index: 100;
}

.cardSmall {
    max-width: 200px;
    height: auto;
}

.image-container {
    max-width: 100%;
}

img {
    max-width: 100%;
}</style>