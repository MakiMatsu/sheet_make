<template>
  <div class="git">
    <h>public repo num : {{userDatas.public_repos}}</h>
  </div>
</template>


<script>
import axios from "axios";
require("dotenv").config();
const GIT_API = process.env.VUE_APP_GIT;
export default {
  name: "GitData",
  props: {
    repoName: String
  },
  data() {
    return { userDatas: [] };
  },
  mounted() {
    console.log(GIT_API);
    const request = axios.create({
      baseURL: "https://api.github.com"
    });
    request.get(`/users/${this.repoName}?access_token=${GIT_API}`).then(res => {
      this.userDatas = res.data;
    });
  }
};
</script>

<style lang="scss">
</style>

