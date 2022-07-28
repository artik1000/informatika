<template>
  <div class="circle"></div>
  <div class="circlebig"></div>
  <nav>
    <router-link to="/">БИЛЕТЫ И АБОНИМЕНТЫ</router-link>
    <router-link to="/">Как купить</router-link>
    <router-link to="/">Правила</router-link>
    <router-link to="/">Возврат билетов</router-link>
    <div class="login">
      <router-link to="/">
        <div class="rowlogin">
         <span></span>
         <span class="material-symbols-outlined">
           login
         </span>
        <span class="vity">Войти</span>
        </div>
      </router-link>
      <router-link to="/">
        <div class="hamburgermenu">
          <div class="noblock"></div>
          <div class="menucontainer">
            <div class="elem"></div>
            <div class="elemsecound"></div>
            <div class="elemthird"></div>
          </div>
        </div>
      </router-link>
    </div>
  </nav>
  <router-view/>
</template>

<style lang="scss">
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    background-image: radial-gradient(circle at center, #4a5086 30%, #010a23 70%);
    color:white;
    height: 100vh;
    width: 100vw;
    position: relative;
    overflow: hidden;
  }
  @media screen and (min-device-width: 1280px) {
  .circle{
    width: 500px;
    height: 500px;
    color: white;
    border: 1px solid;
    position: absolute;
    border-radius: 50%;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    margin: auto;
  }
  .circlebig{
    width: 900px;
    height: 900px;
    color: white;
    border: 1px solid;
    position: absolute;
    border-radius: 50%;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    margin: auto;
  }

nav {
  padding-top: 30px;
  display: grid;
  grid-template-columns: 23vw 16vw 16vw 16vw 25vw;
  position: absolute;
  z-index: 999;
  a {
    font-weight: bold;
    font-size: 1rem;
    color: white;
    text-decoration: none;

    &.router-link-exact-active {
      color: white;
    }
  }
  a:hover{
    transition: 2s;
    color: gray;
    text-transform: uppercase;
  }
}
.login{
  display: grid;
  grid-template-columns: 50% 50%;
  z-index: 2;
}
.rowlogin{
  display: grid;
  grid-template-columns: 50% 20% 10%;
  z-index: 2;
}
.hamburgermenu{
  display: grid;
  grid-template-columns: 50% 50%;
  overflow: hidden;
  z-index: 2;
  .menucontainer{
    overflow: hidden;
    width: 30%;
  }
  .menucontainer:hover{
    .elem{
      transform: translate(70%,0);
      -webkit-transform: translate(70%,0); /** Chrome & Safari **/
      -o-transform: translate(70%,0); /** Opera **/
      -moz-transform: translate(70%,0);
      transition: 2s;
    }
    .elemsecound{
      transform: translate(-70%,0);
      -webkit-transform: translate(-70%,0); /** Chrome & Safari **/
      -o-transform: translate(-70%,0); /** Opera **/
      -moz-transform: translate(-70%,0);
      transition: 2s;
    }
    .elemthird{
      transform: translate(70%,0);
      -webkit-transform: translate(70%,0); /** Chrome & Safari **/
      -o-transform: translate(70%,0); /** Opera **/
      -moz-transform: translate(70%,0);
      transition: 2s;
    }
  }
  .elem{
    width: 100%;
    height: 1.5px;
    background-color: white;
    margin: 6px 0;
  }
  .elemsecound{
    width: 100%;
    height: 1.5px;
    background-color: white;
    margin: 8px 0;
    margin-left: 50%;
  }
  .elemthird{
    width: 100%;
    height: 1.5px;
    background-color: white;
    margin: 6px 0;
    margin-left: 25%;
  }
}
  }
@media screen and (min-device-width: 319px) and (max-device-width: 479px) {
  .circle{
    width: 200px;
    height: 200px;
    color: white;
    border: 1px solid;
    position: absolute;
    border-radius: 50%;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    margin: auto;
  }
  .circlebig{
    width: 300px;
    height: 300px;
    color: white;
    border: 1px solid;
    position: absolute;
    border-radius: 50%;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    margin: auto;
  }

  nav {
    padding-top: 30px;
    display: grid;
    grid-template-columns: 23vw 16vw 16vw 16vw 25vw;
    position: absolute;
    z-index: 999;
    a {
      font-weight: bold;
      font-size: 10px;
      color: white;
      text-decoration: none;

      &.router-link-exact-active {
        color: white;
      }
    }
    a:hover{
      transition: 5s;
      text-transform: uppercase;
    }
  }
  .vity{
    display: none;
  }
  .login{
    display: grid;
    grid-template-columns: 50% 50%;
    z-index: 2;
  }
  .rowlogin{
    z-index: 2;
    width: 40px;
    margin: 0 !important;
    padding: 0 !important;
  }
  .hamburgermenu{
    overflow: hidden;
    z-index: 2;
    .menucontainer{
      overflow: hidden;
      width: 50%;
    }
    .menucontainer:hover{
      .elem{
        transform: translate(70%,0);
        -webkit-transform: translate(70%,0); /** Chrome & Safari **/
        -o-transform: translate(70%,0); /** Opera **/
        -moz-transform: translate(70%,0);
        transition: 2s;
      }
      .elemsecound{
        transform: translate(-70%,0);
        -webkit-transform: translate(-70%,0); /** Chrome & Safari **/
        -o-transform: translate(-70%,0); /** Opera **/
        -moz-transform: translate(-70%,0);
        transition: 2s;
      }
      .elemthird{
        transform: translate(70%,0);
        -webkit-transform: translate(70%,0); /** Chrome & Safari **/
        -o-transform: translate(70%,0); /** Opera **/
        -moz-transform: translate(70%,0);
        transition: 2s;
      }
    }
    .elem{
      width: 100%;
      height: 1px;
      background-color: white;
      margin: 6px 0;
    }
    .elemsecound{
      width: 100%;
      height: 1px;
      background-color: white;
      margin: 6px 0;
      margin-left: 50%;
    }
    .elemthird{
      width: 100%;
      height: 1px;
      background-color: white;
      margin: 6px 0;
      margin-left: 25%;
    }
  }
  .noblock{
    display: none;
  }
}
  @media screen and (min-device-width: 480px) and (max-device-width: 767px) {
    .circle{
      width: 200px;
      height: 200px;
      color: white;
      border: 1px solid;
      position: absolute;
      border-radius: 50%;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
      margin: auto;
    }
    .circlebig{
      width: 400px;
      height: 400px;
      color: white;
      border: 1px solid;
      position: absolute;
      border-radius: 50%;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
      margin: auto;
    }

    nav {
      padding-top: 30px;
      display: grid;
      grid-template-columns: 23vw 16vw 16vw 16vw 25vw;
      position: absolute;
      z-index: 999;
      a {
        font-weight: bold;
        font-size: 15px;
        color: white;
        text-decoration: none;

        &.router-link-exact-active {
          color: white;
        }
      }
      a:hover{
        transition: 2s;
        color: gray;
        text-transform: uppercase;
      }
    }
    .vity{
      display: none;
    }
    .login{
      display: grid;
      grid-template-columns: 50% 50%;
      z-index: 2;
    }
    .hamburgermenu{
      overflow: hidden;
      z-index: 2;
      .menucontainer{
        overflow: hidden;
        width: 100%;
      }
      .menucontainer:hover{
        .elem{
          transform: translate(70%,0);
          -webkit-transform: translate(70%,0); /** Chrome & Safari **/
          -o-transform: translate(70%,0); /** Opera **/
          -moz-transform: translate(70%,0);
          transition: 2s;
        }
        .elemsecound{
          transform: translate(-70%,0);
          -webkit-transform: translate(-70%,0); /** Chrome & Safari **/
          -o-transform: translate(-70%,0); /** Opera **/
          -moz-transform: translate(-70%,0);
          transition: 2s;
        }
        .elemthird{
          transform: translate(70%,0);
          -webkit-transform: translate(70%,0); /** Chrome & Safari **/
          -o-transform: translate(70%,0); /** Opera **/
          -moz-transform: translate(70%,0);
          transition: 2s;
        }
      }
      .elem{
        width: 100%;
        height: 1.5px;
        background-color: white;
        margin: 6px 0;
      }
      .elemsecound{
        width: 100%;
        height: 1.5px;
        background-color: white;
        margin: 10px 0;
        margin-left: 50%;
      }
      .elemthird{
        width: 100%;
        height: 1.5px;
        background-color: white;
        margin: 6px 0;
        margin-left: 25%;
      }
    }
    .material-symbols-outlined{
      font-size: 40px;
    }
  }
  @media screen and (min-device-width: 768px) and (max-device-width: 1023px) {
    .circle{
      width: 600px;
      height: 600px;
      color: white;
      border: 1px solid;
      position: absolute;
      border-radius: 50%;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
      margin: auto;
    }
    .circlebig{
      width: 800px;
      height: 800px;
      color: white;
      border: 1px solid;
      position: absolute;
      border-radius: 50%;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
      margin: auto;
    }

    nav {
      padding-top: 30px;
      display: grid;
      grid-template-columns: 23vw 16vw 16vw 16vw 25vw;
      position: absolute;
      z-index: 999;
      a {
        font-weight: bold;
        font-size: 20px;
        color: white;
        text-decoration: none;

        &.router-link-exact-active {
          color: white;
        }
      }
      a:hover{
        transition: 2s;
        color: gray;
        text-transform: uppercase;
      }
    }
    .vity{
      display: none;
    }
    .login{
      display: grid;
      grid-template-columns: 50% 50%;
      z-index: 2;
    }
    .hamburgermenu{
      overflow: hidden;
      z-index: 2;
      .menucontainer{
        overflow: hidden;
        width: 50%;
      }
      .menucontainer:hover{
        .elem{
          transform: translate(70%,0);
          -webkit-transform: translate(70%,0); /** Chrome & Safari **/
          -o-transform: translate(70%,0); /** Opera **/
          -moz-transform: translate(70%,0);
          transition: 2s;
        }
        .elemsecound{
          transform: translate(-70%,0);
          -webkit-transform: translate(-70%,0); /** Chrome & Safari **/
          -o-transform: translate(-70%,0); /** Opera **/
          -moz-transform: translate(-70%,0);
          transition: 2s;
        }
        .elemthird{
          transform: translate(70%,0);
          -webkit-transform: translate(70%,0); /** Chrome & Safari **/
          -o-transform: translate(70%,0); /** Opera **/
          -moz-transform: translate(70%,0);
          transition: 2s;
        }
      }
      .elem{
        width: 100%;
        height: 1.5px;
        background-color: white;
        margin: 6px 0;
      }
      .elemsecound{
        width: 100%;
        height: 1.5px;
        background-color: white;
        margin: 10px 0;
        margin-left: 50%;
      }
      .elemthird{
        width: 100%;
        height: 1.5px;
        background-color: white;
        margin: 6px 0;
        margin-left: 25%;
      }
    }
    .material-symbols-outlined{
      font-size: 40px;
    }
    .rowlogin{
      z-index: 2;
      width: min-content;
      margin: 0 !important;
      padding: 0 !important;
    }
  }
  @media screen and (min-device-width: 1024px) and (max-device-width: 1279px) {
    .rowlogin{
      display: grid;
      grid-template-columns: 50% 20% 10%;
      z-index: 2;
    }
    .login{
      display: grid;
      grid-template-columns: 50% 50%;
      z-index: 2;
    }
    .circle{
      width: 500px;
      height: 500px;
      color: white;
      border: 1px solid;
      position: absolute;
      border-radius: 50%;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
      margin: auto;
    }
    .circlebig{
      width: 1000px;
      height: 1000px;
      color: white;
      border: 1px solid;
      position: absolute;
      border-radius: 50%;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
      margin: auto;
    }

    nav {
      padding-top: 30px;
      display: grid;
      grid-template-columns: 23vw 16vw 16vw 16vw 25vw;
      position: absolute;
      z-index: 999;
      a {
        font-weight: bold;
        font-size: 20px;
        color: white;
        text-decoration: none;

        &.router-link-exact-active {
          color: white;
        }
      }
      a:hover{
        transition: 2s;
        color: gray;
        text-transform: uppercase;
      }
    }
    .vity{
      display: block;
    }
    .hamburgermenu{
      display: grid;
      grid-template-columns: 50% 50%;
      overflow: hidden;
      z-index: 2;
      .menucontainer{
        overflow: hidden;
        width: 100%;
      }
      .menucontainer:hover{
        .elem{
          transform: translate(70%,0);
          -webkit-transform: translate(70%,0); /** Chrome & Safari **/
          -o-transform: translate(70%,0); /** Opera **/
          -moz-transform: translate(70%,0);
          transition: 2s;
        }
        .elemsecound{
          transform: translate(-70%,0);
          -webkit-transform: translate(-70%,0); /** Chrome & Safari **/
          -o-transform: translate(-70%,0); /** Opera **/
          -moz-transform: translate(-70%,0);
          transition: 2s;
        }
        .elemthird{
          transform: translate(70%,0);
          -webkit-transform: translate(70%,0); /** Chrome & Safari **/
          -o-transform: translate(70%,0); /** Opera **/
          -moz-transform: translate(70%,0);
          transition: 2s;
        }
      }
      .elem{
        width: 100%;
        height: 2px;
        background-color: white;
        margin: 12px 0;
      }
      .elemsecound{
        width: 100%;
        height: 2px;
        background-color: white;
        margin: 12px 0;
        margin-left: 50%;
      }
      .elemthird{
        width: 100%;
        height: 2px;
        background-color: white;
        margin: 12px 0;
        margin-left: 25%;
      }
    }
  }
  @media screen and (min-device-width: 280px) and (max-device-width: 319px) {
    .circle{
      width: 100px;
      height: 100px;
      color: white;
      border: 1px solid;
      position: absolute;
      border-radius: 50%;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
      margin: auto;
    }
    .circlebig{
      width: 200px;
      height: 200px;
      color: white;
      border: 1px solid;
      position: absolute;
      border-radius: 50%;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
      margin: auto;
    }

    nav {
      padding-top: 30px;
      display: grid;
      grid-template-columns: 23vw 16vw 16vw 16vw 25vw;
      position: absolute;
      z-index: 999;
      a {
        font-weight: bold;
        font-size: 10px;
        color: white;
        text-decoration: none;

        &.router-link-exact-active {
          color: white;
        }
      }
      a:hover{
        transition: 2s;
        color: gray;
        text-transform: uppercase;
      }
    }
    .vity{
      display: none;
    }
    .login{
      display: grid;
      grid-template-columns: 50% 50%;
      z-index: 2;
    }
    .rowlogin{
      z-index: 2;
      width: 40px;
      margin: 0 !important;
      padding: 0 !important;
    }
    .hamburgermenu{
      overflow: hidden;
      z-index: 2;
      .menucontainer{
        overflow: hidden;
        width: 50%;
      }
      .menucontainer:hover{
        .elem{
          transform: translate(70%,0);
          -webkit-transform: translate(70%,0); /** Chrome & Safari **/
          -o-transform: translate(70%,0); /** Opera **/
          -moz-transform: translate(70%,0);
          transition: 2s;
        }
        .elemsecound{
          transform: translate(-70%,0);
          -webkit-transform: translate(-70%,0); /** Chrome & Safari **/
          -o-transform: translate(-70%,0); /** Opera **/
          -moz-transform: translate(-70%,0);
          transition: 2s;
        }
        .elemthird{
          transform: translate(70%,0);
          -webkit-transform: translate(70%,0); /** Chrome & Safari **/
          -o-transform: translate(70%,0); /** Opera **/
          -moz-transform: translate(70%,0);
          transition: 2s;
        }
      }
      .elem{
        width: 100%;
        height: 1px;
        background-color: white;
        margin: 6px 0;
      }
      .elemsecound{
        width: 100%;
        height: 1px;
        background-color: white;
        margin: 6px 0;
        margin-left: 50%;
      }
      .elemthird{
        width: 100%;
        height: 1px;
        background-color: white;
        margin: 6px 0;
        margin-left: 25%;
      }
    }
    .noblock{
      display: none;
    }
  }
</style>
