<template>
  <div>
    Hii this is test
    <button @click="$emit('buttonpressed', 'button_is_pressed for Test')">
      Click here
    </button>
  </div>
</template>