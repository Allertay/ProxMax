<template>
  <div class="promer">
    <div class="poisk">
    <button class="button-poisk">поиск</button>
      <input class="poisk-data-object" />
    </div>
  </div>
  <div class="content">
    <div class="container-title">
    <div></div>
      <p class="title-spis">список объявлений</p>
      <div class="creat">
      <button class="creat-button"><p class="plusek">+</p></button>
      </div>
    </div>
  </div>
</template>
<script>
export default {

  data(){
    return{

    }
  }
}
</script>

<style scoped>
.plusek{
  color: black;
  font-weight: 900;
  font-size: 25px;
}
.creat{
margin: 5px 9px 0px 0px;
}
.creat-button{
  cursor: pointer;
  padding: 5px 13px;
  border-radius: 50%;
  background-color: lightblue;
  border: solid 1px transparent;
  transition: all 0.3s cubic-bezier(0, 0, 0.11, 0.93);
}
.creat-button:hover{
  cursor: pointer;
  padding: 5px 13px;
  border-radius: 50%;
  background-color: rgb(126, 186, 206);
  border: solid 1px black;
  transition: all 0.3s cubic-bezier(0, 0, 0.11, 0.93);
}
.title-spis{
  color: azure;
  padding: 10px;
  font-weight: 500;
  font-size: x-large;
  text-decoration: underline;
}
.container-title {
  background-color: black;
  display: flex;
  height: 50px;
  display: flex;
  justify-content: space-between;
  width: auto;
  border-radius: 6px;
  margin: 10px;
}
.content {
  background-color: azure;
  margin: 50px;
  width: auto;
  height: 100vh;
  border-radius: 10px;
  text-align: center;
}
.promer {
  margin-top: 20px;
  height: 50px;
  width: 100%;
}
.poisk {
  padding: 15px;
  display: flex;
  justify-content: center;
}
.poisk-data-object{
  border-radius: 5px;
  border: solid 1px black;
  padding: 8px 170px 0px 0px;
}
.button-poisk{
  margin-right: 10px;
  border-radius: 7px;
  border: solid 1px black;
  cursor: pointer;
  transition: all 0.3s cubic-bezier(0, 0, 0.11, 0.93);
  box-shadow: 0px 1px 5px 1px rgb(20, 20, 20);
}
.button-poisk:hover{
  background-color: lightgray;
  margin-right: 10px;
  border-radius: 7px;
  border: solid 1px black;
  cursor: pointer;
  box-shadow: 0px 1px 5px 2px rgb(36, 36, 36);
  transition: all 0.3s cubic-bezier(0, 0, 0.11, 0.93);
}
</style>
