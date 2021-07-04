<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style>
*,
*::before,
*::after {
  box-sizing: border-box;
}
a {
  text-decoration: none;
  color: var(--clr-neutral-2);
  font-weight: bold;
}
:root {
  --clr-neutral-1: #EDD9A3;
  --clr-neutral-2: #040403;

  --clr-primary-1: #5998C5;
  --clr-primary-2: #1B998B;
  --clr-primary-3: #846C5B;

  --ff-primary: "Roboto", sans-serif;
}

body {
  margin: 0;
  background-color: var(--clr-neutral-1);
}

#app {
  font-family: var(--ff-primary);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: var(--clr-neutral-2);
}

input {
  font-family: inherit;
  width: 50%;
  border: 0;
  border-bottom: 2px solid var(--clr-neutral-2);
  outline: 0;
  font-size: 1.3rem;
  color: var(--clr-neutral-2);
  padding: 7px 0;
  background: transparent;
  transition: border-color 0.2s;
  margin: 1em;
}
</style>
