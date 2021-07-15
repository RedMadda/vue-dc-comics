<template>
<div>
    <div class="bcc">
        <div class="wrapper">
            <div class="first">
                <h2>dc comics</h2>
                <ul>
                    <li><a href="#">Characters</a></li>
                    <li><a href="#">Comics</a></li>
                    <li><a href="#">Movies</a></li>
                    <li><a href="#">TV</a></li>
                    <li><a href="#">Games</a></li>
                    <li><a href="#">Videos</a></li>
                    <li><a href="#">News</a></li>
                </ul>
                <h2>shop</h2>
                <ul>
                    <li><a href="#">Shop DC</a></li>
                    <li><a href="#">Shop Dc Collection</a></li>
                </ul>
            </div>
            <div class="second">
                <h2>dc comics</h2>
                <ul>
                    <li><a href="#">Characters</a></li>
                    <li><a href="#">Comics</a></li>
                    <li><a href="#">Movies</a></li>
                    <li><a href="#">TV</a></li>
                    <li><a href="#">Games</a></li>
                    <li><a href="#">Videos</a></li>
                    <li><a href="#">News</a></li>
                    <li><a href="#">Comics</a></li>
                    <li><a href="#">Movies</a></li>
                    <li><a href="#">TV</a></li>
                    <li><a href="#">Games</a></li>
                  </ul>
            </div>

            <div class="third">
                <h2>sites</h2>
                <ul>
                    <li><a href="#">DC</a></li>
                    <li><a href="#">MAD Megazine</a></li>
                    <li><a href="#">DC Kids</a></li>
                    <li><a href="#">DC Universe</a></li>
                    <li><a href="#">DC Power Visa</a></li>
                </ul>
            </div>

            <div class="fourth">
                <img src="..\assets\dc-logo-bg.png" alt="Logo">
            </div>

        </div>

    </div>

     <div class="low-footer">
        <div class="wrap">
            <span>sign up now!</span>
            <div class="social">
                <h4>follow us</h4>
                <ul>
                   <li v-for="(logo, index) in Logos" :key="index">
                       <a href="">
                           <img v-bind:src="logo.logoSrc" alt="Social Logo">
                       </a>
                   </li>
                </ul>
            </div>
        </div>
     </div>
    
</div>
</template>

<script>
import Logos from "../dati/ImgSocial.js"
export default {
    data(){
        return{
            Logos
        }
    }
}
</script>

<style lang="scss" scoped>

@import "../style/var.scss";
.bcc{
    background-image: url("../assets/footer-bg.jpg");
    background-size: cover;
    height: 350px;
    display:flex;
    justify-content: center;


    .wrapper{
        width:1240px;
        display: flex;
    
   
        .first, .second, .third{
            margin: 20px 50px;
            h2{
            text-transform: $upText;
            color:white;
            font-size: 20px;
            }
            ul{
                padding:0;
            }
            li{
                list-style-type: none;

                &:hover{
                    background-color: #4444442c;
                }

                a{
                    text-decoration: none;
                    color: #5e5d5d;
                    font-size: 13px;
                }
            }

        }
        .fourth{
           
            position: relative;
            width: 100%;
            height: 100%;
            overflow-y: hidden;
        
            img{
                height: 150%;
                position: absolute;
                left: 180px;
                bottom: -80px;
                
            }
        }
    }
}

.low-footer{
    width:100%;
    height: 80px;
    background-color: black;
    justify-content: space-between;
    text-transform: $upText;
    color:white;
    
    

    .wrap{
        width: 1140px;
        height: 100%;
        margin:auto;
        display:flex;
        align-items: center;
        justify-content: space-between;

        span{
            padding: 5px;
            border: 4px solid #0C7CEC;
        }

        .social{
            display:flex;
            align-items: center;
         h4{
             color: #0C7CEC;
             font: bolder;
             margin-right:10px;
         }   
         ul{
             display: flex;
             list-style-type: none;

             li{
                 padding: 10px;
             }
         }}
    }
}


    

</style>