<template>
  <router-view />
</template>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&family=Sora:wght@600;400&display=swap");

/*##RESET*/
* {
  box-sizing: border-box;
  padding: 0px;
  margin: 0px;
}
ul,
ol {
  list-style: none;
}
a {
  text-decoration: none;
}
img {
  height: auto;
}
button,
input,
textarea {
  border: 0;
  outline: none;
}
button:focus,
input:focus,
textarea:focus {
  border: 0;
  outline: none;
}
li {
  cursor: pointer;
}
body {
  font-family: "Inter", sans-serif;
  overflow-x: hidden;
  background-color: $white-200-color;
  scrollbar-color: $blue-color $white-color;
  scrollbar-width: 12px;
}
body::-webkit-scrollbar {
  max-width: 10px;
}
body::-webkit-scrollbar-track {
  background: $white-color;
}
body::-webkit-scrollbar-thumb {
  background: $blue-color;
  box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.5);
  border-radius: 20px;
}
</style>
