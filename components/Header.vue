<template>
  <section class="top-header">
    <div class="container">
      <div class="columns is-mobile">   
        <div class="column">
          <img src="~assets/img/search.svg" alt="search">
        </div>
        <div class="column has-text-centered">
          <img src="~assets/img/himart.svg" alt="himart">
        </div>
        <div class="column has-text-left">
          <img src="~assets/img/profile.svg" alt="profile">
        </div>
      </div> 
    </div>
  </section>
</template>

<script>
export default {
 name : "myHeader"
}
</script>

<style>
  .top-header{
    z-index: 99;
    position: fixed;
    top:0;
    padding: 10px;
    width: 100%;
    background-color: #ffffff;
    direction: rtl;
    box-shadow: 0px 1px 3px rgba(0, 0, 0, 0.2), 0px 0px 2px rgba(0, 0, 0, 0.14);
  }
</style>