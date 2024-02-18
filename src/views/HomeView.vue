<template>
  <ModalHome
    v-if="isEditModal"
    :isEditModal="this.isEditModal"
    @create="creatNewPost"
    @close-modal="onCloseModal"
  />
  <div class="content">
  <div class="content_container">
    <header class="container-title">
      <div></div>
      <p class="title-spis">Список услуг</p>
      <div class="creat">
        <button class="creat-button" @click="opemEdit">
          <p class="plusek">+</p>
        </button>
      </div>
    </header>
  </div>
          <div class="promer">
    <div class="poisk">
      <button class="button-poisk">поиск</button>
      <input
      v-model="serch"
      type="search"
      placeholder="поиск"
      class="poisk-data-object"
      size="50"/>
    </div>
  </div>
    <div class="objavlenia">
      <section class="objavlenia-news">
        <component class="post" v-for="post in filteredPosts" :key="post.heading">
          <div class="title-posts">
            <strong>Название:</strong>{{ post.heading }}
          </div>
          <div class="opis-posts">
            <strong>Описание:</strong>{{ post.description }}
          </div>
          <div class="opis-posts"><strong>Цена:</strong>{{ post.price }}</div>
          <div class="opis-posts"><strong>Телефон:</strong>{{ post.phone }}</div>
          <div>
            <button @click="buy" class="button_buy">Корзина</button>
            <!-- <button class="button_favorinte">Избранное</button> -->
          </div>
        </component>
      </section>
    </div>
  </div>
</template>
<script>
import ModalHome from "./ModalHome.vue";
export default {
  components: {
    ModalHome,
  },
  data() {
    return {
      isEditModal: false,
      serch: '',
      posts: [
        {
          id: 1,
          heading: "дворника",
          description: "описание 1",
          price: "1000",
          phone: "+79050518105"
        },
        {
          id: 2,
          heading: "WebDeveloper",
          description: "описание 2",
          price: "1000",
          phone: "+79050518105"
        },
        {
          id: 3,
          heading: "Backend",
          description: "описание 3",
          price: "1000",
          phone: "+79050518105"
        },
        {
          id: 4,
          heading: "Установка окон",
          description: "описание 4",
          price: "1000",
          phone: "+79050518105"
        },
        {
          id: 5,
          heading: "Механик",
          description: "описание 1",
          price: "1000",
          phone: "+79050518105"
        },
      ],
    };
  },

  methods: {
    opemEdit() {
      this.isEditModal = true;
    },
    onCloseModal() {
      this.isEditModal = false;
      
    },
    creatNewPost(infoobjavl) {
      console.log(infoobjavl);
      this.posts.push(infoobjavl);
      this.onCloseModal()
    },
    buy(){
      alert('новый товар в корзине')
    }
  },
  computed:{
    filteredPosts(){
      return this.posts.filter(Element=>{
        return Element.heading.includes(this.serch)
      })
    }
  }
};
</script>

<style scoped>

.promer{
  display: flex;
  justify-content: center;
  margin-top: 10px;
}
.button-poisk{
  padding: 6px;
  border-radius: 5px;
  border: solid 0px ;
  background-color: #4169E1;
  color: white;
  font-size: 15px;
  font-weight: 700;
  cursor: pointer;
}
.button-poisk:hover{
  padding: 6px;
  border-radius: 5px;
  border: solid 0px ;
  background-color: #304ea8;
  color: white;
  font-size: 15px;
  font-weight: 700;
}
.poisk-data-object{
  padding: 6px;
  border:  solid 2px #4169E1;
  border-radius: 10px;
  margin-left: 15px;
}
.content_container{
  display: flex;
  flex-direction: column;
  align-items: center;
}
.button_favorinte{
  background-color: rgb(235, 165, 124);
  padding: 5px;
  border: solid 0px;
  border-radius: 5px;
  margin: 5px;
  color: white;
  font-weight: 800;
  cursor: pointer;
  transition: all 0.2s cubic-bezier(0, 0, 0.11, 0.93);
}
.button_favorinte:hover{
  background-color: rgb(235, 134, 106);
  padding: 5px;
  border: solid 0px;
  border-radius: 5px;
  margin: 5px;
  cursor: pointer;
}
.button_buy{
  background-color: rgb(169, 206, 68);
  padding: 5px;
  border: solid 0px;
  border-radius: 5px;
  margin: 5px;
  color: white;
  font-weight: 800;
  cursor: pointer;
  transition: all 0.2s cubic-bezier(0, 0, 0.11, 0.93);
}
.button_buy:hover{
  background-color: rgb(138, 167, 58);
  padding: 5px;
  border: solid 0px;
  border-radius: 5px;
  margin: 5px;
  cursor: pointer;
}
.post {
  background-color: #f4ddb8;
  display: flex;
  width: 1900px;
  flex-direction: column;
  align-items: flex-start;
  margin: 10px;
  padding: 16px;
  border-radius: 10px;
}
.objavlenia-news {
  height: 70vh;
  overflow-y: auto;
  max-width: 2000px;
  background-color: #DCDCDC;
  margin-top: 20px;
  border-radius: 20px;
  border: solid 0px;
  scrollbar-color: #d4aa70 #e4e4e4;
  scrollbar-width: thin;
}
.objavlenia{
  display: flex;
  justify-content: center;
}
::-webkit-scrollbar {
  background-color: transparent;
  width: 0px;
}
.plusek {
  color: black;
  font-weight: 900;
  font-size: 25px;
}
.creat {
  margin: 5px 9px 0px 0px;
}
.creat-button {
  cursor: pointer;
  padding: 5px 13px;
  border-radius: 50%;
  background-color: #90533b;
  border: solid 0px transparent;
  transition: all 0.2s cubic-bezier(0, 0, 0.11, 0.93);
  box-shadow: 0px 2px 2px 0px rgb(0, 0, 0, 0.75);
}
.creat-button:hover {
  cursor: pointer;
  padding: 5px 13px;
  border-radius: 50%;
  background-color: #90533b;
  border: solid 0px transparent;
  transition: all 0.2s cubic-bezier(0, 0, 0.11, 0.93);
  box-shadow: 0px 2px 2px 0px rgb(0, 0, 0, 0.35);
}
.title-spis {
  color: black;
  padding: 10px;
  font-weight: 600;
  font-size: x-large;
  text-decoration: underline;
}
.container-title {
  background-color: #DCDCDC;
  min-width: 500px;
  height: 50px;
  display: flex;
  justify-content: space-between;
  border-radius: 6px;
  box-shadow: 0px 4px 12px 0px rgb(0, 0, 0, 0.65);
  margin: 10px;
}

.content {
  margin-top: 50px;
}
</style>
