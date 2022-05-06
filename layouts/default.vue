<template>
  <v-app dark >

    
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
      class="pl-4 d-sm-block d-none"
    
    >
    <img class="mt-4 mb-3" src="../assets/Logo.svg" alt="">
      <v-list class="mt-4 ml-6">
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        
        >
          <v-list-item-action   class="rounded-lg">
            <v-icon color="rgba(38, 115, 209, 1)">{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title style="font-size:21;font-weight:500;" color="rgba(55, 80, 111, 1)" v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <!-- <v-app-bar
      :clipped-left="clipped"
      fixed
      app
      elevation="0"
      color="rgba(255, 255, 255, 1);"
      style="border-bottom:1.5px solid grey"

    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" class="d-sm-block d-none" />
     
     <div class="ml-4 mt-4">
       <h4 style="color:rgba(15, 45, 82, 1);font-size:18px;font-weight:500">Welcome !</h4>
     <p style="font-size:rgba(55, 80, 111, 1)">Evwidonor Allen</p>
     </div>
   
      <v-spacer />


       <nuxt-link to="/auth/login" class="d-sm-block d-none" style="text-decoration:none">  
     <v-btn style="text-transform:none;font-size:18px;font-weight:500" text color="rgba(255, 148, 143, 1)">
       Logout
     </v-btn>
       </nuxt-link>


<v-btn class="d-sm-none d-block" text color="#fff" to="/">
  <img src="../assets/mobile-log-.svg" alt="">
</v-btn>
    </v-app-bar> -->
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <!-- <v-navigation-drawer
      v-model="rightDrawer"
      :right="right"
      temporary
      fixed
    >
      <v-list>
        <v-list-item @click.native="right = !right">
          <v-list-item-action>
            <v-icon light>
              mdi-repeat
            </v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch drawer (click me)</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer> -->

    <div class="d-sm-none d-block">
  <v-bottom-navigation
    :value="value"
    color="blue"
    grow
    fixed
    
  >
    <v-btn to="/">
      <span>Dashboard</span>

      <v-icon>mdi-apps</v-icon>
    </v-btn>

    <v-btn to="/dashboard/transfer">
      <span>Transfer</span>

      <v-icon>mdi-swap-horizontal</v-icon>
    </v-btn>

    <v-btn to="/dashboard/bills">
      <span>Pay Bills</span>

      <v-icon>mdi-credit-card</v-icon>
    </v-btn>

       <v-btn to="/dashboard/profile">
      <span>Profile</span>

      <v-icon>mdi-account-outline</v-icon>
    </v-btn>
  </v-bottom-navigation>
</div>
  
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      clipped: false,
      drawer: false,
       value: '' ,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Dashboard',
          to: '/'
        },
        {
          icon: 'mdi-swap-horizontal',
          title: 'Transfer',
          to: '/dashboard/transfer'
        },
         
         {
          icon: 'mdi-credit-card',
          title: 'Pay Bills',
          to: '/dashboard/bills'
        },
         {
          icon: 'mdi-account-outline',
          title: 'Profile',
          to: '/dashboard/profile'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>

<style >
.app{
  font-family: 'Poppins', sans-serif;
}
.v-list-item--active {
  background-color: rgba(38, 115, 209, 0.01);
  color:blue;
}
.v-list-item-content--active{
  color: blue;
}
</style>
