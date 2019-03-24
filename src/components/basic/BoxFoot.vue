<template>
    <div class="box-foot">
        <div class="music-swiper">

        </div>
        <div class="music-change">
            <p v-waves="{type:'center'}">
                <span class="iconfont icon-bofang"></span>
            </p>
            <p class="caidan" v-waves="{type:'center'}">
                <span class="iconfont icon-caidan"></span>
            </p>
        </div>
    </div>
</template>

<script>
import {mapState} from "vuex";
export default {
    computed:{
        ...mapState,
    },
    mounted(){
        console.log(this.musiclist)
    }
}
</script>

<style lang="less" scoped>
.box-foot{
    position:fixed;
    bottom: 0;
    width: 100%;
    display: flex;
    .h(135);
    border-top: 1px solid #e6e6e6;
    .px2rem(border-top-width,1);
    overflow: hidden;
    background: rgba(255, 255, 255, 0.8);

    .music-swiper{
        box-shadow: 0 0 20px white inset;
        flex: 1;
    }
    .music-change{
        .w(240);
        position: relative;
        p{
            .h(180);
            .lh(180);
            text-align: center;
            .w(180);
            position: absolute;
            top:50%;
            transform: translate(-20%,-50%);
            // border:1px solid black;
            border-radius: 50%;
            span{
                .fs(90);
            }
            
        }
        .caidan{
            right:0;
            transform: translate(20%,-50%)
        }
    }
    
}
</style>

