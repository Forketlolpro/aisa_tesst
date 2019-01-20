<template>
    <div class="content">
        <div class="content-elem"></div>
        <div class="content-elem"></div>
        <div class="content-elem"></div>
        <div class="content-elem"></div>
        <div class="content-elem"></div>
        <div class="content-elem"></div>
    </div>
</template>

<script>
    export default {
        name: "Content"
    }
</script>

<style scoped>
    .content {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
        align-items: center;
    }

    .content-elem {
        border: 1px solid black;
        width: 360px;
        height: 160px;
    }
</style>