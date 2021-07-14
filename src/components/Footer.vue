<template>
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
  
</template>

<script>
export default {

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
    

</style>