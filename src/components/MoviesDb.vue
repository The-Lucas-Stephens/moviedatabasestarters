<template>
    <div>
        <h1>Upcoming Movies</h1>
        <div v-bind:key="movie.id" v-for="movie in movies" >
            <h3>{{movie.title}}</h3>
            <router-link :to="`/movie/${movie.id}`"> Details for: {{movie.title}}</router-link>
        </div>
    </div>
</template>

<script>
import axios from "axios"
export default{
    name:"MoviesDb",
    data(){
        return{
            movies:[]
        }
    },
    mounted(){
        axios
        .get(
          "https://api.themoviedb.org/3/movie/upcoming?api_key=5134b3f56c2cae575bb0ad435f0be5ee&language=en-US&page=1"
        )
        .then((response) => {
          console.log(response);
          this.movies= response.data.results
          console.log(this.movies);
  
          return this.someMovies;
        })
        .catch((err) => {
          console.log(err);
        });
    }
}


</script>
