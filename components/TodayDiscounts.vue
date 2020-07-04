<template>
    <div class="TDBox">
        <div class="catimg">
            <img src="~assets/img/todaydiscounts.svg" alt="">
        </div>
        <div class="catinfo">
            <p class="catname">{{ category.name }}</p>
            <p class="catdiscount">{{ category.discount }}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'TodayDiscounts',
    props:{
        category: Object
    }
}
</script>

<style>
    .TDBox{
        border:1px solid #4285F4;
        box-shadow: 0px 0px 2px rgba(0, 0, 0, 0.16);
        border-radius: 4px;
        box-sizing: border-box;
        margin: 0px 10px 0px 0px;
        direction: rtl;
        text-align: right;
        min-width: 160px;
        display: inline-block;
        padding: 5px;
    }
    .catimg{
        display: inline-block;
        
    }
    .catinfo{
        display: inline-block;
    }
    .catname{
        font-size: 14px;
        line-height: 24px;
        color: #757575;
        margin-bottom: 10px;
    }
    .catdiscount{
        font-size: 10px;
        line-height: 16px;
        letter-spacing: -0.5px;
        color: #FF5050;
    }
</style>