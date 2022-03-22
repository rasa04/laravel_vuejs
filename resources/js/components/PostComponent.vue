<template>
    <div>
        <SinglePostComponent></SinglePostComponent>
        <table class="table">
        <thead>
            <tr>
            <th scope="col">#</th>
            <th scope="col">Name</th>
            <th scope="col">Age</th>
            <th scope="col">Job</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="(person, index) in personsAgeMoreTwenty" v-if="person.age > 20">
                <th scope="row">{{index}}</th>
                <td>{{ person.name }}</td>
                <td>{{ person.age }}</td>
                <td>{{ person.job }}</td>
            </tr>
        </tbody>
        </table>
    </div>
</template>

<script>
import SinglePostComponent from "./SinglePostComponent";
export default {
    name: "PostComponent",

    data(){
        return {
            persons: [
                {
                    name: 'Вася',
                    age: 20,
                    job: 'coach'
                },
                {
                    name: 'Елена',
                    age: 17,
                    job: 'rest'
                },
                {
                    name: 'Петр',
                    age: 34,
                    job: 'seller'
                },
                {
                    name: 'Ксюша',
                    age: 25,
                    job: 'traveller'
                },
                {
                    name: 'Олья',
                    age: 21,
                    job: 'Teacher'
                },
            ]
        }
    },

    methods:{

    },

    computed: {
        personsAgeMoreTwenty() {
            return this.persons.filter(function(person){
                return person.age > 20
            })
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