<template>
    <b-carousel>
        <b-carousel-item v-for="(item, i) in carousels" :key="i">
            <img :src="item.myurl" />
        </b-carousel-item>
    </b-carousel>
</template>

<script>
export default {
    props: {
        imgs : Object
    },
    data(){
        return {
            carousels: this.imgs
        }
    },

}
</script>

<style>
    .carousel .carousel-items {
        width: 93vw;
        margin: 0 auto;
    }
    .carousel .carousel-item{
        text-align: center;
    }
    .carousel .carousel-items img{
        border-radius: 5px;
    }
    .carousel .carousel-indicator .indicator-item:not(:last-child) {
        margin-left: 0.5rem;
        margin-right: 0;
    }
    .carousel-pause{
        display: none;
    }
</style>