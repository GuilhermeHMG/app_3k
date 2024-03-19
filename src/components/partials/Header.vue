<template>
  <div class="custom-header">
    <div class="header-content">
      <div class="row">
        <div class="col">
          <router-link to="/">
            <img class="logo-header" src="../../assets/images/icons/logo.png">
          </router-link>
        </div>
      </div>
      <div class="avatar-icon">
        <Avatar icon="pi pi-user" class="mr-2" size="small" shape="circle"/>
      </div>
    </div>
  </div>
</template>

<script>
import Cookies from 'js-cookie';

export default {
  name: "Header",
  data() {
    return {}
  },
  methods: {},
};
</script>

<style>

.custom-header {
  position: fixed;
  z-index: 99;
  width: 100%;
  background: #E6E6E0;
  border-bottom: 1px solid #E6E6E0;
}

.header-content {
  display: flex;
  align-items: center;
  height: 48px;
}

.header-content h1 {
  height: 40px;
  margin-top: 5px;
  padding-top: 7px;
  padding-right: 10px;
}

.logo-header {
  width: 3rem;
}

.avatar-icon {
  position: relative;
  cursor: pointer;
  margin-left: auto;
  max-width: 15vw;
  padding-right: 1vw;
}

</style>
