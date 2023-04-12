<script>
export default {
    name: 'PreHeader',
    data() {
        return {

        }
    }
}
</script>

<template>
    <div class="ms_bg">
        <div class="container h-100">
            <div class="row d-flex justify-content-between h-100">
                <div class="col-3 d-flex align-items-center h-100">
                    <h6 class=""> <i class="fa-solid fa-clock"></i> Open Hours: Mon - Sat - 9:00 - 18:00</h6>
                </div>
                <div class="col-5 d-flex align-items-center justify-content-end">
                    <ul class="d-flex">
                        <li class="mx-3">
                            <h6><i class="fa-solid fa-phone"></i>+1 (305) 1234-5678</h6>
                        </li>
                        <li class="mx-3">
                            <h6><i class="fa-solid fa-envelope"></i>hello@example.com</h6>
                        </li>
                        <li class="mx-3">
                            <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
                        </li>
                        <li class="mx-3">
                            <a href="#"><i class="fa-brands fa-twitter"></i></a>
                        </li>
                        <li class="mx-3">
                            <a href="#" class="text-secondary-emphasis"><i class="fa-brands fa-linkedin "></i></a>
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
}

h6 {
    color: $color-text-1;
}

a {
    color: $color-text-1;
}
</style>
