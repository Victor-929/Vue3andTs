<template>
    <div class="person">
        <h2>汽车信息：一辆{{ car.brand }}车，价值{{ car.price }}万</h2>
        <button @click="changePrice">修改汽车价格</button>
        <button @click="changeBrand">修改汽车品牌</button>
        <button @click="changeCar">修改汽车</button>
        <hr>
        <h2>当前求和为：{{ sum }}</h2>
        <button @click="changeSum">点我sum+1</button>
    </div>
   
</template>


<script setup lang="ts" name="Person234">
import { reactive ,ref} from 'vue';

//数据
let car = reactive({brand:'奔驰',price:100})
let sum = ref(0)

function changePrice() {
    car.price += 10
}
function changeBrand(){
    car.brand = '保时捷'
}
function changeCar() {
    Object.assign(car,{brand:'奥迪',price:130})
}
function changeSum() {
    sum.value += 1
}

changePrice
changeBrand
</script>

<style scoped>
.person {
    background-color: #ddd;
    box-shadow: 0 0 10px;
    border-radius: 10px;
    padding: 20px;
}

button {
    margin: 0 5px;
}
li {
    font-size: 20px;
}
</style>