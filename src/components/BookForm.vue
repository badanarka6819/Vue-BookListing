<template>
    <form action="#" method="post">
        <input type="text" name="title" value="" placeholder="Book Title" v-model="bookTitle">
        <input type="text" name="author" value="" placeholder="Book Author" v-model="bookAuthor">
        <button type="submit" name="button" @click.prevent="bookSubmit()">Add Book</button>
    </form>
</template>

<script>
    export default {
        name:'BookForm',
        props: ['books'],
        data:{
            return: {
              bookTitle:
              {
                type: String,
                default: '',
              },
              bookAuthor:{
                type: String,
                default: '',
              },
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