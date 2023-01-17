<template>
  <section class="home" id="home">
    <div class="main-inf">
      <div class="image" v-motion-slide-visible-left>
        <img src="./icons/Picture.png" alt="Nikoloz Pic" />
      </div>
      <div  v-motion-slide-visible-right class="text">
        <p class="header">Front-End Web Developer</p>
        <h2 class="name">Nikoloz <span class="spanColor">Abuladze</span></h2>
        <p class="info">
          Welcome to my portfolio website! I am a highly skilled <span class="spanColor">front-end web
          developer</span> with a passion for creating visually stunning and
          user-friendly websites. I specialize in using <span class="spanColor">HTML, CSS, SCSS/SASS,
          JavaScript, VueJS, and GIT</span> to bring your ideas to life. My goal is to
          use my skills to create a website that exceeds your expectations.
          <span class="spanColor">Please take a look around my portfolio</span> to see some of my past work and
          feel free to contact me with any questions or to discuss <span class="spanColor">your next
          project.</span>
        </p>

        <div class="btns">
          <a href="#portfolio">
            <button class="portfolioBtn">Portfolio</button>
          </a>

          <a href="#contact">
            <button class="contactBtn">Contact</button>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>



<script></script>

<style lang="scss">
.home {
  padding: 276px 272px 276px 235px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.spanColor{
  color: #007ced;
}
.image {
  transition: 1s;
}

.main-inf {
  display: flex;
  align-items: center;
  gap: 82px;

  img {
    width: 491px;
    height: 491px;
    border-radius: 50%;
    border: 19px solid #444444;
    box-shadow: 0px 0px 50px rgba(0, 0, 0, 0.8);
  }

  .text {
    width: 803px;
    display: flex;
    flex-direction: column;
    gap: 44px;
    transition: 1s;

    .header {
      font-weight: 400;
      font-size: 24px;
      line-height: 35px;
      color: rgba(255, 255, 255, 0.5);
    }

    .name {
      font-weight: 700;
      font-size: 70px;
      line-height: 35px;
      color: #ffffff;
    }

    .info {
      font-weight: 400;
      font-size: 20px;
      line-height: 35px;
      color: #ffffff;
    }

    .btns {
      display: flex;
      gap: 15px;
      button {
        padding: 13px 46px 13px 46px;
        background: #333333;
        border: 3px solid #d5d5d5;
        border-radius: 30px;
        text-decoration: none;
        font-size: 20px;
        font-weight: 400;
        line-height: 35px;
        color: #ffffff;
        cursor: pointer;
        transition: all 0.5s;

        &:hover {
          border: 3px solid #007ced;
        }
      }
    }
  }
}
</style>
