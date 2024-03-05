<script setup>
import {ref} from 'vue'
defineProps(
{
  houseimage:String,
  title1:String,
  title2:String,
  title3:String,
  title4:String,
  buttontitle:String
})
const emit=defineEmits(['exploring'])
function buttonclick()
{
  emit('exploring')
}
</script>

<template>
  <div class="banner h-auto">
    <div class="bannercontent">
      <div class="house">
        <img :src="houseimage" alt="House image"/>
      </div>
       <div class="presentationtext">
           <h6 class="mt-8 text-h6" :title1="title1">{{title1}}</h6>
           <h4 class="mt-8 text-h4" :title2="title2">{{title2}}</h4>
           <h4 class="mt-2 text-h4" :title3="title3">{{title3}}</h4>
           <h4 class="mt-2 text-subtitle-3" :title4="title4">{{title4}}</h4>
           <v-btn class="exploring mt-5 text-h6" color="#bcbcbc" @click="buttonclick">
             {{buttontitle}}
           </v-btn>
       </div>
     </div>
  </div>
</template>

<script>
</script>

<style>
  @media (min-width: 1200px)
  {
    .banner
    {
      min-height:450px;
      display:flex;
      align-content: center;
      justify-content: center;
      flex-wrap: wrap;
      text-align: left;
      margin-top: 0px;
    }
    .bannercontent
    {
      width:950px;
      margin-left:auto;
      margin-right:auto;
    }
    .bannercontent .house
    {
      float:left;
    }
    .bannercontent .presentationtext
    {
      margin-top:-25px;
      float:right;
      width:450px;
    }
    .exploring
    {
      color:#000000;
    }
  }
  @media (min-width: 992px) and (max-width: 1199px)
  {
    .banner
    {
      min-height:450px;
      display:flex;
      align-content: center;
      justify-content: center;
      flex-wrap: wrap;
      text-align: left;
      margin-top: 0px;
    }
    .bannercontent
    {
      width:950px;
      margin-left:auto;
      margin-right:auto;
    }
    .bannercontent .house
    {
      float:left;
    }
    .bannercontent .presentationtext
    {
      margin-top:-25px;
      float:right;
      width:450px;
    }
    .exploring
    {
      color:#000000;
    }
  }
  @media (min-width: 768px) and (max-width: 991px)
  {
    .banner
    {
      min-height:450px;
      display:flex;
      align-content: center;
      justify-content: center;
      flex-wrap: wrap;
      text-align: left;
      margin-top: 0px;
    }
    .bannercontent
    {
      width:950px;
      margin-left:auto;
      margin-right:auto;
    }
    .bannercontent .house
    {
      float:left;
    }
    .bannercontent .house img
    {
      width:320px;
      height:270px;
      margin-left:10px;
    }
    .bannercontent .presentationtext
    {
      margin-top:-35px;
      float:right;
      width:420px;
    }
    .exploring
    {
      color:#000000;
    }
  }
  @media (min-width: 576px) and (max-width: 767px)
  {
    .banner
    {
      min-height:450px;
      display:flex;
      align-content: center;
      justify-content: center;
      flex-wrap: wrap;
      text-align: left;
      margin-top: 0px;
    }
    .bannercontent
    {
      width:950px;
      margin-left:auto;
      margin-right:auto;
    }
    .bannercontent .house
    {
    }
    .bannercontent .house img
    {
      width:100%;
      height:300px;
      margin:10px;
      margin-right:10px;
    }
    .bannercontent .presentationtext
    {
      margin-top:-25px;
      width:450px;
      margin-left:10px;
      margin-right: 10px;
    }
    .exploring
    {
      color:#000000;
    }
  }
  @media (max-width: 575px)
  {
    .banner
    {
      min-height:450px;
      display:flex;
      align-content: center;
      justify-content: center;
      flex-wrap: wrap;
      text-align: left;
      margin-top: 0px;
    }
    .bannercontent
    {
      width:950px;
      margin-left:auto;
      margin-right:auto;
    }
    .bannercontent .house
    {
      float:left;
      display:none;
    }
    .bannercontent .presentationtext
    {
      margin-top:-25px;
      width:100%;
      margin-left:10px;
    }
    .exploring
    {
      color:#000000;
    }
  }
</style>
