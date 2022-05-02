<template>
    <div>

        <h1>{{movieobj.title}}</h1>
        <h1>Movie Deatails: {{movieobj.overview}}</h1>

    </div>

    
</template>

<script>
import axios from "axios"
export default{
    name:"MovieDetail",
    data(){
        return{
            id:this.$route.params.id,
            movieobj: Object
        }
    },
    mounted(){
        const request=`https://api.themoviedb.org/3/movie/${this.id}?api_key=5134b3f56c2cae575bb0ad435f0be5ee&language=en-US`
        console.log(request)

        axios.get(request)
        .then( (request)=>{
            this.movieobj = request.data
            console.log(this.movieobj)
        })
        
    }
    

}
</script>
