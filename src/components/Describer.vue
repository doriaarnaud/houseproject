<script setup>
import {ref} from 'vue'
const emit=defineEmits(['closedialog'])
function fermerdialog()
{
  emit(closedialog);
}
defineProps(
{
  id:Number,
  mainslider:Object,
  textalt:String,
  price:String,
  chamber:String,
  bathroom:String,
  squarefeet:String,
  fulldescription:String,
  dialog:Boolean
})
</script>

<template>
  <div class="carousselcontainer text-center pa-4">
      <v-dialog
            v-model="dialog"
            transition="dialog-bottom-transition"
            fullscreen
          >
        <v-card>
          <v-toolbar>
            <v-btn
              icon="mdi-close"
              @click="fermerdialog"
            ></v-btn>

          </v-toolbar>
          <div class="carousselcontainer">
            <div class="carousselcontent">
              <v-carousel
                    height="400"
                    progress="primary"
                    hide-delimiters
                    cycle
                  >
                    <v-carousel-item
                      v-for="techimg in mainslider"
                      :key="techimg.id"
                    >
                      <v-img :src="techimg.images" :alt="techimg.textalt" class="mt-10">

                      </v-img>
                    </v-carousel-item>
                  </v-carousel>
            </div>
            <div class="descriptioncontainer">
              <div class="descriptioncontent">
                <h6 class="text-h6">{{price}}</h6>
                <h6 class="text-h6">{{chamber}} <v-icon
                      size="x-small"
                      color="#002600"
                      icon="mdi-bed"
                      class="ms-1"
                    ></v-icon>| {{bathroom}}
                    <v-icon
                      size="x-small"
                      color="#002600"
                      icon="mdi-scale-bathroom"
                      class="ms-1"
                    ></v-icon>| {{squarefeet}} Sqrft</h6>
                    <p class="text-h6 ms-5">{{fulldescription}}</p>
              </div>
            </div>
          </div>
        </v-card>
      </v-dialog>
  </div>
</template>

<script>
</script>

<style>
</style>
