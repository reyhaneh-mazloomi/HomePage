<template>
    <div class="main-content">
        <div class="container">
            <aroundme />
            <Slider :imgs="tizers"/>
        </div>
        <div class="container">
            <p class="cattitle" style="padding-top:10px;">تخفیف های امروز</p>
            <section class="main-div">
                <TodayDiscounts
                v-for="(item,index) in products" :key="index"
                :category="products[index]"
                />
            </section>
        </div>
        <div class="container">
            <p class="cattitle">فروشگاه های برتر</p>
            <section class="main-div">
                <BestStores
                :store="bestproducts[index]"
                v-for="(item,index) in bestproducts" :key="index"
                />
            </section>
        </div>
    </div>
</template>

<script>
import Slider from '../../components/Slider.vue'
import TodayDiscounts from '../../components/TodayDiscounts.vue'
import BestStores from '../../components/BestStores.vue'
import aroundme from '../../components/aroundme.vue'
import axios from 'axios';

export default {
  name: 'homepage',
  data(){
      return {
          products: [
            {name: "انواع لبنیات",
            discount: "تخفیف تا 5,000 تومان"},
            {name: "انواع لبنیات",
            discount: "تخفیف تا 5,000 تومان"},
            {name: "انواع لبنیات",
            discount: "تخفیف تا 5,000 تومان"},
          ],
          bestproducts: [],
          tizers: []
        }
  },
  components: { 
    aroundme,
    Slider,
    TodayDiscounts,
    BestStores 
  },
  methods :{
      Getbanner()
      {
        axios({
            method: 'get',
            url: 'https://api.himart.ir/tizer/GetbannerAndTizers/155/09391165470/ios-customer',
            data : '',
            timeout : 40000
        })
        .then(response=> {
            this.bestproducts = response.data.data.campaignPhotoURLs ;
            for(let i in response.data.data.tizerPhotoURLs)
            {   
                if(response.data.data.tizerPhotoURLs[i].url.indexOf('http')>-1)
                {
                    
                }
                else{
                    response.data.data.tizerPhotoURLs[i].url = 'http://' + response.data.data.tizerPhotoURLs[i].url;
                }
                let pushdata ={
                    mylink : response.data.data.tizerPhotoURLs[i].link,
                    myurl : response.data.data.tizerPhotoURLs[i].url,
                    myname : "myname" + i
                }
                this.tizers.push(pushdata);
            }
        });
      }
  },
  mounted : function(){
     // console.log(this.bestproducts) ;
      this.Getbanner();
  }
}
</script>

<style>
    .main-content{
        margin-top:70px;
        margin-bottom: 120px;
    }
    .cattitle{
        font-size: 12px;
        line-height: 16px;
        color: #B4B4B4;
        margin:10px;
    }
    .main-div{
        overflow-x: scroll;
        white-space: nowrap; 
    }
</style>