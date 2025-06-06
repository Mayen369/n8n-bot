<template>
  <div v-if="message.text">
    <slot name="beforeMessage" />
    <div class="chat-message">{{ message.text }}</div>
  </div>
</template>

<script>
export default {
  props: {
    message: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style scoped>
.chat-message {
  background-color: #f1f1f1;
  padding: 10px;
  margin: 5px 0;
  border-radius: 4px;
  font-family: sans-serif;
}
</style>
fix: corregido Message.vue que causaba error de compilación
