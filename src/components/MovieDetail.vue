<template>
    <div>
        <h1>{{movieobj.title}}</h1>
        <p>{{id}}</p>
    </div>
</template>

<script>
import axios from 'axios'
export default{
    name: "MovieDetail",
    data(){
        return{
            id:this.$route.params.id

        }
    },
    mount(){
        const request = `https://api.themoviedb.org/3/movie/${this.id}?api_key61f54a9dd1f5656234a1d2305506db0a&language=en-US`
        console.log(request)
        axios.get(request)
        .then((response) =>{
            this.movieobj = response.data
        })
    }
}
</script>