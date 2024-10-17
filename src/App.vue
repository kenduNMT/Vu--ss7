<script setup lang="ts">
import { ref } from 'vue';
import Slots from './components/Slots.vue';
import ParentComponent from './components/bt1/ParentComponent.vue';
import ProductParent from './components/bt2/ProductParent.vue';
import CountParent from './components/bt3/CountParent.vue';
import TodoApp from './components/bt4/TodoApp.vue';
import ModalParent from './components/bt5/ModalParent.vue';
import CardParent from './components/bt6/CardParent.vue';
import MessageParent from './components/bt7/MessageParent.vue';
import ListUser from './components/bt8/ListUser.vue';
import BaseButton from './components/bt9/BaseButton.vue';

// import HelloWorld from './components/Props.vue'
// let userList = [{ id: 1, name: "Hạ" }]
// let title = "hello"
// let slotName = ref('slotC');

// function changeSlot() {
//   console.log("đã vào")
//   if (slotName.value == 'slotC') {
//     slotName.value = 'slotB';
//   } else {
//     slotName.value = 'slotC';
//   }
// }
</script>

<template>

    <!-- <h1>Đây là cha</h1> -->
    
  <!-- <h1>Component Cha</h1>
  <Slots>
    <template #slotA={task}>
      <button>Click Me {{ task }}</button>
    </template>
    <template #slotB>
      <button>Click me Now!</button>
    </template>
    <template #[slotName]>
      <div>
        <button @click="changeSlot">Click Me AAAAAA </button>
      </div>
    </template>
  </Slots> -->
  <ParentComponent/>
  <ProductParent/>
  <CountParent/>
  <TodoApp/>
  <ModalParent/>
  <CardParent/>
  <MessageParent/>
  <ListUser/>
  <!-- Sử dụng với slot -->
<BaseButton type="submit" @click="handleSubmit">
  Submit
</BaseButton>

<!-- Sử dụng với prop children -->
<BaseButton 
  type="reset"
  children="Reset"
  @click="handleReset"
/>

<!-- Sử dụng với onClick prop -->
<BaseButton
  type="button"
  :onClick="handleCancel"  
>
  Cancel
</BaseButton>
</template>

<style scoped>
/* .n {
  text-align: center
} */
</style>
