<template>

  <div align="center">
    <div class="titles">
      <h5>Find me on social</h5>
    </div>
    <div class="social">
  <!--    <div class="titles"></div>-->
        <a href="https://instagram.com/chrisfunpics" target="_blank" class="fa fa-instagram"></a>
        <a href="https://twitter.com/chris__karlson" target="_blank" class="fa fa-twitter"></a>
        <a href="https://www.linkedin.com/in/christopher-karlson-787058135/" target="_blank" class="fa fa-linkedin"></a>
        <a href="https://github.com/ckarlson14" target="_blank" class="fa fa-github"></a>
        <a href="mailto:ckarlson14@gmail.com" target="_blank" class="fa fa-envelope"></a>
    </div>
  </div>
</template>

<script>
export default {
  name: "Social.vue"
}
</script>

<style scoped>

.social{
  max-width: 70%;
  display: flex;
  flex-wrap: wrap;
}

.fa {
  padding: 10px;
  font-size: 2rem;
  text-align: center;
  text-decoration: none;
  border-radius: 50%;
}


a{
  color: #e853e7;
  text-decoration: none;
}

a:hover, .fa.fa-instagram:hover{
  color:cyan;
}

.fa-linkedin {
  color: #0976b4;
}

.fa-github {
  color: #333;
}

.fa.fa-instagram {
  color: transparent;
  background: radial-gradient(circle at 30% 107%, #fdf497 0%, #fdf497 5%, #fd5949 45%, #d6249f 60%, #285AEB 90%);
  background: -webkit-radial-gradient(circle at 30% 107%, #fdf497 0%, #fdf497 5%, #fd5949 45%, #d6249f 60%, #285AEB 90%);
  background-clip: text;
  -webkit-background-clip: text;
}

.fa-twitter{
  color: #55acee;
}


</style>