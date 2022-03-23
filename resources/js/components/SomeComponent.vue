<template>
    <div class="w-25">
    <div class="">Color: {{ obj.color }}</div>
    <div class="">Number: {{ obj.number > 10 ? 'more than 10' : 'less than 10'}}</div>
    <div class="">Is published: {{ obj.isPublished ? 'Published' : "Not published" }}</div>
    </div>
</template>

<script>    
export default {
    name: "SomeComponent",

    data() {
        return {
            
        }
    },

    props: [
        'obj'
    ],

    mounted() {
        this.$parent.$parent.parentLog();
    },

    methods: {

    }

}
</script>
<style scoped> 
 
</style>