<template>
        <div class="comic-card" >
        
            <img :src="srcCover" :alt="(titleBook +'cover')">
            <div class="wrap">
                <p>{{titleBook}}</p>
            </div>
        </div>
</template>

<script>
export default {
 name: "ComiCard",
 props: ["book", "srcCover", "titleBook"]
}
</script>

<style lang="scss" scoped>
    
   .comic-card{
       width: calc(200% / 13);
       margin-bottom: 50px;
       img{
           width:90%;
           margin:auto;
        }
        p{
            text-transform: uppercase;
            font-size: 12px;
        }
   }
</style>