<template>
    <div class="main">
        <Content v-if="!profileStat"></Content>
        <Profile @showm="$emit('showm')" v-if="profileStat"></Profile>
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

<style scoped lang="scss">
    .main {
        flex-grow: 1;
        display: flex;
    }
</style>