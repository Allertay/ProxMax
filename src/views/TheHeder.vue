<template>
  <div class="TheHeder-title">
    <div class="Title"><p class="Title-name">ProxMax</p></div>
    <div class="icon">
    <div>
      <img src="../assets/love-svgrepo-com.svg" />
      <img src="../assets/sms-svgrepo-com.svg" />
      <img src="../assets/bell-alt-svgrepo-com.svg" />
    </div>
      <div class="data-users">
        <div class="ava-users"></div>
        <div class="user-name"><RouterLink to="/about" class="user-name">Nikita Chepelev</RouterLink></div>
      </div>
    </div>
  </div>
</template>
<script></script>

<style scoped>
.Title{
  padding: 10px;
  margin-left: 20px;
}
.Title-name{
  font-size: 30px;
  font-weight: 600;
}

.icon {
  margin: 10px;
  display: flex;
}
.data-users{
  display: flex;
}
.user-name{
  text-decoration: none;
  color: black;
  padding: 5px;
  font-size: 20px;
  font-weight: 600;
}
.ava-users {
  background-color: whitesmoke;
  width: 30px;
  height: 30px;
  float: left;
  margin-left: 20px;
  margin-right: 10px;
  border-radius: 50%;
}
.TheHeder-title {
  display: flex;
  justify-content: space-between;
  background-color: #495235;
  height: 50px;
  width: 100%;
}
.title {
  color: black;
  padding-top: 30px;
  padding-left: 10px;
  font-size: 30px;
  position: absolute;
  font-weight: 700;
  text-align: start;
}
</style>
