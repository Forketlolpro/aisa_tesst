<template>
    <div v-bind:class="{responsive: isResponsive }" class="header">
        <div class="home">HOME</div>
        <div class="nav-item logo">LOGO</div>
        <div class="nav-item nickname" @click='showProfile'>NICKNAME</div>
        <div v-bind:class="{change: isResponsive }" class="container icon" v-on:click="myFunction()">
            <div class="bar1"></div>
            <div class="bar2"></div>
            <div class="bar3"></div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Header",
        data: ()=> {return {profilestat: false,isResponsive: false}},

        created: function () {
            this.profilestat=false;
            this.$emit('profile', this.profilestat);
        },

        methods: {
            showProfile () {
                this.profilestat = !(this.profilestat === true);
                this.$emit('profile', this.profilestat);
            },

            myFunction () {
                this.isResponsive=!(this.isResponsive === true);
            }
        }
    }
</script>

<style scoped>
    .header {
        display: flex;
        justify-content: space-between;
        height: 50px;
        border: 1px solid gainsboro;
    }

    .container {
        display: inline-block;
        cursor: pointer;
    }

    .bar1, .bar2, .bar3 {
        width: 35px;
        height: 5px;
        background-color: #333;
        margin: 6px 0;
        transition: 0.4s;
    }

    .change .bar1 {
        -webkit-transform: rotate(-45deg) translate(-9px, 6px);
        transform: rotate(-45deg) translate(-9px, 6px);
    }

    .change .bar2 {opacity: 0;}

    .change .bar3 {
        -webkit-transform: rotate(45deg) translate(-8px, -8px);
        transform: rotate(45deg) translate(-8px, -8px);
    }

    .icon {
        display: none;
    }

    .home {
        display: none;
    }

    @media screen and (max-width: 600px) {
        .header .icon, .header .home {
            display: block;
        }
    }

    @media screen and (max-width: 600px) {
        .header.responsive {
            position: relative;
        }
        .header.responsive .nav-item.logo {
            position: absolute;
            left: 0;
            top: 52px;
        }

        .header.responsive .nav-item.nickname {
            position: absolute;
            left: 0;
            top: 104px;
        }
        .topnav.responsive .nav-item{
            float: none;
            display: block;
            text-align: left;
        }
    }

</style>