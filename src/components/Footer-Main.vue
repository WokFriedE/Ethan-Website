<template>
  <footer>

    <div class="footer">
      <!-- General fade in -->
      <b-container class="footer-boot">
        <b-row>
          <!-- icons -->
          <b-col name="icon-exits">
            <div class="icons">
              <a href="https://github.com/WokFriedE" target="_blank">
                <img src="../assets/socials/github.png" class="icon" />
              </a>
              <a href="https://www.linkedin.com/in/ethan-ho-46a032233/" target="_blank">
                <img src="../assets/socials/linkedin.png" class="icon" />
              </a>
              <a href="mailto:ekh3@njit.edu" target="">
                <img src="../assets/socials/mail.png" class="icon" />
              </a>
            </div>
          </b-col>
        </b-row>
      </b-container>
      <h6 style="font-size: small; ">© Ethan Ho 2022</h6>
    </div>
  </footer>
</template>

<script>

export default {
  data() {
    return {
    };
  },
};
</script>

<style>
footer {
  color: var(--footer-text-color);
  background-color: dimgrey;
  text-align: center;
  justify-content: center;
  bottom: 0%;
  padding-bottom: 0.01%;
}

.icons {
  padding-top: 5px;
  padding-bottom: 5px;
  justify-content: center;
  text-align: center;
}

.icon {
  display: inline;
  margin-inline: 0.5%;
  padding: 0.5%;
  transform: scale(0.95);
}

.icon:hover,
.icon:focus {
  border-radius: 20px;
  background-color: rgba(153, 153, 153, 0.205);
  animation: raiseIn 200ms ease-in-out;
  animation-fill-mode: forwards;
}

.icon:not(:hover) {
  animation: raiseOut 200ms ease-in-out;
  animation-fill-mode: forwards;
}
</style>