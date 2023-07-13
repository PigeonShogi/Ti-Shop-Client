<script setup>
defineProps({
  msg: String,
});
</script>

<template>
  <h1>{{ msg }}</h1>

  <div class="sign-in-form">
    <form>
      <div class="mb-3">
        <label for="exampleInputEmail1" class="form-label">Email address</label>
        <input
          type="email"
          class="form-control"
          id="exampleInputEmail1"
          aria-describedby="emailHelp"
        />
        <div id="emailHelp" class="form-text">
          We'll never share your email with anyone else.
        </div>
      </div>
      <div class="mb-3">
        <label for="exampleInputPassword1" class="form-label">Password</label>
        <input
          type="password"
          class="form-control"
          id="exampleInputPassword1"
        />
      </div>
      <div class="mb-3 form-check">
        <input type="checkbox" class="form-check-input" id="exampleCheck1" />
        <label class="form-check-label" for="exampleCheck1">Check me out</label>
      </div>
      <button type="submit" class="btn btn-primary">Submit</button>
    </form>
  </div>
</template>

<style scoped>
.sign-in-form {
  border: solid;
  display: flex;
  flex-direction: column;
  justify-content: center;
  max-width: 320px;
  padding: 30px;
  margin: auto;
  height: 50vh;
}
</style>
