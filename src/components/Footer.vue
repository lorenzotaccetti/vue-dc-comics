<template>
    <div class="footer">
        <div class="top-footer">
            <div class="footer-links">
                <ul>
                    <h2>DC Comics</h2>
                    <li>
                        <a href="#">Characters</a>
                    </li>
                    <li>
                        <a href="#">Comics</a>
                    </li>
                    <li>
                        <a href="#">Movies</a>
                    </li>
                    <li>
                        <a href="#">TV</a>
                    </li>
                    <li>
                        <a href="#">Games</a>
                    </li>
                    <li>
                        <a href="#">Videos</a>
                    </li>
                    <li>
                        <a href="#">News</a>
                    </li>
                    <h2>Shop</h2>
                    <li>
                        <a href="#">Shop DC</a>
                    </li>
                    <li>
                        <a href="#">Shop DC Collectibles</a>
                    </li>
                </ul>
                <ul>
                    <h2>DC</h2>
                    <li>
                        <a href="#">Terms Of Use</a>
                    </li>
                    <li>
                        <a href="#">Privacy Police (New)</a>
                    </li>
                    <li>
                        <a href="#">Ad Choices</a>
                    </li>
                    <li>
                        <a href="#">Advertising</a>
                    </li>
                    <li>
                        <a href="#">Jobs</a>
                    </li>
                    <li>
                        <a href="#">Subscriptions</a>
                    </li>
                    <li>
                        <a href="#">Talent Workshops</a>
                    </li>
                    <li>
                        <a href="#">CPSC Certificates</a>
                    </li>
                    <li>
                        <a href="#">Ratings</a>
                    </li>
                    <li>
                        <a href="#">Shop Help</a>
                    </li>
                    <li>
                        <a href="#">Contact Us</a>
                    </li>
                </ul>
                <ul>
                    <h2>Sites</h2>
                    <li>
                        <a href="#">DC</a>
                    </li>
                    <li>
                        <a href="#">Mad Magazine</a>
                    </li>
                    <li>
                        <a href="#">DC Kids</a>
                    </li>
                    <li>
                        <a href="#">DC Universe</a>
                    </li>
                    <li>
                        <a href="#">DC Power Visa</a>
                    </li>
                </ul>
            </div>
            <div class="logo-footer">
                <img src="../assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>
        <div class="bottom-footer">
            <div class="btn">
                <button>Sign-Up Now!</button>
            </div>
            <div class="socials">
                <div>Follow Us</div>
                <i class="fab fa-facebook-f"></i>
                <i class="fab fa-twitter"></i>
                <i class="fab fa-youtube"></i>
                <i class="fab fa-pinterest-p"></i>
                <i class="fas fa-map-marker-alt"></i>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Footer"
};
</script>

<style scoped lang="scss">
@import '../style/variables';

.top-footer{
    background-image: url(../assets/img/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    display: flex;
    align-items: center;
    justify-content: space-around;

    .footer-links{
        display: flex;

        ul{
            list-style-type: none;
            margin: 0 30px;
            
            h2{
                color: white;
                text-transform: uppercase;
                font-size: 25px;
                margin: 10px 0;
            }

            li{
                margin: 15px 0;

                a{
                    text-decoration: none;
                    color: #7b7879;
                }
            }
        }
    }
}

.bottom-footer{
    background-color: $brand-primary-color;
    display: flex;
    align-items: center;
    justify-content: space-around;

    .btn{
        padding: 20px;
        button{
            background-color: $brand-primary-color;
            border: 2px solid $brand-secondary-color;
            padding: 15px 20px;
            text-transform: uppercase;
            color: white;
            font-size: 20px;
            cursor: pointer;
        }
    }

    .socials{
        display: flex;
        align-items: center;

        div{
            color: $brand-secondary-color;
            font-size: 20px;
            text-transform: uppercase;
            font-weight: 900;
            margin-right: 20px;
        }

        i{
           color: $brand-primary-color; 
           width: 30px;
           height: 30px;
           background-color: #7b7879;
           margin: 0 10px;
           display: flex;
           align-items: center;
           justify-content: center;
           border-radius: 50%;
           font-size: 18px;
           cursor: pointer;
        }
    }
}
</style>