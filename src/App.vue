<template>
  <h1>Hi</h1>
  <div v-if="showModal">
    <Modal :header="header" :content="content" :theme="theme" @close="showModal=false">
            <h1>Login Success</h1>
              <p>Welcome AungZinMoe</p>

    </Modal>

  </div>
   <div v-if="showModal1">
    <Modal :header="header" :content="content" theme="delete" @close="showModal1=false">
            <h1>Are You Sure Logout</h1>
              <p>Bye Bye</p>

    </Modal>

  </div>
  <button @click="showModal=true">open Model</button>
  <button @click="showModal1=true">delete</button>
</template>

<script>
import Modal from "./components/Modal.vue"
export default {
  
data() {
  return {
    header:"Login Success",
    content:"Welcome AungZinMoe",
    theme:"success",
    showModal:false,
    showModal1:false
    

  }
},
components:{
  Modal
}
}
</script>

<style scoped>
h1{
  color:black;
}
</style>