<template>
  <div id="app" class="h-100">
    <div class="container-fluid h-100">
      
       <div class="col-md-9  h-100 d-flex justify-content-center align-items-left">
       <div class="col-mid-8 rounded px=2 py=3   shadow bg-black text-align-left">

       </div>
       <SignupForm/>
      </div>
    </div>
  
</div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import SignupForm from './components/SignupForm.vue'



export default {
  name: 'App',
  components: {
    SignupForm
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: black;
  margin-top: 30px;
  margin-left: 300px;
  text-align: left;
  margin-right: 250px;
 font-weight: bold;
 background-color: white;
 width: fit-content;
 
  

}

</style>
