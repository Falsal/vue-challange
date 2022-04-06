<template>

  <div class="row d-flex justify-content-center">
    <div class="col-sm-12 w-100 mb-5">
      <h1>{{ title }}</h1>
    </div>
    <div class="w-25 col-sm-12 border border-primary border-3 rounded mb-3 p-5">
      <form>
        <div class="mb-3">
          <label for="firstName" class="form-label">First Name</label>
          <input type="text" class="form-control" v-model="firstName" />
        </div>
        <div class="mb-3">
          <label for="lastName" class="form-label">Last Name</label>
          <input type="text" class="form-control" v-model="lastName" />
        </div>
        <div class="mb-3">
          <label for="email" class="form-label">Email address</label>
          <input type="email" v-model="email" class="form-control" />
        </div>
        <div class="mb-3">
          <Modal  :firstName="firstName" :lastName="lastName" :email="email"  @resetAll="manageClick"/>
        </div>
        <div class="d-flex justify-content-start">
          <div class="my-3 ">
            <p class="text-start m-0 fs-6 fw-bold p-0">You are submitting : </p>
            <p class="text-start m-0 fs-6 p-0">Your Name : {{ firstName }} {{ lastName }} </p>
            <p class="text-start m-0 fs-6 p-0">Email Address: {{ email }}</p>
          </div>
        </div>
      </form>
    </div>
  </div>

  
</template>


<script>
  import Modal from "@/components/Modal.vue"
  

  export default {
    name: "HomeView",
    data() {
      return {
        title: "My First Vue App ever !",
        firstName : "",
        lastName : "",
        email : "" ,
          
      };
    },
    components: {
      Modal
    },

    methods: {
      manageClick() {
       console.log('clicked')
       this.firstName=''
       this.lastName=''
       this.email=''
      },
    },
  };
    // <Modal v-bind:fname="firstName" v-bind:lname="lastName" v-bind:email="email" @resetFname="firstName = $event"/>

</script>

<style>


</style>

