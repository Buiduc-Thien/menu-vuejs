<template>
<div class="container"> 
  <ul id="Level1">
    <li><a href="#">Home</a></li>
    <li><a
    @click.prevent="isActive = !isActive"
     href="#">Product</a>
    <ul v-show="isActive">
      <li><a href="#">None</a></li>
      <li><a href="#">None</a></li>
      <li><a href="#">None</a></li>
    </ul>
    </li>
    <li><a href="#">More</a></li>
  </ul>
</div>
</template>

<script>
export default {
  data(){
    return{
      isActive: false
    }
  },
  

}
</script>

<style>

*{
  box-sizing: border-box;
}
div{
  animation: mymove 5s infinite;
}
@keyframes mymove {
0% {background-color: #45CEEF;} 
25% {background-color: #FFF5A5;}
 50% {background-color: #FFD4DA;}
 75% {background-color: #99D2E4;}
100% {background-color: #D8CAB4;}
}
ul#Level1>li{
  position: relative;
  display: inline-block;
  padding: 0px 15px;
  font-size: 20px;
  text-transform: uppercase;
  letter-spacing: 1px;
}
ul li a{ 
  background-color: coral;
  list-style: none;
  color: black;
  text-decoration: none;
}
ul li>ul{
  list-style: none;
  position:absolute;
}
</style>