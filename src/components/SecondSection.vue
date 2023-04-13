<script>
export default {
    name: 'SecondSection',
    data() {
        return {
            boxCardList: [
                {
                    icon: 'fa-solid fa-ranking-star',
                    title: 'Tradition',
                    paragrafh: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit.'
                },
                {
                    icon: 'fa-solid fa-lock',
                    title: 'Security',
                    paragrafh: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit.'
                },
                {
                    icon: 'fa-regular fa-pen-to-square',
                    title: 'Certificate',
                    paragrafh: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit.'
                },
                {
                    icon: 'fa-solid fa-graduation-cap',
                    title: 'Expertise',
                    paragrafh: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit.'
                }
            ]
        }
    }
}
</script>

<template>
    <div class="d-flex position-relative">
        <div class="d-flex ms_dots_container flex-wrap position-absolute top-0 start-50 translate-middle">
            <div v-for="i in 36" :key="i" class="ms_dotted">
            </div>
        </div>
        <div class="d-flex ms_dots_container flex-wrap position-absolute top-100 start-50 translate-middle">
            <div v-for="i in 36" :key="i" class="ms_dotted">
            </div>
        </div>
        <div class="ms_box d-flex justify-content-end align-items-center">
            <div class="ms_width_box">
                <h6 class="fw-bold">ABOUT THE NETWORK</h6>
                <h1 class="fw-bolder my-4">
                    <div class="d-inline-block ms_br_gr py-1 px-2">The</div>
                    Company
                </h1>
                <p class="mb-5">For 12 years we have been providing audit and warranty, financial
                    advicer risk advice, taxes and related services to select clients.
                </p>
                <div class="row ">
                    <div class="col-6 my-3" v-for="(card, index) in boxCardList" :key="index">
                        <h4 class="fw-bold mb-4">
                            <i :class="card.icon"></i>
                            {{ card.title }}
                        </h4>
                        <p>{{ card.paragrafh }}</p>
                    </div>
                </div>

            </div>
        </div>
        <div class="ms_box">
            <img src="../assets/img/about-3.jpg" alt="">
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/general.scss';
@use '../styles/partials/variable' as *;

.ms_box {
    height: 900px;
    width: calc(100% / 2);

    & img {
        height: 100%;
        width: 100%;
    }
}

.ms_width_box {
    margin-right: 150px;
    width: 500px;

    & h6 {
        color: $color-primary;
    }

    & i {
        color: $color-primary;
    }

    & p {
        color: $color-text-1;
    }
}

.ms_br_gr {
    background-color: $color-primary-opacity-2;
    color: $color-primary;
    border-radius: 5px;
}

.ms_img_container {
    height: 500px;
}

.ms_dots_container {
    width: 100px;
    height: 50px;
}

.ms_dotted {
    height: 5px;
    width: 5px;
    background-color: $color-primary-opacity-1;
    border-radius: 50%;
    margin: 3px;
}
</style>
