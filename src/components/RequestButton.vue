<script setup>
import { ref } from "vue";
import axios from "axios";

const buttonText = ref("檢查後端伺服器是否正常運作");

const fetchData = async () => {
  buttonText.value = "正在等待回應";
  try {
    const response = await axios.get(import.meta.env.VITE_SERVER_BASE_URL);
    console.log(response.data);
    buttonText.value = "後端伺服器正常運作中";
  } catch (error) {
    console.error(error);
    buttonText.value = "後端伺服器運作異常";
  }
};
</script>

<template>
  <button class="btn btn-primary" @click="fetchData">{{ buttonText }}</button>
</template>

<style scoped></style>
