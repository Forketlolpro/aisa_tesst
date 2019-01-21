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

<style scoped lang="scss">
    .content {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
        align-items: center;
    }

    .content-elem {
        border: 1px solid black;
        min-width: 320px;
        height: 140px;
        box-sizing: border-box;

        @media screen and (max-width: 768px){
            margin-bottom: 10px;
        }
    }
</style>