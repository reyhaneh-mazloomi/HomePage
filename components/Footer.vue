<template>
    <section class="botoom-footer">
        <div class="container">
            <div class="columns is-mobile">
                <div @click="isactivehome()" class="column has-text-centered">
                    <img :src="footer.homeimg" alt="home">
                    <p class="footer-nav" id="home">{{footer.hometxt}}</p>
                </div>
                <div @click="isactivestore()" class="column has-text-centered">
                    <img :src="footer.storeimg" alt="store">
                    <p class="footer-nav" id="store">{{footer.storetxt}}</p>
                </div>
                <div @click="isactivewallet()" class="column has-text-centered">
                    <img :src="footer.walletimg" alt="wallet">
                    <p class="footer-nav" id="wallet">{{footer.wallettxt}}</p>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import disactivehomeimg from '../assets/img/home.svg'
import activehomeimg from '../assets/img/activehome.svg'
import disactivestoreimg from '../assets/img/store.svg'
import activestoreimg from '../assets/img/activestore.svg'
import disactivewalletimg from '../assets/img/wallet.svg'
import activewalletimg from '../assets/img/activewallet.svg'

export default {
    name : "myFooter",
    data: function() {
        return{
            footer:{
                homeimg : activehomeimg,
                storeimg : disactivestoreimg,
                walletimg : disactivewalletimg,
                hometxt : 'خانه'
            }
        }
    },
    methods: {
        isactivehome()
        {
            this.footer.homeimg = activehomeimg;
            this.footer.storeimg = disactivestoreimg;
            this.footer.walletimg = disactivewalletimg;
            this.footer.hometxt = 'خانه';
            this.footer.storetxt = '';
            this.footer.wallettxt = '';
        },
        isactivestore()
        {
            this.footer.homeimg = disactivehomeimg;
            this.footer.storeimg = activestoreimg;
            this.footer.walletimg = disactivewalletimg;
            this.footer.hometxt = '';
            this.footer.storetxt = 'فروشگاه';
            this.footer.wallettxt = '';
        },
        isactivewallet()
        {
            this.footer.homeimg = disactivehomeimg;
            this.footer.storeimg = disactivestoreimg;
            this.footer.walletimg = activewalletimg;
            this.footer.hometxt = '';
            this.footer.storetxt = '';
            this.footer.wallettxt = 'کیف پول';
        }
    }
}
</script>

<style>
  .botoom-footer{
    position: fixed;
    bottom: 0;
    width: 100%;
    background-color: #ffffff;
    box-shadow: 0px 1px 3px rgba(0, 0, 0, 0.2), 0px 2px 2px rgba(0, 0, 0, 0.12), 0px 0px 2px rgba(0, 0, 0, 0.14);
    border-radius: 6px 6px 0px 0px;
    padding: 5px 0px;
    direction: rtl;
    font-size: 12px;
    line-height: 21px;
    color: #2B71B8;
  } 
</style>