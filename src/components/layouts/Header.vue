<template>
<div class="header">
    <h1>Logo</h1>
     <div class="navigations">
      <router-link to="/" class="home">Home</router-link>
      <!-- <router-link to="/about" class="about">List of Todo's</router-link> -->
    </div>
</div>
</template>
<script>
export default {
    name: 'Header'
}
</script>
<style scoped>
.header h1{
  padding: 20px;
}
.header{
    text-align: center;
    background-color: rgb(155, 43, 43);
    color: white;
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.navigations{
  color: #fff;
  text-decoration: none;
  padding: 20px;
  
}
.navigations a{
  padding-left: 20px;
}
.home:hover{
  color: #42b983;
}
.about{
  color: #fff;
  text-decoration: none;
    padding-left: 5px;
}
.about:hover{
   color: #42b983;
}


</style>