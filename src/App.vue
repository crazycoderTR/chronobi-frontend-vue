<template>
  <div id="app">
    <app-nav-bar/>
    <app-header/>
    <app-services v-bind:items="ServicesItem" />
    <app-products v-bind:items="ProductItem"/>
    <app-about v-bind:items="AboutItem"/>
    <app-team v-bind:items="TeamItem"/>
    <app-clients v-bind:items="ClientsItem"/>
    <app-contacts/>
    <app-footer v-bind:item="SocialItem"/>
    <app-modal v-bind:items="ProductItem"/>
  </div>
</template>

<script>
import Navbar from './components/Navbar';
import Header from './components/Header';
import Services from './components/Services';
import Products from './components/Products';
import About from './components/About';
import Teams from './components/Teams';
import Clients from './components/Clients';
import Contacts from './components/Contacts';
import Footer from './components/Footer';
import Modal from './components/Modal';
import json from "./components/data.json";
export default {
  name: 'App',
  components: {
    appNavBar: Navbar,
    appHeader: Header,
    appServices: Services,
    appProducts: Products,
    appAbout: About,
    appTeam: Teams,
    appClients: Clients,
    appContacts: Contacts,
    appFooter: Footer,
    appModal: Modal
  },
  created(){
   this.TeamItem=json.team;
   this.AboutItem=json.about;
   this.ProductItem=json.products;
   this.ServicesItem=json.services;
   this.ClientsItem=json.clients;
   this.SocialItem=json.socialMedia;
  },
  data:function () {
    return{
      AboutItem:[],
      ProductItem:[],
      ServicesItem:[],
      TeamItem:[],
      ClientsItem:[],
      SocialItem:Object,
      isModelOpened:false,
      selectedProductId:0,

    }
  }
}
</script>

<style>

</style>
