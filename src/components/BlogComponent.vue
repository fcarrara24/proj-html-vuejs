<template>
    <div class="bg-blog d-flex flex-column justify-content-center align-items-center ">
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
                <div :class="card.bigCard ? 'cardBig' : 'cardSmall'">
                    <div class="d-flex flex-column justify-content-end p-2">
                        <div class="image-container">
                            <img :src="card.backGroundImg" :alt="card.title">
                        </div>
                        <div class="card-description">
                            <div>{{ card.role }}</div>
                            <div class="BlogCardtitle">{{ card.title }}</div>
                            <span><i class="fa-regular fa-calendar"></i> {{ card.date }} &nbsp;</span>
                            <span><i class="fa-regular fa-eye"></i> {{ card.views }} &nbsp;</span>
                        </div>
                    </div>
                </div>
            </div>
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

.cardBig {
    max-width: 400px;
    height: auto;
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
}
</style>