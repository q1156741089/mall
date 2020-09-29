<template>
    <div>
        <van-search
                shape="round"
                background="red"
                placeholder="请输入搜索关键词"
        >
            <template #left>
                <van-icon name="shop" size="20"  color="#FFFFFF"  />
            </template>
        </van-search>
        <van-swipe :autoplay="3000">
            <van-swipe-item v-for="(image, index) in images" :key="index">
                <img v-lazy="image" class="imgUrl"/>
            </van-swipe-item>
        </van-swipe>
        <div class="wrapper" ref="wrapper">
            <ul class="content">
     
            </ul>
        </div>
    </div>
</template>

<script>
    export default {
        name: "shop",
        data(){
            return {
                images :[
                    'https://img.alicdn.com/imgextra/i4/102/O1CN01pugfcR1Ccl1HgBJWJ_!!102-0-luban.jpg',
                    'https://aecpm.alicdn.com/simba/img/TB1CWf9KpXXXXbuXpXXSutbFXXX.jpg_q50.jpg',
                    'https://picasso.alicdn.com/imgextra/i1/370808/O1CNA18AYAOk100f48c5caf90b0b2e9c0006_!!370808-0-picassobanner.jpg',
                    'https://gw.alicdn.com/imgextra/i3/187/O1CN01d5uvAF1DFggWEloM7_!!187-0-lubanu.jpg'
                ]
            }
        }
    }
</script>

<style scoped>
.imgUrl{
    height: 102px;
    width: 100%;
}
</style>