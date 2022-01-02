<template>
  <div class="footer">
      <p>© Copyright Farzan Ali {{new Date().getFullYear()}}</p>
  </div>
</template>

<script>
// document.getElementById('copyright').appendChild(document.createTextNode(new Date().getFullYear()));
// document.getElementById("year").innerHTML = new Date().getFullYear();
export default {
    name: 'Footer'
}
</script>

<style>
.footer p{
    color: #fff;
}
</style>