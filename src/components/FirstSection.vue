<script>
export default {
    name: 'FirstSection',
    data() {
        return {
            cardListSectionFirst: [
                {
                    icon: 'fa-solid fa-users',
                    title: 'Human Capital',
                    paragraph: 'Humanizing business: Harness the power of technology to improve the way people work.'
                },
                {
                    icon: 'fa-solid fa-chart-pie',
                    title: 'Core Business',
                    paragraph: 'It takes innovative approaches to transform, modernize, and run existing platforms.'
                },
                {
                    icon: 'fa-solid fa-gauge-high',
                    title: 'Performance',
                    paragraph: 'Achieving maximum impact and value from investments in finance and supply chain.'
                }
            ]
        }
    }
}
</script>

<template>
    <div class="ms_container">
        <div class="container h-100">
            <div class="row d-flex justify-content-around align-items-center h-100">
                <div class="col-3" v-for="(card, index) in cardListSectionFirst" :key="index">
                    <div class="card p-3 ms_card_border">
                        <div class="card-body">
                            <div class="ms_icon_container d-flex justify-content-center align-items-center">
                                <i :class="card.icon"></i>
                            </div>
                            <h5 class="card-title fw-bold my-3">{{ card.title }}</h5>
                            <p class="card-text">{{ card.paragraph }}</p>
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
    height: 500px;
    background-color: $color-secondary-bg;
}

.ms_card_border {
    width: 18rem;
    height: 16rem;
    border-color: $color-white;
    transition: ease 1s;
}

.ms_card_border:hover {
    transform: scale(1.2);
}

.ms_icon_container {
    height: 50px;
    width: 50px;
    border-radius: 50%;
    background-color: $color-primary-opacity-2;

    & i {
        color: $color-primary;
        font-size: 24px;
    }
}

p {
    color: $color-text-grey;
}
</style>