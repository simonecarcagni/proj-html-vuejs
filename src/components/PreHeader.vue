<script>
export default {
    name: 'PreHeader',
    data() {
        return {
            preHeaderListIcon: [
                {
                    icon: 'fa-solid fa-phone',
                    text: '+1 (305) 1234-5678'
                },
                {
                    icon: 'fa-solid fa-envelope',
                    text: 'hello@example.com'
                },
                {
                    icon: 'fa-brands fa-facebook-f',
                },
                {
                    icon: 'fa-brands fa-twitter',
                },
                {
                    icon: 'fa-brands fa-linkedin',
                },
            ]
        }
    }
}
</script>

<template>
    <div class="ms_bg">
        <div class="container h-100">
            <div class="row d-flex justify-content-between h-100">
                <div class="col-3 d-flex align-items-center h-100">
                    <h6> <i class="fa-solid fa-clock"></i> Open Hours: Mon - Sat - 9:00 - 18:00</h6>
                </div>
                <div class="col-6 d-flex align-items-center justify-content-end">
                    <ul class="d-flex">
                        <li class="mx-3 d-flex align-items-center" v-for="(element, index) in preHeaderListIcon"
                            :key="index">
                            <i :class="element.icon" class="mx-2"></i>
                            <h6>{{ element.text }}</h6>
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

.ms_bg {
    height: 50px;
    background-color: $color-header-bg;

    & i {
        color: $color-text-1;
    }
}

h6 {
    color: $color-text-1;
    margin: 0;
}
</style>
