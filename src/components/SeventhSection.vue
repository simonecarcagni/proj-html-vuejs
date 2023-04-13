<script>
export default {
    name: 'SeventhSection',
    data() {
        return {
            exampleList: [
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
            ]
        }
    }
}
</script>

<template>
    <div class="ms_container">
        <div class="container-md">
            <div class="row ms_row_margin">
                <div class="col-7">
                    <h6 class="fw-bold">SEND A MESSAGE</h6>
                    <h1 class="fw-bolder my-4">
                        Get in
                        <div class="d-inline-block ms_br_gr py-1 px-2">Touch</div>
                    </h1>
                    <p class="mb-5">We will respond to your message as soon as possible. </p>
                    <form class="d-flex flex-wrap ms_form gap-2">
                        <div class="position-relative">
                            <input class="form-control form-control-lg " type="text" placeholder="Name"
                                aria-label="formName">
                            <img src="../assets/img/image (1).png" class="position-absolute end-0 top-50 translate-middle">
                        </div>
                        <div>
                            <input class="form-control form-control-lg " type="text" placeholder="Email"
                                aria-label="formEmail">
                        </div>
                        <div>
                            <input class="form-control form-control-lg " type="text" placeholder="Phone"
                                aria-label="formPhone">
                        </div>
                        <div class="position-relative">
                            <input class="form-control form-control-lg " type="text" placeholder="More Info"
                                aria-label="formInfo">
                            <i
                                class="fa-solid fa-chevron-down position-absolute end-0 top-50 translate-middle text-secondary"></i>
                        </div>
                        <div class="w-100">
                            <textarea class="form-control form-control-lg" id="exampleFormControlTextarea1"
                                placeholder="Message" rows="3"></textarea>
                        </div>
                        <button type="button" class="ms_button_gr my-2 text-white">SEND</button>
                    </form>
                </div>
                <div class="col-5">
                    <h4 class="mb-3 fw-bold">Example Inc.</h4>
                    <p class="my-3 w-75">Lorem ipsum dolor sit amet. Consectetur adipiscing elit. Consectetur adipiscing
                        elit.</p>
                    <p class="my-3 w-75">Praesent diam lacus. dapibus sed imperdiet consectetur.</p>
                    <ul class="my-4">
                        <li v-for="(element, index) in exampleList" :key="index" class="my-3">
                            <h6 class="d-flex align-items-center">
                                <div class="ms_icon_container d-flex justify-content-center align-items-center me-3">
                                    <i :class="element.icon"></i>
                                </div>
                                {{ element.text }}
                            </h6>
                        </li>
                    </ul>
                    <button type="button" class="ms_button_gr_invert">VIEW MAP</button>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/general.scss';
@use '../styles/partials/variable' as *;

.ms_container {
    height: 600px;

    & h6 {
        color: $color-primary;
    }

    & p {
        color: $color-text-grey;
        margin: 0;
    }
}

.ms_row_margin {
    margin-top: 150px;
}

.ms_br_gr {
    background-color: $color-primary-opacity-2;
    color: $color-primary;
    border-radius: 5px;
}

.ms_form {
    & div {
        width: calc(100% / 2 - 4px);

        & input {
            background-color: rgba($color: $color-text-grey, $alpha: 0.2);
            border-color: transparent;
            width: 100%;
        }
    }

    & textarea {
        background-color: rgba($color: $color-text-grey, $alpha: 0.2);
        border-color: transparent;
    }
}

.ms_button_gr {
    height: 45px;
    padding: 5px 21px;
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
    color: $color-primary;
    transition: ease 1s;
}

.ms_button_gr_invert:hover {
    background-color: $color-primary;
    border-color: $color-primary;
    color: $color-white;
}

.ms_icon_container {
    height: 40px;
    width: 40px;
    border-radius: 50%;
    background-color: $color-primary-opacity-2;

    & i {
        color: $color-primary;
        font-size: 20px;
    }
}
</style>
