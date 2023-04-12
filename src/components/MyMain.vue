<script>
import FirstSection from './FirstSection.vue';
import SecondSection from './SecondSection.vue';
import ThirdSection from './ThirdSection.vue';
import FourthSection from './FourthSection.vue';
export default {
    components: {
        FirstSection,
        SecondSection,
        ThirdSection,
        FourthSection,
    },
    name: 'MyMain',
    data() {
        return {

        }
    }
}
</script>

<template>
    <FirstSection />
    <SecondSection />
    <ThirdSection />
    <FourthSection />
</template>

<style lang="scss" scoped>
@use '../styles/general.scss';
@use '../styles/partials/variable' as *;
</style>
