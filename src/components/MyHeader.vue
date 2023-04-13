<script>
export default {
    name: 'MyHeader',
    data() {
        return {
            headerLinkList: [
                {
                    name: 'HOME',
                    path: '#home',
                },
                {
                    name: 'ABOUT',
                    path: '#about',
                },
                {
                    name: 'SERVICES',
                    path: '#services',
                },
                {
                    name: 'PRICING',
                    path: '#pricing',
                },
                {
                    name: 'BLOG',
                    path: '#blog',
                },
            ]
        }
    }
}
</script>

<template>
    <div class="ms_jumbotron position-relative">
        <div class="ms_overlay h-100 w-100 ">
        </div>
        <div class="container">
            <div class="row d-flex justify-content-between py-3 px-4 position-absolute top-0 start-50translate-middle w-75">
                <div class="col-4">
                    <div class="ms_header_title d-flex">
                        <h6 class="ms_borded_title ps-3 py-1 pe-1">N E X</h6>
                        <h6 class="mx-1 py-1">G E N</h6>
                    </div>
                </div>
                <div class="col-6 d-flex justify-content-end ms_margin_right">
                    <ul class="d-flex align-items-center">
                        <li v-for="(link, index) in headerLinkList" :key="index" class="mx-2 mt-1">
                            {{ link.name }}</li>
                        <li class="mx-2 mt-1">
                            <button type="button" class="ms_button_gr text-white">GET IN TOUCH</button>
                        </li>
                    </ul>
                </div>
            </div>
            <div
                class="row d-flex justify-content-center align-items-center position-absolute top-50 start-50 translate-middle">
                <div class="col-12">
                    <h1 class="text-white fw-bold text-center">Lead ~ <span>Customer</span></h1>
                </div>
                <div class="col-8">
                    <p class="text-center">Successful strategies require data analysis, creativity and customer focus,
                        taking advantage of the Iatest technologies to offer excellent services.</p>
                </div>
                <div class="col-12 d-flex justify-content-center">
                    <button type="button" class="ms_button_gr mx-2 text-white">GET IN TOUCH</button>
                    <button type="button" class="ms_button_gr_invert mx-2 text-white">READ MORE</button>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/general.scss';
@use '../styles/partials/variable' as *;

.ms_jumbotron {
    height: 910px;
    width: 100%;
    background-image: url(../assets/img/hero-image.png);
    background-repeat: no-repeat;
    background-position: top;
    background-size: cover;

    & .ms_overlay {
        background-color: $color-black;
        opacity: 0.7;
    }
}

.ms_margin_right {
    margin-right: 7rem;

    & li {
        color: $color-text-1;
    }
}

.ms_header_title {

    & h6 {
        height: 32px;
        font-weight: bold;
        font-size: 20px;
    }

    & .ms_borded_title {
        background-color: $color-primary-opacity-1;
        border-radius: 50px 0px 0px 50px;
        color: $color-primary;
    }

    & :last-child {
        color: $color-text-1;
    }
}





.ms_button_gr {
    padding: 5px 15px;
    background-color: $color-primary;
    border-color: $color-primary;
    border-radius: 5px;
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

p {
    color: $color-text-1;
}

h1 {
    font-size: 60px;
}
</style>
