<template>
    <header>
      <input type="text" placeholder="Suche..." >
      <button class="bi bi-search"></button>
    </header>
</template>

<script>
    export default {
        name: 'Header',
        data() {
            return {
                search: String,
            }
        }
    }
</script>

  <style scoped>
  header {
    background-color: #f4bc39;
    height: 120px;
    padding: 16px;
    display: flex;
    align-items: flex-end;
    border-bottom-left-radius: 8px;
    border-bottom-right-radius: 8px;
  }

  input {
  border: 0;
  border-radius: 8px;
  width: 100%;
  height: 30px;
  }
  </style>