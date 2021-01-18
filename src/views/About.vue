<template>
  <div class="about">
    <Header></Header>
    <div class="wrapper">
      <div class="image">
        <img src="@/assets/images/asif.jpg" class="profile">
        <div class="summary">
          <p><span>Contact me at:</span> asif.mojtoba@gmail.com</p>
          <p>Find my resume <a :href="resumeLink" target="_blank">here</a></p>
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
        </div>
      </div>
      <div class="contents">
        <h2 class="title">Hi, I'm Asif!</h2>
        <div class="pronunciation" v-on:click="playNameAudio()">
          <audio controls id="nameAudio">
            <source src="@/assets/audio/asif.mp3" type="audio/mpeg">
            Your browser does not support the audio element.
          </audio>
          <img src="@/assets/images/icons/speaker.svg" class="icon"> <span>(aa-Siy-F)</span>
        </div>
        <p>A Product Designer (UX) from Dhaka, Bangladesh.</p>
        <p>I enjoy working with companies with multiverse-culture to create sustainable digital
          products and happy customers. I quite enjoy making things easy. It's a big part of my job
          as a designer.</p>
        <p>
          I practice design strategy from the user-centered design perspective utilizing my
          familiarity with Interaction Design, Principles of Behaviorism, and Product Design
          Methodologies; these also allows me to engineer designs that convert visitors to
          customers, and guide users to complete their tasks effortlessly. I always love to
          contribute to a better experience by making things clear & intuitive and communicating
          effectively while also keeping branding in mind.
        </p>
        <p>
          Additionally, having an appreciative level of knowledge about Programming Languages, Data
          Structures, Algorithms, and Technical Communications also keeps me on the same page with
          the core developer team. I'm an absolute team player and enjoy working with creative
          people, while appreciating Autodidacticism, and circumventing Dunning–Kruger effect.
        </p>
        <p>
          Aaaand, when I'm not busy with my works, you can find me making
          <b><a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ&feature=youtu.be"
                target="_blank">Memes</a></b> on random
          social media platforms or writing scripts for local sitcoms!
        </p>
      </div>
    </div>
  </div>
</template>
<script>
import Header from '@/components/Header.vue';

export default {
  components: { Header },
  data() {
    return {
      resumeLink: '//drive.google.com/file/d/1YQq6AbBNRkrwVT8fJXuUzthNT6VOKJTx/view?usp=sharing',
    };
  },
  methods: {
    playNameAudio() {
      const audio = document.getElementById('nameAudio');
      audio.play();
    },
  },
};
</script>

<style lang="less" scoped>
  .wrapper {
    padding: 100px 100px 20px;
    width: 100%;
    height: 100%;
    min-height: 100vh;
    display: flex;
    align-items: flex-start;
    justify-content: center;
    .image {
      flex-basis: 40%;
      width: 40%;
      .profile {
        width: 100%;
        border-radius: 4px;
        margin-bottom: 10px;
      }
      .summary {
        text-align: center;
        .social {
          margin-top: 20px;
          ul {
            list-style: none;
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
      }
    }
    .contents {
      padding: 0 40px;
      flex-basis: 60%;
      width: 60%;
      h2 {
        font-size: 34px;
        margin-bottom: 20px;
      }
      .pronunciation {
        margin-bottom: 15px;
        cursor: pointer;
        display: inline-block;
        audio {
          display: none;
        }
        .icon {
          width: 20px;
          vertical-align: middle;
          margin-right: 5px;
        }
        span {
          font-family: "Proxima Nova", sans-serif;
          font-weight: 100;
        }
      }
      p {
        font-size: 18px;
        margin-bottom: 15px;
      }
    }
  }
</style>
