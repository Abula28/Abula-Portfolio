<template>
  <section class="skill" id="skill">
    <div class="head">
      <h1 v-motion-fade-visible>Front-End Skills</h1>
    </div>

    <div class="main-info">
      <div class="lang-side">
        <div v-motion-slide-visible-left class="lang-header">
          <h2>Programming <span class="spanColor">Languages:</span></h2>
          <img src="./icons/line.png" alt="line" class="line" />
        </div>
        <div
          v-motion
          :initial="{ opacity: 0, y: -100 }"
          :visible="{ opacity: 1, y: 0 }"
          :delay="100"
          class="about"
        >
          <img src="./icons/pc_icon.png" alt="pc icon" />
          <div class="text">
            <h1>HTML, CSS, JavaScript</h1>

            <p>
              HTML: I have experience working with HTML to structure and
              organize content on the web. CSS: I am proficient in using CSS to
              style and layout web pages. JavaScript: I have experience using
              JavaScript to add interactive elements and functionality to
              websites.
            </p>
          </div>
        </div>

        <div
          v-motion
          :initial="{ opacity: 0, y: -100 }"
          :visible="{ opacity: 1, y: 0 }"
          :delay="200"
          class="about"
        >
          <img src="./icons/image-16.png" alt="img" />
          <div class="text">
            <h1>SCSS/SASS Vue.js</h1>

            <p>
              SCSS/SASS: I am skilled in using preprocessor languages like SCSS
              and SASS to write efficient, organized stylesheets. VueJS: I have
              experience working with Vue.js, a JavaScript framework for
              building user interfaces. I have built various web applications
              using Vue.js, such as components, directives, and the Vuex state
              management library.
            </p>
          </div>
        </div>
      </div>
      <div class="skill-side">
        <div v-motion-slide-visible-right class="skill-header">
          <h1>Coding <span class="spanColor">Skills</span></h1>
          <img src="./icons/line.png" alt="line" class="line" />
        </div>

        <div class="indicator">
          <div class="indicators-div">
            <div
              v-motion
              :initial="{ opacity: 0, y: -100 }"
              :visible="{ opacity: 1, y: 0 }"
              :delay="100"
              class="indicators"
            >
              <div class="txt">
                <h2>HTML</h2>
                <p>100%</p>
              </div>
              <div class="percentage">
                <div class="percentage-line html"></div>
              </div>
            </div>

            <div
              v-motion
              :initial="{ opacity: 0, y: -100 }"
              :visible="{ opacity: 1, y: 0 }"
              :delay="250"
              class="indicators"
            >
              <div class="txt">
                <h2>CSS</h2>
                <p>90%</p>
              </div>
              <div class="percentage">
                <div class="percentage-line css"></div>
              </div>
            </div>

            <div
              v-motion
              :initial="{ opacity: 0, y: -100 }"
              :visible="{ opacity: 1, y: 0 }"
              :delay="450"
              class="indicators"
            >
              <div class="txt">
                <h2>SCSS/SASS</h2>
                <p>80%</p>
              </div>
              <div class="percentage">
                <div class="percentage-line scss"></div>
              </div>
            </div>

            <div
              v-motion
              :initial="{ opacity: 0, y: -100 }"
              :visible="{ opacity: 1, y: 0 }"
              :delay="550"
              class="indicators"
            >
              <div class="txt">
                <h2>JavaScript</h2>
                <p>75%</p>
              </div>
              <div class="percentage">
                <div class="percentage-line javascript"></div>
              </div>
            </div>

            <div
              v-motion
              :initial="{ opacity: 0, y: -100 }"
              :visible="{ opacity: 1, y: 0 }"
              :delay="650"
              class="indicators"
            >
              <div class="txt">
                <h2>VueJs</h2>
                <p>35%</p>
              </div>
              <div class="percentage">
                <div class="percentage-line vue"></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>


<script></script>



<style lang="scss">
.skill {
  width: 100%;
  margin-top: 100px;
  padding-bottom: 127px;
}

.head {
  width: 100%;
  padding: 93px 0px 93px 62px;
  background: #252525;
  border-top: 2px solid #333333;
  border-bottom: 2px solid #333333;
  h1 {
    font-weight: 700;
    font-size: 55px;
    line-height: 35px;
    color: #ffffff;
    transition: all 1s;
  }
}

.main-info {
  padding: 61px 107px 0px 62px;
  display: flex;
  gap: 100px;
}

.line {
  width: 200px;
  margin-top: 18px;
}
.lang-side {
  display: flex;
  flex-direction: column;

  .lang-header {
    transition: all 1s ease;
    h2 {
      font-weight: 700;
      font-size: 28px;
      line-height: 35px;
      color: #ffffff;
    }
  }

  .about {
    display: flex;
    align-items: flex-start;
    gap: 28px;
    margin-top: 35px;
    transition: all 1s;
    .text {
      width: 627px;
      display: flex;
      flex-direction: column;
      gap: 11px;

      h1 {
        font-weight: 700;
        font-size: 18px;
        line-height: 35px;
        color: #ffffff;
      }
      p {
        font-weight: 400;
        font-size: 16px;
        line-height: 30px;
        color: rgba(255, 255, 255, 0.7);
      }
    }
  }
}

.skill-side {
  display: flex;
  flex-direction: column;
  width: 100%;

  .skill-header {
    font-weight: 700;
    font-size: 28px;
    line-height: 35px;
    color: #ffffff;
    transition: all 1s;
  }
}

.indicator {
  width: 665px;
  margin-top: 23px;


  .indicators-div {
    display: flex;
    flex-direction: column;
    gap: 40px;
    .indicators {
      width: 100%;
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      transition: all 1s;

      .txt {
        width: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;
        h2 {
          font-weight: 700;
          font-size: 18px;
          line-height: 35px;
          color: #ffffff;
        }

        p {
          font-weight: 400;
          font-size: 14px;
          line-height: 35px;
          color: rgba(255, 255, 255, 0.7);
        }
      }

      .percentage {
        width: 100%;
        height: 15px;
        background-color: #4444;
        border-radius: 8px;
        overflow: hidden;
        display: flex;
        align-items: center;

        .percentage-line {
          &.html {
            width: 100%;
          }

          &.css {
            width: 90%;
          }

          &.scss {
            width: 80%;
          }

          &.javascript {
            width: 75%;
          }
          &.vue {
            width: 35%;
          }
          height: 7px;
          background-color: #007ced;
          border-radius: 8px;
          margin: 0px 5px 0px;
        }
      }
    }
  }
}
</style>
