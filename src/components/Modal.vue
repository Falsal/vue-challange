<template>
  <div> 
    <!-- Button trigger modal -->
    <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#exampleModal">
      Submit
    </button>

    <!-- Modal -->
    <div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="exampleModalLabel">Success</h5>
            <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
          </div>
          <div class="modal-body"  style="height: '110%' ">
          <div class="text-primary fw-bold"><h1>Hello Hokify !</h1></div>
            <div class="my-3 ">
                <p class="text-start m-0 fs-6 fw-bold p-0">You are submitting : </p>
                <p class="text-start m-0 fs-6 p-0">{{ firstName }} {{ lastName}}  {{ email }} </p>
              </div>
          </div>
          <div class="modal-footer h-50">
            <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">
            Close
            </button>
            <button type="button" class="btn btn-success" data-bs-dismiss="modal" @click="resetFname"
            >Reset 
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Modal',
    props: [
      'firstName',
      'lastName',
      'email'
    ],
    emits: ["resetAll"],
    methods: {
      resetFname() {
        this.$emit("resetAll");
      },
    },
  }
</script>

<style>


</style>