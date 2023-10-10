<template>
  <div class="container-wrapper">
    <div class="container">
      <div class="input-wrapper">
        <i><img class="lupa-img" src="../assets/lupa.png" alt="" /></i>

        <input type="text" placeholder="Pesquisa" class="input-filter" />
      </div>
    </div>
  </div>
</template>

<script></script>

<style lang="css" scoped>
.lupa-img {
  width: 16px;
  height: auto;
  margin-top: 5px;
}
.container-wrapper {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
 
}

.input-wrapper {
  display: flex;
  align-items: center;
  gap: 6px;
  border-radius: 7px;
  background-color: white;
  padding: 0.5px 4px;
  border-width: 1px;
  border-style: double;
}
.input-filter {
  background-color: transparent;
  border: none;
  color: black;
  font-size: 15px;
  width: 160px;
}
.input-filter:focus-visible {
  outline: none;
}
</style>
