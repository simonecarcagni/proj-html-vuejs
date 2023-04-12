<script>
import FirstSection from './FirstSection.vue';
import SecondSection from './SecondSection.vue';
import ThirdSection from './ThirdSection.vue';
export default {
    components: {
        FirstSection,
        SecondSection,
        ThirdSection
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
</template>

<style lang="scss" scoped>
@use '../styles/general.scss';
@use '../styles/partials/variable' as *;
</style>
