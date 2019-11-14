<template>
    <div class="resume-page">
        <h1 id="resume-title"> Resume </h1>
        <ResumeContainer />
    </div>

</template>

<script>

import ResumeContainer from '@/components/ResumeContainer.vue'

export default {
    name: 'resume',
    components: {
        ResumeContainer
    }
}

</script>

<style scoped lang="scss">

    .resume-page {
        // background-color: #F7882F;
        // color: #DCC7AA
        background-color: #6B7A8F;
        color: #DCC7AA;
    }

    #resume-title{
        font-size: 40pt;
        margin-top: 0;
        padding-top: 2rem;
    }

</style>