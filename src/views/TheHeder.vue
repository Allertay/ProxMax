<template>
  <div class="TheHeder-title">
    <div class="Title"><p class="Title-name">ProxMax</p></div>
    <div class="icon">
    <div>
      <img src="../assets/love-svgrepo-com.svg" />
    </div>
      <div class="data-users">
        <div class="ava-users"></div>
        <div class="user-name"><RouterLink to="/about" class="user-name-a">Nikita Chepelev</RouterLink></div>
      </div>
    </div>
  </div>
</template>
<script>
export default {

  data(){
    return{
      TheCart: false
    }
  },
  methods:{
    openCartMenu(){
    }
  }
}
</script>

<style scoped>



.Title{
  padding: 10px;
  margin-left: 20px;
  color: #4169E1;
}
.Title-name{
  font-size: 30px;
  font-weight: 600;
}

.icon {
  margin: 10px;
  gap: 10px;
  display: flex;
}
.data-users{
  display: flex;
}

.user-name a{
  display: inline-block;
    color: #000; /* Цвет обычной ссылки */
    margin-top: 8px;
    font-size: 20px;
    font-weight: 700;
    line-height: 1;
    text-decoration: none; /* Убираем подчеркивание */
    cursor: pointer;
}
.user-name a::after{
  background-color: #000; /* Цвет линии при наведении на нее курсора мыши */
    display: block;
    content: "";
    height: 2px; /* Высота линии */
    width: 0%;
    -webkit-transition: width .3s ease-in-out;
    -moz--transition: width .3s ease-in-out;
    transition: width .3s ease-in-out;
}
.user-name a:hover:after,
.user-name a:focus:after {
    width: 100%;
}
.ava-users {
  background-color: black;
  width: 40px;
  height: 40px;
  float: left;
  margin-left: 20px;
  margin-right: 10px;
  border-radius: 50%;
}
.TheHeder-title {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: #FFFAFA;
  height: 90px;
  width: 100%;
}
</style>
