<script>
export default {
    name: 'ThirdSection',
    data() {
        return {
            cardListSectionThird: [
                {
                    icon: 'fa-solid fa-network-wired',
                    title: 'Audit & Assurance',
                    paragraph: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit.'
                },
                {
                    icon: 'fa-solid fa-briefcase',
                    title: 'Financial Advisory',
                    paragraph: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit.'
                },
                {
                    icon: 'fa-solid fa-chart-simple',
                    title: 'Analytics and M&A',
                    paragraph: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit.'
                },
                {
                    icon: 'fa-solid fa-plane-departure',
                    title: 'Middle Marketing',
                    paragraph: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit.'
                },
                {
                    icon: 'fa-solid fa-globe',
                    title: 'Legal Colsunting',
                    paragraph: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit.'
                },
                {
                    icon: 'fa-solid fa-inbox',
                    title: 'Regulatory Risk',
                    paragraph: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit.'
                }
            ]
        }
    }
}
</script>

<template>
    <div class="ms_container">
        <div class="container">
            <div class="row pt-5">
                <div class="col-12 mt-5">
                    <h6 class="fw-bold">OURS BUSINESS AREA</h6>
                    <h1 class="fw-bolder my-4 text-white">
                        Excellence in
                        <div class="d-inline-block ms_br_gr py-1 px-2">Services</div>
                    </h1>
                </div>
                <div class="row d-flex justify-content-between">
                    <div class="col-7">
                        <p class="mb-5">
                            We are leaders in providing consultancy services with a set of cutting-edge
                            technologiesand a team of and renowned professionals. These are some options that you can hire.
                        </p>
                    </div>
                    <div class="col-2 d-flex justify-content-end">
                        <button type="button" class="ms_button_gr_invert mx-2 text-white">SEE ALL</button>
                    </div>
                </div>
            </div>
            <div class="d-flex justify-content-between align-items-center flex-wrap">
                <div class="d-flex ms_card_gap" v-for="(card, index) in cardListSectionThird" :key="index">
                    <div class="card p-4 ms_card_bg ">
                        <div class="card-body ">
                            <div class="ms_card_icon">
                                <i :class="card.icon"></i>
                            </div>
                            <h5 class="card-title fw-bold my-3 text-white">{{ card.title }}</h5>
                            <p class="card-text">{{ card.paragraph }}</p>
                            <button type="button" class="ms_button_gr_invert text-white">READ MORE</button>
                        </div>
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
    height: 1100px;
    background-color: $color-primary-bg;

    & h6 {
        color: $color-primary;
    }

    & p {
        color: $color-text-1;
    }
}

.ms_card_gap {
    height: 300px;
    width: calc(100% / 3 - 50px);
    margin: 15px 0px;
    transition: ease 1s;
}

.ms_card_gap:hover {
    transform: scale(1.1);

    & i {
        color: $color-white;
    }

    & p {
        color: $color-white;
    }
}

.ms_card_bg {
    background-color: $color-bg-card-dark;
}

.ms_card_icon {
    height: 35px;
    width: 35px;

    & i {
        color: $color-primary;
        font-size: 32px;
    }
}

.ms_button_gr_invert {
    height: 45px;
    padding: 5px 21px;
    background-color: transparent;
    border-color: $color-primary;
    border-radius: 5px;
    transition: ease 1s;
}

.ms_button_gr_invert:hover {
    background-color: $color-primary;
    border-color: $color-primary;
}

.ms_br_gr {
    background-color: $color-primary-opacity-2;
    border-radius: 5px;
}
</style>
