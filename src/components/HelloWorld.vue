<template>
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
  <div class="text">
    Current number of stones <p class="Num">
      {{ counter }}
    </p>
  </div>

  <div>
    <div class="text2">
      <!-- floor(&#8730;N) =  {{ Math.floor(Math.sqrt(counter)) }}  -->
      <img src="../components/Photu.png" />{{ Math.floor(Math.sqrt(counter)) }} 

    </div>
  </div>

  <div id="marbles1">
    <div v-if="counter > 0">
      <div class="m1" v-for="n in counter">
        <img src="../components/new_marble.png" />
      </div>
    </div>
  </div>

  <div id="marbles2">
    <div v-if="counter<1" class="game-over">Game Over.</div>
  </div>
  <br />
  <button @click="increment" class="btn btn-primary m-1 p-auto">+</button>
  <button @click="decrement" class="btn btn-primary m-1 p-auto">-</button>
  <br />
  <br />
  <br />

  <footer>Made by Abhishek</footer>
  <footer></footer>

</template>

<script>
export default {
  // name: 'HelloWorld',
  // props: {
  //   msg: String
  // }
  data() {
    return {
      counter: 15,
      x: 0,
    };
  },
  methods: {
    increment() {
      this.counter++;
    },
    decrement() {
      this.counter--;
    },
  },
};
</script>

<style>
  /* body{
    background-color: black;
  } */
  .game-over{
  color:white;
  font-weight:900;
  font-size:xx-large;
  font-family: Arial, Helvetica, sans-serif;
  text-align: center;
  padding: auto;
  padding: 10px;
  }
  .Num{
    font-size: 110px;
  }
footer {
  color:white;
  /* font-weight: 800; */
  font-size: x-large;
  font-family: Arial, Helvetica, sans-serif;
  text-align: right;
  padding: auto;
  padding: 10px;
  margin: 5px;
}
#marbles1 {
  margin-bottom: 100px;
}
#marbles2 {
  margin-bottom: 50px;
  font-size: 36px;
}
img {
  width: 120px;
  margin-left: -46px;
  text-shadow: 0 0 3px #ff0000, 0 0 5px #0000ff;
}
.m1 {
  display: inline;
}
.text {
  font-size: 36px;
  margin-bottom:20px;
  margin-top:0px
}
.text2 {
  font-size: 40px;
  margin-bottom:49px;
  /* font-style: roboto slab; */
}
#lol {
  font-size: 65px;
}
</style>
