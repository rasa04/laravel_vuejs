<template>
    <div>
        <SinglePostComponent></SinglePostComponent>
    </div>
</template>

<script>
import SinglePostComponent from "./SinglePostComponent";
export default {
    name: "PostComponent",

    data(){
        return {
            
        }
    },

    mounted(){
        this.getPosts()
    },

    methods:{
        getPosts(){
            axios.get('/posts')
            .then(function(data){
                console.log(data.data);
            })
        },
    },

    computed: {
         
    },

    components:{
        SinglePostComponent
    }
}
</script>
<!-- scope нужен для того что бы стили действовали только в рамках темплейта -->
<style scoped> 
 
</style>