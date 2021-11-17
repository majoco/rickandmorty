<template>
  <div id="nav">
    <router-link to="/">Home</router-link>
  </div>
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

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

.caja{
    background: lightgray;
    margin: 5px;
    border-radius: 10px;
    padding-bottom: 10px;
    margin-bottom: 15px;
}
.caja:hover{
  box-shadow: 0px 0px 10px #888888;
}
img{
  width: 100%;
  border-radius: 10px 10px 0px 0px;
}
.row::marker{
  color: transparent;
}
.about>.col-3 {
  margin: auto;
}
.tleft{
  text-align: left;
}
.caja_detalle{
  padding: 30px;
}

@media screen and (max-width: 992px) {
  .col-3 {      
      max-width: 45%;
      margin: 0px;
      display: inline-block;
  }
  .card-body>.container>.row {
    display: list-item;
  }
}
@media screen and (max-width: 480px) {
  .col-3 {      
    display: contents;
  }
}
</style>
