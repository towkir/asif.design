<template>
  <div class="home">
    <Header></Header>
    <div class="intro">
      <div class="wrapper">
        <h1>Hi, I'm Asif!</h1>
        <h4>Currently, a UXer @<span>Sheba.xyz</span></h4>
        <p>
          I'm a Product Designer with a foundation in UX and Service Design; pursuing Bachelors of
          Computer Science @<span>Brac University</span>
        </p>
        <p>
          <a class="orange" href="#works">View my works</a>
        </p>
      </div>
    </div>
    <div class="works" id="works">
      <div class="image">
        <img src="@/assets/images/chevval.png" class="preview">
        <div class="summary">
          <p class="duration"><span>Duration:</span> 6 months</p>
          <p class="time">(Jan 2018 - June 2018)</p>
        </div>
      </div>
      <div class="contents">
        <h4 class="title"><span class="chevval">Chevval</span> — a makeup enthusiasts hub</h4>
        <p class="details">
          Chevval helps to decrease the hassle to beautify yourself! Discover best makeup artists &
          beauty salons recommended by users from all over the country.
        </p>
        <ul class="points">
          <li>Facilitated the client’s product vision by researching, conceiving,
            sketching, prototyping and user-testing</li>
          <li>Applied knowledge of UX design to develop mock-ups, new
            interaction models, and navigation schemes</li>
        </ul>
        <p>
          <a href="https://drive.google.com/file/d/1hIi0tGtYkL7V3zccc_W86KsOToNd_DjP/view?usp=sharing"
             target="_blank" class="orange">View Case Study</a>
          <span>(10 minute read)</span>
        </p>
      </div>
    </div>
    <div class="works">
      <div class="image">
        <img src="@/assets/images/go-11.png" class="preview">
        <div class="summary">
          <p class="duration"><span>Duration:</span> 2 years</p>
          <p class="time">(Nov 2018 - Nov 2020)</p>
        </div>
      </div>
      <div class="contents">
        <h4 class="title"><span class="go-11">GameOf11</span> — a fantasy gaming platform</h4>
        <p class="details">
          GameOf11 is the first ever user focused fantasy gaming platform in Bangladesh where
          participants can play cricket and football fantasy leagues.
        </p>
        <ul class="points">
          <li>Lead the cross-functional product and design team</li>
          <li>Created design concepts & low-fi sketches to iterate latent features</li>
          <li>Coordinated with team members to ensure consistency in design</li>
        </ul>
        <p>
          <button class="orange" disabled>View Case Study</button>
          <span>(Coming Soon!)</span>
        </p>
      </div>
    </div>
    <div class="works">
      <div class="image">
        <img src="@/assets/images/swap.png" class="preview">
        <div class="summary">
          <p class="duration"><span>Duration:</span> 9 months</p>
          <p class="time">(Nov 2019 - Jul 2020)</p>
        </div>
      </div>
      <div class="contents">
        <h4 class="title"><span class="swap">SWAP</span> — a multiverse online marketplace</h4>
        <p class="details">
          SWAP is the combination of the e-commerce and re-commerce marketplace in Bangladesh where
          customers can purchase as well as sell products.
        </p>
        <ul class="points">
          <li>Created wireframes, site maps, user flows, use cases and detailed
            functional requirement documents</li>
          <li>Made strategic design and user-experience decisions related to
            core & functions and features</li>
        </ul>
        <p>
          <button class="orange" disabled>View Case Study</button>
          <span>(Coming Soon!)</span>
        </p>
      </div>
    </div>
    <div class="conclusion">
      <div class="wrapper">
        <p>
          As a designer I'm always consciously curious about the UX realm while
          also being head over heels in love with crafting delightful, effective
          moments for the end users.
        </p>
      </div>
    </div>
    <Footer></Footer>
  </div>
</template>

<script>
// @ is an alias to /src

import Header from '@/components/Header.vue';
import Footer from '@/components/Footer.vue';

export default {
  name: 'Home',
  components: {
    Footer,
    Header,
    // HelloWorld,
  },
};
</script>

<style lang="less" scoped>
  button.orange, a.orange {
    background-color: #E08867;
    appearance: none;
    border: 0;
    padding: 15px 30px;
    color: #fff;
    /*display: block;*/
    font-size: 24px;
    border-radius: 4px;
    text-transform: uppercase;
    cursor: pointer;
    transition: 0.3s ease-in-out;
    display: inline-block;
    text-decoration: none;
    &:hover {
      background-color: #3A5769;
    }
    &:disabled {
      opacity: 0.7;
      cursor: default;
      &:hover {
        background-color: #E08867;
      }
    }
  }
  .home {
    .intro, .works, .conclusion {
      width: 100%;
      height: 100%;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 100px;
      text-align: center;
    }
    .intro {
      .wrapper {
        h1 {
          font-family: 'Proxima Nova', sans-serif;
          font-size: 60px;
          font-weight: bold;
          color: #10344C;
        }
        h4 {
          font-family: 'Proxima Nova', sans-serif;
          font-size: 34px;
          font-weight: normal;
          color: #3A5769;
          margin-bottom: 30px;
          span {
            color: #D879A6;
          }
        }
        p {
          font-size: 32px;
          color: #11354C;
          span {
            color: #519BF4;
          }
          & + p {
            margin: 40px auto 0;
          }
        }
      }
    }
    .works {
      text-align: left;
      .image {
        flex-basis: 40%;
        width: 40%;
        img {
          display: block;
          margin: 0 auto 20px;
        }
        .summary {
          text-align: center;
          font-size: 18px;
          p {
            color: #3A5769;
            span {
              font-weight: 600;
            }
            &.time {
              margin-top: 5px;
              font-size: 14px;
            }
          }
        }
      }
      .contents {
        font-family: "Proxima Nova", sans-serif;
        padding: 0 40px;
        flex-basis: 60%;
        width: 60%;
        .title {
          font-size: 34px;
          font-weight: normal;
          margin-bottom: 25px;
          color: #11354C;
          span {
            &.go-11 {
              color: #92CA00;
            }
            &.swap {
              color: #519BF4;
            }
            &.chevval {
              color: #D879A6;
            }
          }
        }
        p {
          color: #2E3033;
          font-size: 24px;
          margin-bottom: 25px;
          position: relative;
          button, a {
            & + span {
              margin-left: 15px;
              font-size: 16px;
              font-weight: 100;
              color: #6D7E8B;
            }
          }
          button:disabled {
            & + span {
              font-weight: 400;
            }
          }
        }
        ul {
          margin-bottom: 25px;
          padding-left: 20px;
          li {
            font-size: 18px;
            margin-bottom: 8px;
          }
        }
      }
    }
    .conclusion {
      min-height: calc(100vh - 80px);
      .wrapper {
        p {
          font-size: 34px;
          color: #11354C;
          max-width: 80%;
          margin: 0 auto;
        }
      }
    }
  }
</style>
