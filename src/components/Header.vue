<template>
  <div id="header">
    <div class="logo">
      <router-link to="/" exact>asif.design</router-link>
    </div>
    <div class="links">
      <ul>
        <li><router-link to="/#works" exact>work</router-link></li>
        <li><router-link :to="resumeLink" target="_blank">resume</router-link></li>
        <li><router-link to="/about" exact>about</router-link></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
  props: {
    msg: String,
  },
  data() {
    return {
      resumeLink: '//drive.google.com/file/d/1YQq6AbBNRkrwVT8fJXuUzthNT6VOKJTx/view?usp=sharing',
    };
  },
};
</script>

<style scoped lang="less">
  #header {
    position: fixed;
    width: 100%;
    top: 0;
    left: 0;
    padding: 30px 100px;
    display: flex;
    justify-content: space-between;
    font-family: "Proxima Nova", sans-serif;
    background-color: #F4ECE9;
    z-index: 10;
    .logo {
      a {
        color: #11354C;
        text-decoration: none;
        font-size: 16px;
        font-weight: 800;
        opacity: 0.3;
        &.router-link-active {
          opacity: 1;
          text-decoration: underline;
        }
      }
    }
    .links {
      ul {
        list-style: none;
        li {
          display: inline-block;
          margin-right: 30px;
          &:last-child {
            margin-right: 0;
          }
          a {
            color: #3A5769;
            text-decoration: none;
            font-size: 16px;
            font-weight: 800;
            opacity: 0.3;
            transition: .3s ease-in-out;
            &.router-link-active {
              opacity: 1;
              /*color: #519BF4;*/
              text-decoration: underline;
            }
            &:hover {
              opacity: 1;
              color: #519BF4;
              text-decoration: underline;
            }
          }
        }
      }
    }
  }
</style>
