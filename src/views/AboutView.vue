<template>
  <div class="ContentAcn">
    <h1 class="user-name-acc">Добро пожаловать !имя!</h1>
    <div class="images-base">
    <div class="contentANCA">
      <div class="image"></div>
      <input type="file" class="button-images">
    </div>
    </div>
  </div>
</template>

<script></script>

<style>
.images-base {
  background-color: #b87b5c;
  display: flex;
  border-radius: 10px;
  align-items: flex-end;
  margin: 10px;
  box-shadow: 5px 5px 5px 0px rgb(0, 0, 0, 0.55);

}
.button-images {
  padding: 10px;
  margin-left: 80px;
  border-radius: 10px;
  border: solid 1px;
  background-color: #90533b;
  box-shadow: 5px 5px 5px 0px rgb(0, 0, 0, 0.55);
  margin-bottom: 10px;
}
.user-name-acc {
  margin: 30px;
  background-color: #b87b5c;
  padding: 10px;
  border-radius: 10px;
  box-shadow: 5px 5px 5px 0px rgb(0, 0, 0, 0.55);
}
.image {
  background-color: grey;
  height: 250px;
  width: 250px;
  border-radius: 50px;
  box-shadow: 5px 5px 5px 0px rgb(0, 0, 0, 0.55);
  margin: 30px;
}

  .ContentAcn {
    background-color: #f4ddb8;
    height: 100vh;
    width: auto;
    margin: 50px;
    border-radius: 20px;
  }
</style>
