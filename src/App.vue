<template>
  <div class="container">
    <HeaderTop appName="Wanderlust" tagName="~Lets Explore"/>
    <MyPlace :place="place" />
  </div>
</template>
<script>
import HeaderTop from './components/HeaderTop.vue'
import MyPlace from './components/MyPlace.vue'
export default{
  name: 'App',
  components: {
    HeaderTop,
    MyPlace
  },
  data(){
    return{
      place:[]
    }
  },

  methods: {

    async fetchPlaces(){
      const res = await fetch("https://wanderlust7.herokuapp.com/api")
      const data = await res.json()
      console.log("Data is", data )
      return data.place
    }
  },
  async created(){
    this.place = await this.fetchPlaces()
  }
}
</script>
<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
*{
box-sizing: border-box;
margin: 0;
padding: 0;
background-image: url(image.jpg);


}
body{
  font-family: 'Montserrat', sans-serif;

}
.container {
  max-width: 450px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
  background-color: #39918C;
}

div{
  margin-bottom: 0.5em;
}
</style>