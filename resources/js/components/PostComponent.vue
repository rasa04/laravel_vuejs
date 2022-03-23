<template>
    <div>
        <CreateComponent></CreateComponent>
        <IndexComponent ref="index"></IndexComponent>
     <!--    <table class="table">
        <thead>
            <tr>
            <th scope="col">#</th>
            <th scope="col">Name</th>
            <th scope="col">Age</th>
            <th scope="col">Job</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="(person, index) in persons">
                <th scope="row">{{index}}</th>
                <td>{{ person.name }}</td>
                <td>{{ person.age }}</td>
                <td>{{ person.job }}</td>
            </tr>
        </tbody>
        </table> -->
    </div>
</template>

<script>
import CreateComponent from "./CreateComponent";
import IndexComponent from "./IndexComponent";
export default {
    name: "PostComponent",

    data(){
        return {
            persons: null
        }
    },

    mounted() {
        console.log(this.$refs.index.indexLog());
    },

    methods:{
        parentLog() {
            console.log('this is parent component');
        }
    },

    components:{
        CreateComponent,
        IndexComponent
    }
}
</script>
<!-- scope нужен для того что бы стили действовали только в рамках темплейта -->
<style scoped> 
 
</style>