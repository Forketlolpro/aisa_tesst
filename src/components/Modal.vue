<template>
    <transition name="modal">
        <div class="modal-mask">
            <div class="modal-wrapper">
                <div class="modal-container">

                    <div class="modal-header">
                        <div name="header">
                            MODAL WINDOW WITH SORT
                        </div>
                        <button class="modal-default-button" @click="$emit('close')">
                            &#10006;
                        </button>
                    </div>

                    <div class="modal-body">
                        <div class="category-wrapper">
                            <div class="category">CATEGORY 1</div>
                            <div class="category">CATEGORY 2</div>
                            <div class="category">CATEGORY 3</div>
                            <div class="category">CATEGORY 4</div>
                        </div>
                        <div class="rectangle-wrapper">
                            <div class="rectangle"></div>
                            <div class="rectangle"></div>
                            <div class="rectangle"></div>
                            <div class="rectangle"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </transition>
</template>

<script>
    export default {
        name: "Modal"
    }
</script>

<style scoped lang="scss">
    .category-wrapper {
        display: flex;
        flex-wrap: nowrap;
        justify-content: space-around;

        @media screen and (max-width: 768px) {
            flex-wrap: wrap;
        }

        .category {
            border: 1px solid black;
            width: 140px;
        }
    }

    .rectangle-wrapper {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
        height: 400px;
        align-items: center;
        .rectangle {
            width: 300px;
            height: 90px;
            border: 1px solid black;
        }
    }

    .modal-header {
        display: flex;
        justify-content: space-between;
    }
    .modal-mask {
        position: fixed;
        z-index: 9998;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, .5);
        display: table;
        transition: opacity .3s ease;
    }

    .modal-wrapper {
        display: table-cell;
        vertical-align: middle;
    }

    .modal-container {
        width: 760px;
        margin: 0px auto;
        padding: 20px 30px;
        background-color: #fff;
        border-radius: 2px;
        box-shadow: 0 2px 8px rgba(0, 0, 0, .33);
        transition: all .3s ease;
        font-family: Helvetica, Arial, sans-serif;

        @media screen and (max-width: 768px) {
            width: 320px;
            padding: 0;
        }
    }

    .modal-header h3 {
        margin-top: 0;
        color: #42b983;
    }

    .modal-body {
        margin: 20px 0;
    }

    .modal-default-button {
        //float: right;
    }

    .modal-enter {
        opacity: 0;
    }

    .modal-leave-active {
        opacity: 0;
    }

    .modal-enter .modal-container,
    .modal-leave-active .modal-container {
        -webkit-transform: scale(1.1);
        transform: scale(1.1);
    }
</style>