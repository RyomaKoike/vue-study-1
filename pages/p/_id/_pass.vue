<template>
    <section class="container">
        <h1>{{title}}</h1>
        <p v-html="message">no message</p>
        <hr>
        <div class="right">
            <router-link to="/">Go to Top</router-link>
        </div>
    </section>
</template>

<script>
export default {
    data: function() {
        return {
            title: 'Login',
        };
    },
    computed: {
        message: function() {
            let id = this.$route.params.id != undefined
                ? this.$route.params.id : '*** no id ***';
            let pass = this.$route.params.pass != undefined
                ? this.$route.params.pass : '*** no pssword';
            return 'ID:' + id + '<br>PASS:' + pass;
        },
    },
}
</script>

<style>
.container {
    padding:5px 10px;
}

h1 {
    font-size:60px;
    color: #345980
}

p {
    padding-top:5px;
    font-size: 20px;
}

a {
    font-size: 16px;
}

.right {
    text-align: right;
}

</style>