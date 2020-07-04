<template>
    <div class="BSBox">
        <div class="storepic">
            <img :src="'https://' + store.url" alt="">
        </div>
        <!-- <div class="storeinfo">
            <p class="name">{{ store.name }}</p>
            <p>
                <span class="store">{{ store.distance }}</span>
                <span class="store">{{ store.point }}</span>
            </p>
        </div> -->
    </div>
</template>

<script>
export default {
    name: 'BestStores',
        props:{
        store: Object
    },
}
</script>

<style>
    .BSBox{
        border: 0.25px solid #C5C5C5;
        box-sizing: border-box;
        box-shadow: 0px 0px 2px rgba(0, 0, 0, 0.16);
        border-radius: 4px;
        margin: 0px 10px 0px 0px;
        direction: rtl;
        text-align: right;
        min-width: 200px;
        display: inline-block;
        padding: 5px;
    } 
    .storepic{
        display: inline-block;
    }
    /* .storeinfo{
        display: inline-block;
    }
    .name{
        font-size: 14px;
        line-height: 24px;
        color: #757575;
    }
    .store{
        font-size: 10px;
        line-height: 16px;
        letter-spacing: 0.15px;
        color: #C9C9C9;
    } */
</style>