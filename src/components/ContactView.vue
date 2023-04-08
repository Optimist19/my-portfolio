<template>
  <div class="con">
    <div class="i-a-div">
      <!-- <p>Hello world</p> -->
      <a href="https://www.linkedin.com/in/oluwasegun-bamidele/" target="_blank">
        <i class="fa-brands fa-linkedin fa-bounce"></i>
      </a>
      
      <a href="https://twitter.com/optimist_BGO" target="_blank">
        <i class="fa-brands fa-twitter fa-bounce"></i>
      </a>
      <i class="fa-solid fa-envelope fa-beat-fade"></i>
      <span>oluwasegunbamidele3@gmail.com</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeView',
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.i-a-div{
  padding-top: 3vh;
  padding-bottom: 3vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

i{
  color: green;
  font-size: 20px;
}

a{
 margin: 0 0.5vw;
 font-size: 20px;
 color: green
}

span{
  text-decoration: none;
  color: rgb(250, 249, 246);
	font-family: 'Montserrat Alternates', sans-serif;
  font-size: 20px;
  margin: 0 0.5vw;
}



@media only screen and (max-width: 574px) {
  a, span{
    font-size: 14px;
  }
  i{
    font-size: 14px;
  }
}
@media only screen and (max-width: 375px) {

  a, span{
    font-size: 10px;
  }
  i{
    font-size: 10px;
  }
}
</style>
