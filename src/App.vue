<template>
  <div>
    <the-header></the-header>
    <div>
      <button @click="setComponenId('active-user')">Active User</button>
      <button @click="setComponenId('manage-user')">Manage User</button>
    </div>
    <keep-alive>
    <component :is="componentId"></component>
    </keep-alive>
  </div>
</template>

<script>
import TheHeader from './components/Layout/TheHeader.vue';
import ActiveUser from './components/ActiveUser.vue';
import ManageUser from './components/ManageUser.vue';

export default {
  data() {
    return {
      componentId:'active-user',
      activeUser: {
        name: 'Maximilian Schwarzmüller',
        description: 'Site owner and admin',
        role: 'admin',
      },
    };
  },
  methods:{
    setComponenId(id){
      this.componentId=id;
    }
  },
  components:{
    TheHeader,
    ActiveUser,
    ManageUser,
  }
};
</script>

<style>
html {
  font-family: sans-serif;
}

body {
  margin: 0;
}
</style>