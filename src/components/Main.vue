<template>
    <div class="main">
        <Content v-if="!profileStat"></Content>
        <Profile v-if="profileStat"></Profile>
    </div>
</template>

<script>

    import Content from "./Content";
    import Profile from "./Profile";

    export default {
        name: "Main",
        props: ['profileStat'],
        components: {
            Content,
            Profile
        }
    }
</script>

<style scoped>
    .main {
        flex-grow: 1;
        display: flex;
    }
</style>