<script>
export default {
    name: 'PostFooter',
    data() {
        return {

        }
    }
}
</script>

<template>
    <div class="ms_container d-flex align-items-center">
        <div class="container d-flex justify-content-between align-items-center h-100   ">
            <p class="text-white-50">Enjoy the low price. We are tracking any intention of piracy.</p>
            <p class="text-white-50">© 2020 NEXGEN is Proudly Powered by <span>Codings</span>.</p>
        </div>
        <div class="ms_icon_container d-flex justify-content-center align-items-center me-3 ">
            <i class="fa-solid fa-arrow-up"></i>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/general.scss';
@use '../styles/partials/variable' as *;

.ms_container {
    height: 100px;
    background-color: black;

    & p {
        margin: 0;
    }

    & span {
        color: $color-primary;
    }
}

.ms_icon_container {
    height: 40px;
    width: 40px;
    border-radius: 50%;
    background-color: $color-bg-card-dark;

    & i {
        color: $color-primary-bg;
        font-size: 20px;
    }
}
</style>