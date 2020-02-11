<template>
  <div id="app">
    <comp-header 
      v-bind:Keymsg="msg"
      v-on:changeTitleEvent="handleChangeTitle"
      />
    <list-user 
      v-bind:listUser="listUser"
      v-on:deleteUserEvent="handleDeleteUser"
      />
  </div>
</template>

<script>
import CompHeader from './components/CompHeader'
import ListUser from './components/ListUser'
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      listUser: [
        {id:1, name: 'hello1', isActive: true},
        {id:2, name: 'hello2', isActive: true},
        {id:3, name: 'hell2o', isActive: true},
        {id:4, name: 'hello3', isActive: true},
        {id:5, name: 'he5llo', isActive: true},
        {id:6, name: 'hell2o', isActive: true},
      ]
    }
  },
  components: {
    CompHeader,
    ListUser
  },
  methods:{
    handleChangeTitle(){
      this.msg = "hello 123"
    },
    handleDeleteUser(data){
      var indexDelete = -1;
      this.listUser.forEach(u =>{
        console.log(u.id)
        if (u.id === data.id){
          indexDelete = u.idx;
        }
      });
      this.listUser.splice(indexDelete,1);
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}


</style>
