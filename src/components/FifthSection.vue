<script>
export default {
    name: 'FifthSection',
    data() {
        return {
            cardImgContent: [
                {
                    title: 'Increasing creativity is possible for everyone',
                    src: 'news-1'
                },
                {
                    title: 'Because market reserch is part  of the business plan',
                    src: 'news-2'
                },
                {
                    title: 'Working from home is now a trend',
                    src: 'news-3'
                }
            ]
        }
    },
    methods: {
        getImagePath(path) {
            return new URL(path, import.meta.url).href
        }
    }
}
</script>

<template>
    <div class="ms_container">
        <div class="container-lg">
            <div class="row pt-5">
                <div class="col-12 mt-5">
                    <h6 class="fw-bold">OURS EDITORIAL CONTENT</h6>
                    <h1 class="fw-bolder my-4">
                        Latest
                        <div class="d-inline-block ms_br_gr py-1 px-2">News</div>
                    </h1>
                </div>
                <div class="row d-flex justify-content-between mb-5">
                    <div class="col-7 d-flex align-items-center">
                        <p class="">Every week we publish content about what is best in the business world.</p>
                    </div>
                    <div class="col-2 d-flex justify-content-end">
                        <button type="button" class="ms_button_gr mx-2">SEE ALL</button>
                    </div>
                </div>
            </div>
            <div class="row d-flex justify-content-between ">
                <div class="col-3" v-for="(card, index) in cardImgContent" :key="index">
                    <div class="card ms_img_card position-relative" style="width: 18rem;">
                        <img :src="getImagePath(`../assets/img/${card.src}.jpg`)" class="card-img-top" alt="Girl-1">
                        <h5 class="text-center text-white position-absolute w-75 top-100 start-50 translate-middle">
                            {{ card.title }}
                        </h5>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/general.scss';
@use '../styles/partials/variable' as *;

.ms_container {
    height: 700px;

    & h6 {
        color: $color-primary;
    }

    & p {
        color: grey;
        margin: 0;
    }
}

.ms_br_gr {
    background-color: $color-primary-opacity-2;
    color: $color-primary;
    border-radius: 5px;
}

.ms_button_gr {
    height: 45px;
    padding: 5px 21px;
    background-color: $color-primary;
    border-color: $color-primary;
    border-radius: 5px;
    color: white;
}

.ms_img_card {
    border-color: transparent;

    & img {
        border-radius: 10px;
        filter: contrast(45%);
    }

    & h5 {
        padding-bottom: 150px;
    }
}
</style>
