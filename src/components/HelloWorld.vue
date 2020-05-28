<template>
  <v-container>
    <h2 class="display-2 center mb-4">New</h2>
    <v-layout>
    <template v-for="(product, index) in products">
    <v-flex xs2 pa-1 :key="index">
      <v-hover>
        <v-card slot-scope="{hover}" class="mx-auto" color="grey lighten-4" max-width="600" height="220">
          <v-img :src="product.src" :aspect-ratio="16/9">
            <v-expand-transition>
              <div v-if="hover" class="d-flex transition-fast-in-fast-out purple  darken-2 v-card--reveal display-3 white--text" style="height: 100%"> 
                {{product.price}}฿
              </div>
            </v-expand-transition>
          </v-img>

        <v-card-text class="pt-4" style="position: relative;">
          <v-btn absolute color="purple" class="shite--text" fab medium right top>
            <v-icon>mdi-shopping</v-icon>
          </v-btn>
        </v-card-text>

        
        <h3 class="display-1 font-weight-light purple--text mb-2 ml-2">
          {{product.title}}
        </h3> 
        <div class="font-weight-light mb-2 ml-2">
          {{product.description}}
        </div>
    </v-card>
      </v-hover>
    </v-flex>
    </template>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",

  data: () => ({
    products: [{
      price: 450,
      src: 'https://unicphscat.blob.core.windows.net/images-prd/s0000751.png',
      title: 'Blue whale',
      description: 'so lovely with whale'
    },{
      price: 500,
      src: 'https://unicphscat.blob.core.windows.net/images-prd/s0000751.png',
      title: 'Blue whale',
      description: 'so lovely with whale'
    },{
      price: 750,
      src: 'https://unicphscat.blob.core.windows.net/images-prd/s0000751.png',
      title: 'Blue whale',
      description: 'so lovely with whale'
    },{
      price: 1250,
      src: 'https://unicphscat.blob.core.windows.net/images-prd/s0000751.png',
      title: 'Blue whale',
      description: 'so lovely with whale'
    },{
      price: 1520,
      src: 'https://unicphscat.blob.core.windows.net/images-prd/s0000751.png',
      title: 'Blue whale',
      description: 'so lovely with whale'
    },{
      price: 2275,
      src: 'https://unicphscat.blob.core.windows.net/images-prd/s0000751.png',
      title: 'Blue whale',
      description: 'so lovely with whale'
    }]
  })
};
</script>

<style scoped>
  .v-card--reveal {
    align-items: center;
    bottom: 0;
    justify-content: center;
    opacity: 0.5;
    position: absolute;
    width: 100%;
  }

</style>
