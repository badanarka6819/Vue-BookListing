<template>
    <form v-on:submit.prevent="bookSubmit(bookTitle,bookAuthor)" action="#" method="post">
        <input v-model="bookTitle" type="text" name="title" value="" placeholder="Book Title" v-model="bookTitle">
        <input v-model="bookAuthor" type="text" name="author" value="" placeholder="Book Author" v-model="bookAuthor">
        <button type="submit" name="button" >Add Book</button>
    </form>
</template>

<script>
    export default {
        name:'BookForm',
        props: ['books'],
        data:{
            return: {
              bookTitle:'',
              bookAuthor:'',
            }
        },
        methods: {
            bookSubmit: function(bookTitle, bookAuthor) {
               this.$emit('addBook',bookTitle,bookAuthor); 
            }
        },
    }
</script>

<style>

</style>