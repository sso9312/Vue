<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>|
    <router-link to="/welcome">Welcome</router-link>|
    <router-link to="/databinding/string">string</router-link>|
    <router-link to="/databinding/html">HTML</router-link>|
    <router-link to="/databinding/input">Input</router-link>|
    <router-link to="/databinding/attr">Attribute</router-link>|
    <router-link to="/event/list">배열</router-link>|
    <router-link to="/event/click">Click</router-link>|
    <router-link to="/event/change">Change</router-link>|
    <router-link to="/event/key">Key</router-link>|
    <router-link to="/memolist">Memo</router-link>|
  </nav>
  <router-view/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
