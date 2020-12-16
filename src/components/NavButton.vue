<template>
  <li>
    <slot></slot>
  </li>
</template>

<script>
export default {
  name: "NavButton"
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Architects+Daughter&family=Open+Sans&display=swap');

li {
  padding: .5rem 2rem;
  margin: 0 1rem;
  color: white;
  text-transform: uppercase;
  border: 1px solid yellow;
  font-size: 24px;
  font-family: 'Architects Daughter', cursive;
}

li:hover {
  text-shadow: 0 0 5px yellow, 0 0 5px yellow;
  box-shadow: 0 0 5px 1px yellow;
}
</style>
