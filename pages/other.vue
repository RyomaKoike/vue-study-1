<template>
    <section class="container">
        <h1>{{title}}</h1>
        <p>{{message}}</p>
        <hr>
        <router-link to="/">Go to Top</router-link>
    </section>
</template>

<script>
export default {
    data: function() {
        return {
            title:'Other',
            message:'これは、別のページ',
        };
    },
}
</script>

<style>
.container {
    padding: 5px 10px;
}

h1 {
    font-size:60p; 
    color:#345980
}

p {
    padding-top: 2px;
    font-size: 20px;
}

a {
    font-size: 10px;
}
</style>