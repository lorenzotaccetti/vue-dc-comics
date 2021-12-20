<template>
    <div class="header">
        <div class="logo">
            <img src="../assets/img/dc-logo.png" alt="">
        </div>
        <div class="links" v-for="(element, index) in links" :key="index">
            {{element.text}}
        </div>
    </div>
</template>

<script>
export default {
    name: "Header",
    data: function(){
        return{
            links: [
                {
                    text: 'Characters',
                    current: false
                },
                {
                    text: 'Comics',
                    current: true
                },
                {
                    text: 'Movies',
                    current: false
                },
                {
                    text: 'TV',
                    current: false
                },
                {
                    text: 'Games',
                    current: false
                },
                {
                    text: 'Collectibles',
                    current: false
                },
                {
                    text: 'Videos',
                    current: false
                },
                {
                    text: 'Fans',
                    current: false
                },
                {
                    text: 'News',
                    current: false
                },
                {
                    text: 'Shop',
                    current: false
                }
            ]
        }
    }
};
</script>

<style scoped lang="scss">
@import '../style/variables';

.header{
    background-color: white;
    height: 125px;
    line-height: 125px;
    width: 80%;
    margin: auto;
    display: flex;
    flex-direction: row;

    .logo{
        flex-grow: 1;

        img{
            display: inline-block;
            width: 90px;
            vertical-align: middle;
        }
    }

    .links{
        font-size: 20px;
        margin: 0 15px;
        text-transform: uppercase;
        color: $brand-primary-color;
        cursor: pointer;

        &:hover{
            color: $brand-secondary-color;
            border-bottom: 4px solid $brand-secondary-color;
        }
    }
}
</style>