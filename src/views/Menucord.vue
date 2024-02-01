<template>
  <div class="menu">
  <div>
    <h1>Menu</h1>
    <div class="list_menu">
      <ul>
        <li><RouterLink to="/" >Главная</RouterLink></li>
        <li><RouterLink to="/about" >Личный профиль</RouterLink></li>
        <li><a href="#">Уведомления</a></li>
        <li><a href="#"></a></li>
        <li><a href="#">Поддержка</a></li>
      </ul>
    </div>
</div>
    <div class="portner">
    <p>Data Create - 31-01-2024</p>
    </div>
  </div>
  
</template>
<script>
export default {
};
</script>

<style scoped>
h1{
    font-size: 40px;
    margin: 40px;
    color: white;
}
li{
    padding: 10px;
}
a{
    color: white;
  transition: 0.4s;
  font-weight: 600;
  border-radius: 10px;
  font-size: 20px;
}
.portner{
    color: white;
  transition: 0.4s;
  font-weight: 600;
  border-radius: 10px;
  font-size: 20px;
}
.menu {
    display:flex;
    flex-direction:column; 
    justify-content: space-between;
  position: fixed;
  background: rgba(20, 20, 20, 0.8);
  height: 100vh;
  border-right:solid 12px white;
  left: -286px;
  transition: all 0.3s cubic-bezier(0, 0, 0.11, 0.93);
}
.menu:hover{
    left: 0;
    transition: all 0.3s cubic-bezier(0, 0, 0.11, 0.93);
}
.list_menu {
  margin-bottom: 50px;
}
.list_menu{
    margin: 25px 0;
}
</style>
