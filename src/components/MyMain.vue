<template>
    <main>
        <SectionCompany/>
        <SectionServices/>
        <SectionManagement/>
        <SectionTeam/>
    </main>
</template>

<script>
import SectionCompany from './MainSections/SectionCompany.vue';
import SectionServices from './MainSections/SectionServices.vue';
import SectionManagement from './MainSections/SectionManagement.vue';
import SectionTeam from './MainSections/SectionTeam.vue';


export default {
    name: 'MyMain',
    components: {
        SectionCompany,
        SectionServices,
        SectionManagement,
        SectionTeam
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
        color: grey;
    }
</style>