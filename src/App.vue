<template>
  <div id="app" ref="app">
    <TheHeader/>
    <TheMain/>
    <TheFooter/>
  </div>
</template>

<script>
import TheHeader from './components/TheHeader.vue';
import TheMain from './components/TheMain.vue';
import TheFooter from './components/TheFooter.vue';

export default {
  name: 'App',
  components: {
    TheHeader,
    TheMain,
    TheFooter
}
}
</script>

<style lang="scss">
@font-face {
  font-family: 'Gotham';
  src: url('./assets/fonts/Gotham-Book.otf');
  font-weight: 400;
}

@font-face {
  font-family: 'Gotham';
  src: url('./assets/fonts/Gotham-Light.otf');
  font-weight: 300;
}

@font-face {
  font-family: 'Gotham';
  src: url('./assets/fonts/Gotham-Thin.otf');
  font-weight: 100;
}

@font-face {
  font-family: 'Gotham';
  src: url('./assets/fonts/Gotham-Medium.otf');
  font-weight: 600;
}

@font-face {
  font-family: 'Gotham';
  src: url('./assets/fonts/GothamNarrow-Black.otf');
  font-weight: 650;
}

@font-face {
  font-family: 'Gotham';
  src: url('./assets/fonts/Gotham-Ultra.otf');
  font-weight: 700;
}

:root{
  /* 
    blue(violet) = #843bcb
    pink = #ff3182 
  */
  --dark: #090f19;
  --dark-rgb: 9, 15, 25;
  --blue: rgb(132, 59, 203);
  --blue-rgb: 132, 59, 203;
  --pink: rgb(255, 49, 130);
  --pink-rgb: 255, 49, 130;
  --cyan: rgb(1, 186, 239);
  --cyan-rgb: 1, 186, 239;
  --pastel-pink: rgb(219, 168, 172);
  --pastel-pink-rgb: 219, 168, 172;
  --black: rgb(14, 0, 4);
  --black-rgb: 14, 0, 4;
  --white: whitesmoke;
  --white-rgb: 245 245 245;
}

#app {
  font-family: 'Gotham', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: var(--white);
  overflow: hidden;
}


a {
  display: inline-block;
  text-decoration: none;
  color: inherit;

  &:hover {
    color: unset;
  }
}

h1, h2 {
  font-weight: 700;
}

p{
  color: var(--white);
}

button, .button {
  border: none;
  outline: none;
  padding: 0.5rem 1.5rem;
  border-radius: 0.5rem;
}

.large-btn{
  padding: 0.5rem 2.5rem;
}

.primary-btn {
  color: var(--white);
  font-weight: 600;
  box-shadow: 0 0.5rem 1rem rgba(var(--black-rgb), 0.5);
  background: linear-gradient(135deg, var(--blue), var(--pink), var(--blue));
  background-size: 200%;
  background-position: left;
  transition: 200ms linear;
  &:hover {
    background-position: right;
  }
  &:active{
    transform: translateY(0.3rem);
    box-shadow: 0 0.2rem 0.5rem rgba(var(--black-rgb), 0.5);
    color: var(--cyan);
  }
}

ul{
  list-style: none;
  padding: 0;
}

img{
  width: 100%;
}

.form-control {
    color: var(--white);
    background-color: rgba(var(--dark-rgb), 0.3);
    backdrop-filter: blur(0.1rem);
    border-color: rgba(0,0,0,0);
    border-radius: 0.5rem;
    box-shadow: inset 0 0 1rem rgba(245, 245, 245, 0.5);
    resize: none;
}

.form-control:focus {
    color: var(--white);
    background: rgba(var(--dark-rgb), 0.3);
    border-color: var(--blue);
    outline: 0;
    box-shadow: 0 0 0 0.25rem rgb(132 59 203 / 25%);
}

.col-50{
  width: 50%;
}

.section{
  padding-top: 130px;
  padding-bottom: 100px;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  .container{
    flex-grow: 1;
  }
}

@media screen and (max-width: 327px){
  .section{
    padding-top: 70px;
  }
}

/* width */
::-webkit-scrollbar {
  width: 10px;
}

/* Track */
::-webkit-scrollbar-track {
  background: var(--black);
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: linear-gradient(135deg, var(--pink), var(--blue), var(--pink));
  border-radius: 1rem;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:active {
  background: linear-gradient(135deg, var(--blue), var(--pink), var(--blue));
}
</style>
