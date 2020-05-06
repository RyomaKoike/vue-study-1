<template>
  <section class="container">
    <h1>{{title}}</h1>
    <p>{{message}}</p>
    <hr>
    <pre>{{now}}</pre>
  </section>
</template>

<script>
export default {
  data: function() {
    return {
      title: 'hello',
      message: 'hello too',
      now: 'wait.....'
    };
  },
  created: function() {
    setInterval (()=>{
      var d = new Date();
      this.now = d.getHours()
          + ':' +  d.getMinutes()
          + ':' +  d.getSeconds();
    }, 1000);
  }
}
</script>

<style>
.container {
  padding: 5px 10px;
}

h1 {
  font-size: 60px;
}

p {
  padding-top: 5px;
  font-size: 20px;
}

pre {
  padding: 10px;
  font-size: 10px;
  background-color: #efefef;
}

hr {
  margin:10px 0px; 
}


</style>
