<template>
  <div id="footer">
    <div class="learn-more">
      <span>stay connected with me</span>
    </div>
    <div class="social">
      <ul>
        <li>
          <a href="https://www.linkedin.com/in/asif-design" target="_blank">
            <img src="@/assets/images/icons/linkedin.svg">
          </a>
        </li>
        <li>
          <a href="https://twitter.com/asif_mojtoba" target="_blank">
            <img src="@/assets/images/icons/twitter.svg">
          </a>
        </li>
        <li>
          <a href="https://www.instagram.com/asif.m.kabir" target="_blank">
            <img src="@/assets/images/icons/instagram.svg">
          </a>
        </li>
        <li>
          <a href="https://www.facebook.com/asif.m.kabir" target="_blank">
            <img src="@/assets/images/icons/facebook.svg">
          </a>
        </li>
      </ul>
    </div>
    <div class="action" v-if="!reachedBottom" v-on:click="scrollOneFold()">
      <span>scroll down <img src="@/assets/images/icons/arrow-down.svg" class="icon"></span>
    </div>
    <div class="action" v-else v-on:click="scrollToTop()">
      <span>back to top <img src="@/assets/images/icons/arrow-down.svg"
                               class="icon up-side-down"></span>
    </div>
  </div>
</template>

<script>
import $ from 'jquery';

export default {
  name: 'Footer',
  data() {
    return {
      currentPage: 1,
      reachedBottom: false,
    };
  },
  methods: {
    scrollOneFold() {
      $('html, body').animate({ scrollTop: window.scrollY + window.innerHeight }, 1000);
    },
    scrollToTop() {
      $('html, body').animate({ scrollTop: 0 }, 1500);
    },
    checkScrollPosition() {
      if ((window.innerHeight + window.scrollY) >= document.body.offsetHeight) {
        // you're at the bottom of the page
        this.reachedBottom = true;
      } else {
        this.reachedBottom = false;
      }
      this.currentPage = Math.ceil(window.scrollY > window.innerHeight
        ? document.body.scrollHeight / window.scrollY : 0);
    },
  },
  mounted() {
    window.addEventListener('scroll', this.checkScrollPosition);
  },
  destroyed() {
    window.removeEventListener('scroll', this.checkScrollPosition);
  },
};
</script>

<style lang="less" scoped>
  #footer {
    padding: 20px 100px;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    .learn-more {
      margin-bottom: 15px;
      span {
        text-decoration: none;
        font-size: 16px;
        font-weight: 600;
        color: #11354C;
      }
    }
    .social {
      ul {
        list-style: none;
        margin-bottom: 10px;
        li {
          display: inline-block;
          a {
            margin: 0 10px;
            padding: 0;
            border-radius: 50%;
            border: 1px solid #2E3033;
            line-height: 1;
            display: flex;
            align-items: center;
            justify-content: center;
            height: 40px;
            width: 40px;
            opacity: 0.3;
            transition: 0.3s ease-in-out;
            &:hover {
              opacity: 1;
            }
            img {
              width: 20px;
              /*max-height: 40px;*/
            }
          }
        }
      }
    }
    .action {
      position: fixed;
      bottom: 20px;
      right: 100px;
      cursor: pointer;
      font-size: 16px;
      /*display: none;*/
      img.icon {
        margin: 0 10px;
        padding: 8px;
        border-radius: 50%;
        border: 1px solid #2E3033;
        line-height: 1;
        height: 40px;
        width: 40px;
        opacity: 0.3;
        transition: 0.3s ease-in-out;
        vertical-align: middle;
        &.up-side-down {
          transform: scale(-1);
        }
      }
      &:hover {
        img.icon {
          opacity: 1;
        }
      }
    }
  }
</style>
