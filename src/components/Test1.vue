<template>
  <div>
    Hii this is test1
    <button @click="$emit('buttonpressed', 'button_is_pressed for Test1')">
      Click here
    </button>
  </div>
</template>