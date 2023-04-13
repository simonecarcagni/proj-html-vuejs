<script>
export default {
    name: 'MyFooter',
    data() {
        return {
            footerTouchList: [
                {
                    icon: 'fa-solid fa-phone',
                    text: '+1 (305) 1234-5678'
                },
                {
                    icon: 'fa-solid fa-envelope',
                    text: 'hello@example.com'
                },
                {
                    icon: 'fa-solid fa-location-dot',
                    text: 'Main Avenue, 987'
                },
            ],
            footerCardList: [
                {
                    title: 'About',
                    footerItemList: [
                        {
                            name: 'The Company'
                        },
                        {
                            name: 'Institutional'
                        },
                        {
                            name: 'Social & Events'
                        },
                        {
                            name: 'Innovation'
                        },
                        {
                            name: 'Environment'
                        },
                        {
                            name: 'Technology'
                        }
                    ]
                },
                {
                    title: 'Services',
                    footerItemList: [
                        {
                            name: 'Audit & Assurance'
                        },
                        {
                            name: 'Financial Advisory'
                        },
                        {
                            name: 'Analytics M&A'
                        },
                        {
                            name: 'Middle Marketing'
                        },
                        {
                            name: 'Legal Consulting'
                        },
                        {
                            name: 'Regulatory Risk'
                        }
                    ]
                },
                {
                    title: 'Support',
                    footerItemList: [
                        {
                            name: 'Responsibility'
                        },
                        {
                            name: 'Terms of Use'
                        },
                        {
                            name: 'About Cookies'
                        },
                        {
                            name: 'Privacy policy'
                        },
                        {
                            name: 'Accessibility'
                        },
                        {
                            name: 'Information'
                        }
                    ]
                }
            ]
        }
    }
}
</script>

<template>
    <div class="ms_container">
        <div class="container">
            <div class="row d-flex gap-5 ms_padding_top">
                <div class="col-3">
                    <div class="ms_header_title d-flex">
                        <h6 class="ms_borded_title ps-3 py-1 pe-1">N E X</h6>
                        <h6 class="mx-1 py-1">G E N</h6>
                    </div>
                    <p class="my-3 text-white-50">A Functional HTML Template for & Business</p>
                    <ul class="my-4">
                        <li v-for="(element, index) in footerTouchList" :key="index" class="my-3">
                            <h6 class="d-flex align-items-center text-white-50 my-3">
                                <div class="ms_icon_container d-flex justify-content-center align-items-center me-3 ms-1">
                                    <i :class="element.icon"></i>
                                </div>
                                {{ element.text }}
                            </h6>
                        </li>
                    </ul>
                    <button type="button" class="ms_button_gr_invert">GET IN TOUCH</button>
                </div>
                <div class="ms_col_footer" v-for="(card, index) in footerCardList" :key="index">
                    <h4 class="text-white mb-3">{{ card.title }}</h4>
                    <ul>
                        <li class="d-flex justify" v-for="(element, index) in card.footerItemList" :key="index">
                            <h6 class="d-flex align-items-center text-white-50">
                                <div class="ms_icon_container d-flex justify-content-center align-items-center me-3">
                                    <i class="fa-solid fa-chevron-right"></i>
                                </div>
                                {{ element.name }}
                            </h6>
                        </li>
                    </ul>
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
    background-color: $color-primary-bg;
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

.ms_button_gr_invert {
    height: 45px;
    padding: 5px 21px;
    background-color: transparent;
    border-color: $color-primary;
    border-radius: 5px;
    color: $color-primary;
}

.ms_icon_container {
    height: 10px;
    width: 10px;
}

.ms_col_footer {
    width: 230px;
    background-color: $color-bg-card-dark;
    padding: 25px 35px;
    border-radius: 5px;
}

.ms_padding_top {
    padding-top: 200px;
}
</style>
