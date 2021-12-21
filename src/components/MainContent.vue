<template>
    <div class="main-content">
        <div class="jumbotron"></div>
        <div class="comics">
            <div class="single-box" v-for="(element, index) in comics" :key=index>
                <div class="comic-image">
                    <img :src="element.thumb" :alt="element.type">
                </div>
                <div class="comic-title">
                    {{element.series}}
                </div>
                <div class="comic-price">
                    {{element.price}}
                </div>
            </div>
             <div class="current-button">
            <a href="#">Current Series</a>
        </div>
        </div>
        <div class="load-button">
            <a href="#">Load More</a>
        </div>
    </div>

</template>

<script>
export default {
    name: "MainContent",
    data: function(){
        return {
            comics: [
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
                }
            ]
        }
    }
};
</script>

<style scoped lang="scss">
@import '../style/variables';

.main-content{
    background-color: $brand-primary-color;
    position: relative;
}

.jumbotron{
    background-image: url(../assets/img/jumbotron.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    padding: 250px 0;
}

.comics{
    width: 80%;
    margin: auto;
    color: white;
    padding: 75px 0 30px;
    display: flex;
    flex-wrap: wrap;
    position: relative;

    .single-box{
        width: calc(100% / 6);
        text-transform: uppercase;
        display: flex;
        font-size: 18px;
        flex-direction: column;

        .comic-image{
            height: 50%;
            overflow: hidden;
            margin-bottom: 20px;
        }

        .comic-title{
            margin-bottom: 10px;
            width: 80%;
        }

        .comic-price{
            display: none;
        }

        &:hover .comic-price{
            display: inline-block;
        }
    }
}

.current-button{
    position: absolute;
    top: -20px;
    left: -10px;

    a{
        text-decoration: none;
        color: white;
        background-color: $brand-secondary-color;
        border: 3px solid $brand-secondary-color;
        text-transform: uppercase;
        font-size: 30px;
        padding: 10px 20px;
    }
}

.load-button{
    padding-bottom: 50px;
    text-align: center;

    a{
        text-decoration: none;
        color: white;
        background-color: $brand-secondary-color;
        border: 3px solid $brand-secondary-color;
        padding: 10px 70px;
        font-size: 20px;
        text-transform: uppercase;

        &:hover{
            background-color: white;
            color: $brand-secondary-color;
        }
    }
}
</style>