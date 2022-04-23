<template>
   <v-toolbar
  height="70"
  color="transparent"
  
flat

class=""

>

   <v-app-bar-nav-icon color="#fff" class="hidden-md-and-up" @click="drawer=true"></v-app-bar-nav-icon>
<img  class="hidden-sm-and-down" style="cursor:pointer;" @click="goHome" src="../assets/Logo.svg" alt="">
<img class="hidden-md-and-up" style="cursor:pointer;width:70px" @click="goHome" src="../assets/Logo.svg" alt="">

<v-spacer></v-spacer>

<v-toolbar-items class="hidden-sm-and-down">
    <v-btn active-class="active" to="about" class="text-capitalize buttons" text>Home</v-btn>
    <v-btn to="pricing" text class="buttons">Contact</v-btn>
   
  
</v-toolbar-items>

<v-toolbar-items class="hidden-md-and-up">
 
    <v-navigation-drawer
    v-model="drawer"
    height="300"
    absolute
 
    width="100%"
    >
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="text-h6">
          Structurerite
          </v-list-item-title>
        
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list
        dense
        nav
      >
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
          :to="item.to"
          color="#007889"
        >
       

          <v-list-item-content>
            <v-list-item-title style="color:#007889;" color="#007889">{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

</v-toolbar-items>

<v-btn elevation="0" to="/auth/signup" style="color:#fff" color="rgba(38, 115, 209, 1)" class="buttons hidden-sm-and-down">Sign In</v-btn>
   </v-toolbar>
</template>

<script>
export default {

  data(){
return{
   items: [
        {
          icon: 'mdi-apps',
          title: 'About Us',
          to: '/about'
        },
        
        {
          icon: 'mdi-chart-bubble',
          title: 'Pricing',
          to: '/pricing'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Learn',
          to: '/learn'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'FAQs',
          to: '/faqs'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Sign In',
          to: '/faqs'
        },
      ],
      drawer:false,
       miniVariant: false,
         clipped: false,
      drawer: false,
      fixed: false,

       right: true,
      rightDrawer: false,
}
  },
methods:{
  goHome(){
    this.$router.push({path:'/'})
  }
}
}
</script>

<style scoped>
.buttons{
 
  border-radius: 6px;
  text-transform: capitalize;
  color:rgba(15, 45, 82, 1);
}


.active{
  text-decoration: underline;
}

</style>