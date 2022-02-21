<template>
  <div>
    <Header />
    <div class="Apps">
      <h2>
        Count Apps
      </h2>
      <p id="increase_count">
        0
      </p>
      <button class="btn" @click="increase()">
        Increase Namber
      </button>
      <button class="btn" @click="save()">
        Save Namber
      </button>
      <button class="btn" @click="reset()">
        Reset Namber
      </button>
      <p id="save_count">
         last Namber is 
      </p>
    </div>
    <div>

    </div>
  </div>
</template>
<script>
export default {
  data(){
    return{
      count:0,
      
    };
  },
  methods:{
    increase(){
      this.count += 1;
      document.getElementById("increase_count").innerText = this.count
    },
    save(){
      document.getElementById("save_count").innerText = document.getElementById("save_count").innerText +" "+ this.count + " - "
      this.count = 0;
      document.getElementById("increase_count").innerText = this.count
    },
    reset(){
      this.count = 0;
      document.getElementById("increase_count").innerText = this.count
      document.getElementById("save_count").innerText = "last Namber is "
    }
  }

}
</script>
<style scoped>
.Apps{
  text-align: center;
}
.Apps p{
  margin: 100px auto;
  font-size: 30px;
}
.btn{
  padding: 20px 30px;
  background-color: black;
  color: white;
}
</style>