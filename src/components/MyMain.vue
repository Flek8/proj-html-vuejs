<template>
    <main>
        <SectionCompany/>
        <SectionServices/>
    </main>
</template>

<script>
import SectionCompany from './MainSections/SectionCompany.vue';
import SectionServices from './MainSections/SectionServices.vue'

export default {
    name: 'MyMain',
    components: {
        SectionCompany,
        SectionServices
    }
}
</script>

<style lang='scss'>
    h5 {
        color: #048383;
    }

    h3 {
        margin: 15px 0;
    }

    h2 {
        margin: 15px 0;
        font-size: 50px;
    }

    p {
        margin-bottom: 15px;
        font-size: 16px;
    }
</style>