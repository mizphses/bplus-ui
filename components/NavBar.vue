<template>
  <div>
    <nav>
      <nuxt-link class="no-decorator" to="/">
        <h1 class="logotype no-decorator">B plus</h1>
      </nuxt-link>
      <div>
        <a class="login-button-wrap no-decorator" href="#">
          <span class="material-symbols-outlined">account_circle</span>
          <span class="login-text-wrap">ログイン</span>
        </a>
      </div>
    </nav>
  </div>
</template>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Libre+Baskerville:ital@1&display=swap');

  .logotype{
    font-family: 'Libre Baskerville';
    font-style: italic;
  }

  nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 0;
    padding: 0 2em;
    background-color: #fff;
  }
  .login-button-wrap{
    display: flex;
    align-items: center;
    padding: 1px 1px 1px 7px;
    color: white;
    background-color: rgb(220, 0, 0);
    border-radius: 0.2em;
  }

  .login-button-wrap:hover{
    display: flex;
    align-items: center;
    padding: 1px 1px 1px 7px;
    color: white;
    background-color: rgb(165, 0, 0);
    border-radius: 0.2em;
  }

  .login-text-wrap{
    background-color: white;
    padding: 0.5em 1em;
    margin-left: 0.5em;
    color: black;
    border-radius: 0 0.2em 0.2em 0;
  }

  .login-text-wrap:hover{
    background-color: rgb(240,240,240);
  }
</style>