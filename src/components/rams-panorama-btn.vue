<template>
  <div class="btn">
    <button @click="moveLeft">
      <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-caret-left-fill" viewBox="0 0 16 16">
        <path d="m3.86 8.753 5.482 4.796c.646.566 1.658.106 1.658-.753V3.204a1 1 0 0 0-1.659-.753l-5.48 4.796a1 1 0 0 0 0 1.506z"/>
      </svg>
    </button>
    <button @click="moveRight">
      <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-caret-right-fill" viewBox="0 0 16 16">
        <path d="m12.14 8.753-5.482 4.796c-.646.566-1.658.106-1.658-.753V3.204a1 1 0 0 1 1.659-.753l5.48 4.796a1 1 0 0 1 0 1.506z"/>
      </svg>
    </button>
  </div>
</template>

<script>
export default {
  methods: {
    moveLeft() {
      this.$emit('move', 'left');
    },
    moveRight() {
      this.$emit('move', 'right');
    },
  },
};
</script>

<style>
.btn {
  margin-top: 10px;
}

 button {
  background: linear-gradient(90deg, #3D7369 0%, #60AB9E 100%);
  width: 50px;
  height: 50px;
  border-radius: 3px;
  outline: none;
  border: none;
  color: white;
  margin-left: 30px;
}
</style>
