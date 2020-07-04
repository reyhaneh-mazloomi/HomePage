<template>
    <div class="AMBox">
        <img class="aroundmeimg" src="~assets/img/aroundme.svg" alt="">
        <span>اطراف من</span>
        <img class="openitimg" src="~assets/img/opensign.svg" alt="">
    </div>
</template>

<script>
export default {
    name: 'aroundme',
}
</script>

<style>
    .AMBox{
        background: #FFFFFF;
        border: 0.25px solid #C5C5C5;
        box-sizing: border-box;
        box-shadow: 0px 0px 2px rgba(0, 0, 0, 0.16);
        border-radius: 4px;
        margin:10px;
        padding:10px;
    }
    .aroundmeimg{
        float:right;
        margin-left: 10px;
    }
    .openitimg{
        float: left;
        margin-top: 8px;
    }
</style>