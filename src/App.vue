<template>
  <Navbar />
  <router-view :bookList="booksData" @store="storeData" 
  @update="updateData" @delete="deleteData"/>
</template>

<script>

import Navbar from "./components/Navbar.vue";
export default {
  name: 'App',
  components: { Navbar },
  methods: {
    storeData(bookCreated){
      console.log(bookCreated);
      alert("Data berhasil ditambahkan");
    },
    updateData(bookChange, bookIndex){
      console.log(bookChange, bookIndex);
      alert("Data Berhasil diperbarui!")
    },
    deleteData(book, index){
      console.log(book);
      console.log(index);
      alert("Data berhasil dihapus");
    },
  },
  data(){
    return {
      // datanya
      booksData: [
        {_id : 1, judul : "Laskar Pelangi", pengarang: "Andrea Hirata", harga: 80000, stok: 7},
        {_id : 2, judul : "Bumi", pengarang: "Tere Liye", harga: 85000, stok: 5}
      ],
    };
  },
  // methods: {
  //   retrieve(namamu) {
  //     this.dataNama = namamu;
  //     alert("Nama diterima: " + this.dataNama);
  //   }
  // }
};
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
