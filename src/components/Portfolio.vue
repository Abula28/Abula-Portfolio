<template>
  <section class="portfolio" id="portfolio">
    <div class="head">
      <h1 v-motion-fade-visible>Portfolio</h1>
    </div>
    <div class="projects-div">
      <div v-motion-roll-visible-right class="project-header">
        <h3>My <span class="spanColor">Projects</span></h3>
      </div>

      <div class="projects">
        <div 
        v-motion
        :initial="{opacity: 0, y: -100}"
        :visible="{opacity: 1, y: 0}"
        :delay="100"
        class="proj">
          <h1>Space Tourism Website</h1>
          <a
            href="https://abula28.github.io/Space-Tourism-Website/"
            target="_blank"
          >
            <div class="projects-img">
              <img
                src="./icons/space-tourism-website-img.png"
                alt="space website"
              />
              <div class="layer">
                <h3>View</h3>
              </div>
            </div>
          </a>
        </div>

        <div v-motion
        :initial="{opacity: 0, y: 100}"
        :visible="{opacity: 1, y: 0}"
        :delay="300" class="proj">
          <h1>Fylo Landing page</h1>
          <a
            href="https://abula28.github.io/Fylo-Landing-Page/"
            target="_blank"
          >
            <div class="projects-img">
              <img
                src="./icons/fylo-landing-page-img.png"
                alt="space website"
              />
              <div class="layer">
                <h3>View</h3>
              </div>
            </div>
          </a>
        </div>

        <div v-motion
        :initial="{opacity: 0, y: -100}"
        :visible="{opacity: 1, y: 0}"
        :delay="500" class="proj">
          <h1>Todo App</h1>
          <a
            href="https://abula28.github.io/Todo-App/"
            target="_blank"
          >
            <div class="projects-img">
              <img
                src="./icons/todo-list-img.png"
                alt="space website"
              />
              <div class="layer">
                <h3>View</h3>
              </div>
            </div>
          </a>
        </div>

        <div v-motion
        :initial="{opacity: 0, y: 100}"
        :visible="{opacity: 1, y: 0}"
        :delay="700" class="proj">
          <h1>Advice Generator</h1>
          <a
            href="https://abula28.github.io/Advice-Generator/"
            target="_blank"
          >
            <div class="projects-img">
              <img
                src="./icons/advice-generator-img.png"
                alt="space website"
              />
              <div class="layer">
                <h3>View</h3>
              </div>
            </div>
          </a>
        </div>


      </div>
    </div>
  </section>
</template>


<script>
</script>

<style lang="scss">
.portfolio {
  margin-top: 100px;
  padding-bottom: 100px;
}

.projects-div {
  padding-top: 47px;
  .project-header {
    transition: all 1s;
    h3 {
      font-weight: 700;
      font-size: 28px;
      line-height: 35px;
      color: #ffffff;
      text-align: center;
    }
  }
}

.projects {
  width: 100%;
  margin-top: 80px;
  padding: 0px 62px 0px;
  display: flex;
  justify-content: center;
  gap: 20px;
  align-items: center;
  flex-wrap: wrap;

  .proj {
    display: flex;
    flex-direction: column;
    gap: 20px;
    transition: all 1s;

    a {
      text-decoration: none;
    }

    h1 {
      font-weight: 700;
      font-size: 28px;
      line-height: 35px;
      color: #ffffff;
    }

    .projects-img {
      width: 350px;
      height: 180px;
      position: relative;
      z-index: 2;
      border-radius: 25px;
      overflow: hidden;
      cursor: pointer;
      img {
        width: 100%;
        height: 100%;
      }
      .layer {
        position: absolute;
        left: 0;
        top: 0;
        z-index: 3;
        width: 100%;
        height: 100%;
        background: transparent;
        transition: all 0.5s;
        h3 {
          widows: 100%;
          font-weight: 700;
          color: #007ced;
          font-size: 26px;
          bottom: 0;
          left: 50%;
          position: absolute;
          transform: translateX(-50%);
          opacity: 0;
          transition: all 0.5s;
        }
        &:hover {
          background: rgba(68, 68, 68, 0.8);
        }
        &:hover h3 {
          opacity: 1;
          bottom: 50%;
          transform: translate(-50%, 50%);
        }
      }
    }
  }
}
</style>
