<template>
    <div class="profile">
        <div class="left-content">
            <div class="profile-image"></div>
        </div>
        <div class="right-content">
            <div class="right-content-name">USER USER USER</div>
            <div class="email-phone-ip-wrapper">
            <div class="right-content-email">cat@cat.com</div>
            <div class="right-content-phone">8-999-999-99-99</div>
            <div class="right-content-ip">11.11.1111</div>
            </div>
            <div class="right-content-p">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</div>
            <div @click="$emit('showm')" class="button show-modal">SHOW</div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Profile"
    }
</script>

<style scoped lang="scss">
    .profile {
        display: flex;
        width: 1100px;
        margin: 0 auto;
        padding: 40px 10px;
    }

    .left-content {
        margin-right: 50px;
    }

    .right-content {
        display: flex;
        flex-direction: column;
    }

    .profile-image {
        width: 150px;
        height: 150px;
        border-radius: 50%;
        background-color: bisque;

        @media screen and (max-width: 768px){
            width: 100px;
            height: 100px;
        }
    }

    .right-content-name {
        border-bottom: 1px solid black;

        @media screen and (max-width: 768px){
            align-self: flex-end;
        }

        align-self: flex-start;
    }

    .email-phone-ip-wrapper {
        padding: 10px 0 10px 10px;

        @media screen and (max-width: 768px){
            align-self: flex-end;
        }

        align-self: flex-start;
    }

    .button.show-modal {
        height: 28px;
        width: 107px;
        background-color: aqua;
        display: flex;
        justify-content: center;
        align-items: center;
        cursor: pointer;
        margin-top: 10px;

        @media screen and (max-width: 768px) {
           display: none;
        }
    }

    .right-content-p {
        @media screen and (max-width: 768px){
            margin-left:   -138px;
            margin-top: 30px;
        }
    }
</style>