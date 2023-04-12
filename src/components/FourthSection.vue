<script>
export default {
    name: 'FourthSection',
    data() {
        return {
            pricingList: [
                {
                    icon: 'fa-solid fa-rocket',
                    title: 'Standard',
                    price: '490',
                    services: [
                        {
                            name: 'Standard Accounting',
                            icon: 'fa-solid fa-check'
                        },
                        {
                            name: 'Standard Accounting',
                            icon: 'fa-solid fa-check'
                        },
                        {
                            name: 'Standard Accounting',
                            icon: 'fa-solid fa-xmark'
                        },
                        {
                            name: 'Standard Accounting',
                            icon: 'fa-solid fa-xmark'
                        },
                        {
                            name: 'Standard Accounting',
                            icon: 'fa-solid fa-xmark'
                        }
                    ]
                },
                {
                    icon: 'fa-solid fa-briefcase',
                    title: 'Professional',
                    price: '890',
                    services: [
                        {
                            name: 'Standard Accounting',
                            icon: 'fa-solid fa-check'
                        },
                        {
                            name: 'Standard Accounting',
                            icon: 'fa-solid fa-check'
                        },
                        {
                            name: 'Standard Accounting',
                            icon: 'fa-solid fa-check'
                        },
                        {
                            name: 'Standard Accounting',
                            icon: 'fa-solid fa-xmark'
                        },
                        {
                            name: 'Standard Accounting',
                            icon: 'fa-solid fa-xmark'
                        }
                    ]
                },
                {
                    icon: 'fa-regular fa-gem',
                    title: 'Ultimate',
                    price: '1.390',
                    services: [
                        {
                            name: 'Standard Accounting',
                            icon: 'fa-solid fa-check'
                        },
                        {
                            name: 'Standard Accounting',
                            icon: 'fa-solid fa-check'
                        },
                        {
                            name: 'Standard Accounting',
                            icon: 'fa-solid fa-check'
                        },
                        {
                            name: 'Standard Accounting',
                            icon: 'fa-solid fa-check'
                        },
                        {
                            name: 'Standard Accounting',
                            icon: 'fa-solid fa-check'
                        }
                    ]
                },

            ],
            servicesIncluded: [
                {
                    name: ''
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
                <div class="col-6 mx-auto text-center my-5">
                    <h6 class="fw-bold ms_color">MONTHLY PLANS</h6>
                    <h1 class="fw-bold my-4">
                        <div class="d-inline-block ms_br_gr py-1 px-2">Pricing</div>
                        Table
                    </h1>
                    <p>We can help you deliver and execute your future, wherever you compete, using the latest
                        technologies, from strategy development to implementation.</p>
                </div>
            </div>
            <div class="row">
                <div class="col-4 bg-white ms_card_width mx-5 p-5" v-for="(element, index) in pricingList" :key="index">
                    <div class="text-center ms_services_top">
                        <i :class="element.icon"></i>
                        <h4 class="my-3 fw-bold">{{ element.title }}</h4>
                        <h3 class="my-3fw-bold">$ <span class="fs-1">{{ element.price }}</span> /mo</h3>
                    </div>
                    <div>
                        <ul class="ms_list_services mb-4">
                            <li v-for="service in element.services" class="d-flex justify-content-between my-4">
                                <h6> {{ service.name }}</h6>
                                <i :class="service.icon"></i>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/general.scss';
@use '../styles/partials/variable' as *;

.ms_card_width {
    width: calc(100% / 3 - 100px);
    border-radius: 10px;
}

.ms_color {
    color: $color-primary;
}

.ms_container {
    height: 1100px;
    background-color: $color-secondary-bg;

    & p {
        color: grey;
    }
}

.ms_br_gr {
    background-color: $color-primary-opacity-2;
    color: $color-primary;
    border-radius: 5px;
}

.ms_services_top {
    & i {
        color: $color-primary;
        font-size: 32px;
    }

    & h3 {
        color: $color-primary;
    }

}

.ms_list_services {
    & h6 {
        color: grey;
    }

    & i {
        color: $color-primary;
    }
}
</style>
