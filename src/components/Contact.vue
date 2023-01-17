<template>
  <section class="contact" id="contact">
    <div class="head">
      <h1 v-motion-fade-visible>Contact</h1>
    </div>

    <div class="contact-icons">
      <div
      v-motion
      :initial="{opacity: 0, x: -50}"
      :visible="{opacity: 1, x: 0}"
      :delay="100"
      
      class="icons">
        <p>Gmail:</p>
        <a
          href="https://mail.google.com/mail/u/1/#search/nikaabuladze28%40gmail.com?compose=new"
          target="_blank"
        >
          <i class="fa-regular fa-envelope"></i>
        </a>
      </div>

      <div
      v-motion
      :initial="{opacity: 0, x: -50}"
      :visible="{opacity: 1, x: 0}"
      :delay="300"
      
      class="icons">
        <p>Facebook:</p>
        <a
          href="https://www.facebook.com/profile.php?id=100011452353777"
          target="_blank"
        >
          <i class="fa-brands fa-facebook-f"></i>
        </a>
      </div>

      <div
      v-motion
      :initial="{opacity: 0, x: -50}"
      :visible="{opacity: 1, x: 0}"
      :delay="500"
      
      class="icons">
        <p>Instagram:</p>
        <a
          href="https://www.instagram.com/abulaa77/"
          target="_blank"
        >
          <i class="fa-brands fa-instagram"></i>
        </a>
      </div>

      <div
      v-motion
      :initial="{opacity: 0, x: -50}"
      :visible="{opacity: 1, x: 0}"
      :delay="700"
      
      class="icons">
        <p>Github:</p>
        <a href="https://github.com/Abula28" target="_blank">
          <i class="fa-brands fa-github"></i>
        </a>
      </div>

      <div
      v-motion
      :initial="{opacity: 0, x: -50}"
      :visible="{opacity: 1, x: 0}"
      :delay="800"
      
      class="icons">
        <p>Linkedin:</p>
        <a
          href="https://www.linkedin.com/in/nikoloz-abuladze-21304a21a/"
          target="_blank"
        >
          <i class="fa-brands fa-linkedin"></i>
        </a>
      </div>
    </div>
  </section>
</template>


<script></script>

<style lang="scss">
.contact {
  margin-top: 100px;
}

.contact-icons {
  margin: 40px 62px 0px;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 40px;

  .icons {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;
    transition: all 1s;
    p {
      font-size: 18px;
      color: #ffff;
      font-weight: 500;
    }
    i {
      font-size: 48px;
      cursor: pointer;
      color: #007ced;
      transition: all 0.5s;

      &:hover {
        opacity: 0.5;
      }
    }
  }
}
</style>
