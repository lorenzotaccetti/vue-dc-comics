<template>
    <div class="info-area">
        <div class="single-box">
            <img src="../assets/img/buy-comics-digital-comics.png" alt="">
            Digital Comics
        </div>
        <div class="single-box">
            <img src="../assets/img/buy-comics-merchandise.png" alt="">
            DC Merchandise
        </div>
        <div class="single-box">
            <img src="../assets/img/buy-comics-subscriptions.png" alt="">
            Subscription
        </div>
        <div class="single-box">
            <img class="smaller" src="../assets/img/buy-comics-shop-locator.png" alt="">
            Comic Shop Locator
        </div>
        <div class="single-box">
            <img src="../assets/img/buy-dc-power-visa.svg" alt="">
            DC Power Visa
        </div>
    </div>
</template>

<script>
export default {
    name: "InfoArea"
};
</script>

<style scoped lang="scss">
@import '../style/variables';

.info-area{
    background-color: $brand-secondary-color;
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;

    .single-box{
        display: flex;
        align-items: center;
        margin: 40px 40px;
        text-transform: uppercase;

        img{
            width: 60px;
            margin-right: 10px;
        }

        .smaller{
                width: 50px;
        }
    }
}
</style>