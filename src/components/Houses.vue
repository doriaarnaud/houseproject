<script setup>
import {ref} from 'vue'
defineProps(
{
  houseimage:String,
  houseprice:String,
  chamber:String,
  bathroom:String,
  squarefeet:String,
  housedescription:String
})
const emit=defineEmits(['describe']);
function imageclick(id)
{
  emit('describe');
}
</script>
<template>
  <v-card class="housespresentation ma-5">
    <div class="house ma-5 pa-5">
      <v-img :src="houseimage" class="mt-n16"
             title="See details"
             alt="Each house presentation"
             @click="imageclick"
             width="350"
             height="250">
      </v-img>
      <p class="text-h6 mt-n10 ms-1 price">AED {{houseprice}}</p>
      <p class="text-h6 mt-2 ms-1" id="houseprice">{{chamber}}
                    <v-icon
                      size="x-small"
                      color="#002600"
                      icon="mdi-bed"
                      class="ms-1 mb-1"
                    ></v-icon> /
                    {{bathroom}}
                    <v-icon
                      size="x-small"
                      color="#002600"
                      icon="mdi-scale-bathroom"
                      class="ms-1 mb-1"
                    ></v-icon> /
                    {{squarefeet}} sqrft</p>
        <p class="text-h6 mt-0">{{housedescription}}</p>
    </div>
  </v-card>
</template>

<script>
</script>

<style>
  @media (min-width: 1200px)
  {
    .housespresentation
    {
      width:320px;
      height:350px;
    }
    .house
    {
      margin:0;
    }
    img:hover
    {
      cursor: pointer;
    }
    p.price
    {
      color:#15a2ff;
    }
  }
  @media (min-width: 992px) and (max-width: 1199px)
  {
    .housespresentation
    {
      width:220px;
      height:330px;
    }
    .house
    {
      margin:0;
    }
    img:hover
    {
      cursor: pointer;
    }
    p.price
    {
      color:#15a2ff;
    }
  }
  @media (min-width: 768px) and (max-width: 991px)
  {
    .housespresentation
    {
      width:220px;
      height:330px;
    }
    .house
    {
      margin:0;
    }
    img:hover
    {
      cursor: pointer;
    }
    p.price
    {
      color:#15a2ff;
    }
  }
  @media (min-width: 576px) and (max-width: 767px)
  {
    .housespresentation
    {
      width:320px;
      height:290px;
    }
    .house
    {
      margin:0;
    }
    img:hover
    {
      cursor: pointer;
    }
    p.price
    {
      color:#15a2ff;
    }
  }
  @media (max-width: 575px)
  {
    .housespresentation
    {
      width:320px;
      height:290px;
    }
    .house
    {
      margin:0;
    }
    img:hover
    {
      cursor: pointer;
    }
    p.price
    {
      color:#15a2ff;
    }
  }

</style>
