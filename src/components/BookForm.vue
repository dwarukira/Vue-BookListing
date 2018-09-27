<template>
    <form v-on:submit.prevent="bookSubmit(booksTitle, bookAuthor)" class="" action="#" method="post">
        <input v-model="booksTitle" type="text" name="title" value="" placeholder="Book Title">
        <input v-model="bookAuthor" type="text" name="author" value="" placeholder="Book Author">
        <button type="submit" name="button">Add Book</button>
    </form>
</template>

<script>
export default {
    name: 'BookForm',
    props:['books'],

    data() {
        return {
            booksTitle:"",
            bookAuthor:"",
        }
    },
    methods: {
        bookSubmit(booksTitle, bookAuthor){
            this.$emit('addBook', booksTitle, bookAuthor);
        }
    }
}
</script>

<style>

</style>
