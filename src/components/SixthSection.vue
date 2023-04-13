<script>
export default {
    name: 'SixthSection',
    data() {
        return {

        }
    }
}
</script>

<template>
    <div class="ms_container overflow-y-hidden position-relative">
        <img src="../assets/img/bg-1.jpg">
        <div class="container-sm position-absolute start-50 top-50 d-flex translate-middle">
            <div class="ms_width_box mx-auto">
                <div class="row">
                    <div class="col-6">
                        <h6 class="fw-bold">NEWS LETTER</h6>
                        <h1 class="fw-bolder my-4 text-white">
                            <div class="d-inline-block ms_br_gr py-1 px-2">Know</div>
                            First
                        </h1>
                        <p class="mb-5">Follow closely and receive content about our company
                            and the news of the current market.
                        </p>
                    </div>
                    <div class="col-6">
                        <input class="form-control form-control-lg my-2" type="text" placeholder="Name"
                            aria-label="formName">
                        <input class="form-control form-control-lg my-2" type="text" placeholder="Email"
                            aria-label="formEmail">
                        <button type="button" class="ms_button_gr my-2 text-white">SUBSCRIBE</button>
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

    & img {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
}

.ms_width_box {

    & h6 {
        color: $color-primary;
    }

    & p {
        color: $color-text-1;
    }

    & input {
        background-color: rgba($color: $color-white, $alpha: 0.5);
        border-color: transparent;
    }
}

.ms_br_gr {
    background-color: $color-primary-opacity-2;
    border-radius: 5px;
}

.ms_button_gr {
    height: 45px;
    padding: 5px 21px;
    background-color: $color-primary;
    border-color: $color-primary;
    border-radius: 5px;
}
</style>
