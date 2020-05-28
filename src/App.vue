<template>
  <v-app>
    
    <v-navigation-drawer v-model="drawer" app temporary></v-navigation-drawer>
    <v-app-bar dense  app color="#FFCC33">
      <v-app-bar-nav-icon @click="drawer=!drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>YOLO</v-toolbar-title>
      <v-spacer></v-spacer>
      
      
        <v-btn flat color="#FFCC33" >
          <v-icon>mdi-storefront</v-icon>
          Products
        </v-btn> 
        
        <v-btn flat color="#FFCC33">
          <v-badge left color="green">
            <span slot="badge">5</span>
            <v-icon>mdi-shopping</v-icon>
           Basket
          </v-badge>
        </v-btn>
      
    </v-app-bar>

    <v-content>
      
      <HelloWorld />
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";


export default {
  name: "App",

  components: {
    HelloWorld
  },
  data () {
    return {
      drawer:false,
      items: [{
        icon: 'perm_identity',
        href: '#',
        title: 'Account'
      }],
    icons: {
    iconfont: 'mdi', // 'mdi' || 'mdiSvg' || 'md' || 'fa' || 'fa4' || 'faSvg'
  }
    }

  }
};
</script>
