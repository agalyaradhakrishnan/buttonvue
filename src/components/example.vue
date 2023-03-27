<template>
    <div class="one">
        <p>Current count: {{ count }}</p>
    <button @click="increment" >Increment</button>
  </div>
  <div class="tow">
    <button @click="greet">Click me!</button>
  </div>
  <div class="three">
    <button @click="showDateTime">Click me!</button>
    <p v-if="dateTime">{{ dateTime }}</p>
  </div>
</template>

<script>
    export default {
        data(){
            return{
                count: 0,
               dateTime: ''
            }
        },
        watch: {
    count(newValue, oldValue) {
      console.log(`count changed from ${oldValue} to ${newValue}`)
    }
  },
   methods:{
    increment() {
        this.count++
      },
      greet() {
        alert('Hello, world!')
      },
      showDateTime() {
        this.dateTime = new Date().toLocaleString()
      }
   
}
    }
</script>

<style scoped>
*{
  margin:0;
  padding:0
}
button{
  padding: 10px 7px;
  border-radius: 20px;
  background-color: blue;
  color: white;
}
.one{
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: darkorange;
  min-width: 50%;
  min-height: 75%;
  padding: 5% 5%;
}
.tow{
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: rgb(0, 255, 13);
  min-width: 50%;
  min-height: 75%;
  padding: 5% 5%;

}
.three{
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: rgb(0, 217, 255);
  min-width: 50%;
  min-height: 75%;
  padding: 5% 5%;
}
</style>