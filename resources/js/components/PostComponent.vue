<template>
    <div>
        <SinglePostComponent></SinglePostComponent>
        <div>Name: {{name}}</div>
        <div>Job: {{vasyaJob}}</div>
        <button @click="sayHello">Hello</button>
        <button @click="sayHi">Hi</button>
    </div>
</template>

<script>
import SinglePostComponent from "./SinglePostComponent";
export default {
    name: "PostComponent",

    data(){
        return {
            name: "Вася",
            age: 20,
            boolean:true,
            someNull: null,
            arr: [
                [],
            ],
            someObj: {
                personName: 'Ivan'
            }
        }
    },

    methods:{
        sayHello(){
            document.write('Hello')
        },
        sayHi(){
            console.log('Hi')
        }
    },

    computed: {
        vasyaJob(){
            return this.name + ' работает в булошной'
        }
    },

    components:{
        SinglePostComponent
    }
}
</script>
<!-- scope нужен для того что бы стили действовали только в рамках темплейта -->
<style scoped> 
 
</style>