<template>
  <footer>
    <div class="footer">
      <b-container class="footer-boot">
        <b-row cols-lg="12">
          <b-col class="links">
            <h5>Links</h5>
            <div class="link-redirects"><a href="#">Link</a> <br /></div>
          </b-col>

          <b-col name="icon-exits">
            <div class="icons">
              <a href="https://google.com" target="_blank">
                <img src="../assets/socials/github.png" class="icon" />
              </a>
              <a href="#" target="_blank">
                <img src="../assets/socials/linkedin.png" class="icon" />
              </a>
              <a href="#" target="_blank">
                <img src="../assets/socials/discord.png" class="icon" />
              </a>
            </div>
          </b-col>

          <b-col class="contact-me">
            <h5>Contact Me</h5>
            <b-row cols="12" cols-sm="2" cols-md="8" cols-lg="12">
              <b-col>
                <ul class="contact-info">
                  <li style="font-size: 105%; font-style: bold">Phone:</li>
                  <li style="font-size: 90%">123-456-7890</li>
                </ul>
              </b-col>
              <b-col class="contact-info">
                <li style="font-size: 105%; font-style: bold">Email:</li>
                <li style="font-size: 90%">ekh3@njit.edu</li>
              </b-col>
            </b-row>
          </b-col>
        </b-row>
      </b-container>
      <h6>By: Ethan H.</h6>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style scoped>
:root {
  --footer-color: ;
  --footer-text-color: rgb(73, 73, 73);
}

footer {
  color: var(--footer-text-color);
  background: linear-gradient(0deg, rgb(199, 199, 199), rgb(196, 196, 196) 95%);
  text-align: center;
  justify-content: center;
  bottom: 0%;
  padding-top: 15px;
  padding-bottom: 5px;
}

.icons {
  padding-top: 5px;
  padding-bottom: 5px;
  justify-content: center;
  text-align: center;
}

.icon {
  display: inline;
  padding: 2%;
  padding-left: 3%;
  padding-right: 3%;
}

.icon:hover,
.icon:focus {
  border-radius: 20px;
  background-color: rgba(153, 153, 153, 0.205);
  animation: raiseIn 200ms ease-in-out;
  animation-fill-mode: forwards;
}

.contact-me,
.links {
  border: 1px #3d1717;
  border-style: solid;
  margin-left: 5px;
  margin-right: 5px;
  justify-content: center;
  text-align: center;
}

.contact-info {
  float: initial;
  overflow: auto;
  list-style: none;
  text-align: left;
  justify-content: center;
  padding: 0;
  width: 3fr;
}

.link-redirects {
  text-align: left;
  font-style: italic;
  text-decoration-line: underline;
  width: 2fr;
}

a:link,
a:visited {
  color: rgb(73, 73, 73);
  text-decoration: none;
}

a:hover {
  color: #fcfcfc;
}

@keyframes raiseIn {
  from {
    transform: scale(1);
  }

  to {
    transform: scale(0.85);
  }
}
</style>