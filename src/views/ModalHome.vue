<template>
  <div class="window">
    <div class="window__container">
      <form @submit.prevent="submitEdit">
        <input
          v-model="infoobjavl.heading"
          type="text"
          required
          placeholder="Введите заголовок объявления"
        />
        <input
          v-model="infoobjavl.description"
          type="text"
          required
          placeholder="Введите описание объявления"
        />
        <input
          v-model="infoobjavl.price"
          type="text"
          required
          placeholder="Введите цену"
        />
        <input
          v-model="infoobjavl.phone"
          type="text"
          required
          placeholder="Введите номер телефона"
        />
        <div class="button-mas">
          <button type="button" @click.prevent="closeEdit" class="cancel-btn">
            Отмена
          </button>
          <button type="submit" @click.prevent="submitEdit" >Создать</button>
        </div>
      </form>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      infoobjavl: {
        heading: '',
        description: '',
        price: '',
        phone: '',
      },
    };
  },

  methods: {
    submitEdit() {
      this.infoobjavl.id = Date.now()
      this.$emit('create', this.infoobjavl)
      this.infoobjavl={
        heading: '',
        description: '',
        price: '',
        phone: '',
      }
    },
    closeEdit() {
      this.$emit("close-modal");
    },
    resetform(){
    this.infoobjavl = {heading:'', description:'', price:'',phone:''}
    },
    
  },
};
</script>
<style>
.button-mas {
  display: flex;
  justify-content: space-between;
}
.window {
  display: flex;
  justify-content: center;
  align-items: center;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgb(255 255 255 / 33%);
  backdrop-filter: blur(15px);
}
.window__container {
  display: flex;
  background-color: white;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
  width: 430px;
}

form {
  display: flex;
  width: 100%;
  flex-direction: column;
  gap: 10px;
}

input[type="text"],
textarea {
  padding: 10px;
  border: 1px solid #ddd;
  border-radius: 5px;
}

textarea {
  resize: vertical;
}

button[type="submit"] {
  padding: 10px 20px;
  background-color: #455947;
  color: black;
  border: solid 1px;
  border-radius: 5px;
  cursor: pointer;
}

button[type="submit"]:hover {
  background-color: #c9d9c3;
}

.cancel-btn {
  padding: 10px 20px;
  background-color: bisque;
  color: black;
  border: solid 1px;
  border-radius: 5px;
  cursor: pointer;
}

.cancel-btn:hover {
  background-color: blanchedalmond;
}
</style>
