<template>
    <div>
        <h1>Upcoming Movies</h1>
        <div v-for="movie in movies" :key=movie.id>
            {{movie.title}} >>
            <router-link :to="`/movie/${movie.id}`">
            {{movie.id}}
            </router-link>
        </div>
      
    </div>
</template>

<script>
import axios from 'axios'
export default{
    name:"MoviesDb",
    data(){
        return {
            movies: []
        }
    },
    mounted(){
        axios.get("https://api.themoviedb.org/3/movie/now_playing?api_key=61f54a9dd1f5656234a1d2305506db0a&language=en-US&page=1")
        .then ((response) => {
            this.movies = response.data.results;
            console.log(this.movies)
        })
    }
}
</script>
