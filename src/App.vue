<template>
  <router-view/>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=League+Spartan:wght@500;600;700&display=swap');
/* font-family: 'League Spartan', sans-serif; */

*, *::before, *::after {
  box-sizing: border-box;
}
* {
  margin: 0;
}
html, body {
  height: 100%;
  font-size: 12px;
}
body {
  line-height: 1.5;
  -webkit-font-smoothing: antialiased;
}
img, picture, video, canvas, svg {
  display: block;
  max-width: 100%;
}
input, button, textarea, select {
  font: inherit;
}
p, h1, h2, h3, h4, h5, h6 {
  overflow-wrap: break-word;
}
#root, #__next {
  isolation: isolate;
}

:root{
  --darkgrey: hsl(0, 0%, 63%);
  --verydarkgrey: hsl(0, 0%, 27%);
  --black: hsl(0, 0%, 0%);
  --white: hsl(0, 0%, 100%);

}
</style>
