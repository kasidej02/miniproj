<template>
    <v-container>
        <h2 class="display-2 mb-4">Basket</h2>

        <v-list two-line>
            <template v-for="(product, index) in products">
                <v-list-tile :key="product.product_id" avatar>
                    <v-list-tile-avatar>
                        <img :src="product.src">
                    </v-list-tile-avatar>
                    
                    <v-list-tile-content>
                        <v-list-tile-title v-html="product.title"></v-list-tile-title>
                    </v-list-tile-content>

                    <v-list-tile>
                        {{product.price}}฿
                    </v-list-tile>

                    <v-list-tile-action>
                        <v-text-field label="Quantity" reverse :value="product.qty"></v-text-field>
                    </v-list-tile-action>

                    <v-list-tile>
                        {{product.price * product.qty}}฿
                    </v-list-tile>

                    <v-list-tile-action>
                        <v-btn icon ripple>
                            <v-icon color="red lighten-1">mdi-delete</v-icon>
                        </v-btn>
                    </v-list-tile-action>

                </v-list-tile>
                <v-divider v-if="index + 1 < products.length" :key="index"></v-divider>
            </template>
                </v-list>
            </template>
        </v-list>

        <v-container>
            <v-btn color="success" larger style="float: right;">Go payment</v-btn>
        <v-container>

        </v-container>
</template>

<script>
export default {
name: "Basket",
  data: () => ({
    products: [{
      price: 450,
      src: 'https://unicphscat.blob.core.windows.net/images-prd/s0000751.png',
      title: 'Blue whale',
      description: 'so lovely with whale',
      qty: 1,
      product_id:555
    },{
      price: 500,
      src: 'https://unicphscat.blob.core.windows.net/images-prd/s0000751.png',
      title: 'Blue whale',
      description: 'so lovely with whale',
      qty: 2,
      product_id:555
    },{
      price: 750,
      src: 'https://unicphscat.blob.core.windows.net/images-prd/s0000751.png',
      title: 'Blue whale',
      description: 'so lovely with whale',
      qty: 2,
      product_id:555
    },{
      price: 1250,
      src: 'https://unicphscat.blob.core.windows.net/images-prd/s0000751.png',
      title: 'Blue whale',
      description: 'so lovely with whale',
      qty: 2,
      product_id:555
    },{
      price: 1520,
      src: 'https://unicphscat.blob.core.windows.net/images-prd/s0000751.png',
      title: 'Blue whale',
      description: 'so lovely with whale',
      qty: 2,
      product_id:555
    },{
      price: 2275,
      src: 'https://unicphscat.blob.core.windows.net/images-prd/s0000751.png',
      title: 'Blue whale',
      description: 'so lovely with whale',
      qty: 2,
      product_id:555
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