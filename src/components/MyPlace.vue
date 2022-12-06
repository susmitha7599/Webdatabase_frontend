<template>
    <div class="myplace">
        <div v-for="place in place" :key="place.id">
        <PlaceList :place="place"/>
        </div>
    </div>
</template>
<script>
import PlaceList from './PlaceList.vue'
export default{
    name:'MyPlace',
    components:{
        PlaceList
    },
    props:{
        place: Array
    }
}
</script>
<style scoped>
.myplace{
background-color: #2F435A ;
padding:1em;
border: 0.3em solid black;
color:grey;
}
    </style>
