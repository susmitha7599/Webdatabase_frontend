<template>
    <div>
       <p><b>Destination:</b>  {{place.Destination}}<br>
        <b>TopAttraction:</b>  {{place.TopAttraction}}<br>
        <b>FamousActivity:</b> {{place.FamousActivity}}<br>
        <b>Cusine:</b>   {{place.Cusine}}<br>
        <b>Budget:</b>   {{place.Budget}}<br>
        <b>Best time to visit:</b>   {{place.Besttimetovisit}}<br>
       </p>
    </div>
</template>
<script>
export default{
    name:'PlaceList',
    props:{
        place: Array
    }
}
</script>
<style scoped>
h4{
    margin: 2px;
}

div{
    background-color: #D0B49F;
    color: black;
    padding: 1em;
    border: 0.3em solid black;
    font-family: sans-serif;
}




</style>