<template>
  <footer>
    <div class="footer">
      <b-container class="footer-boot">
        <b-row>
          <b-col class="links">
            <h5>Links</h5>
            <div class="link-redirects"><a href="#">hard vibes</a> <br /></div>
          </b-col>
          <b-col class="contact-us">
            <h5>Contact Us</h5>
            <b-row>
              <b-col>
                <ul class="contact-info">
                  <li style="font-size: 105%">Email:</li>
                  <li style="font-size: 90%">ekh3@njit.edu</li>
                </ul>
              </b-col>
              <b-col>
                <ul class="contact-info">
                  <li style="font-size: 105%">Located:</li>
                  <li style="font-size: 90%">Somewhere in US</li>
                </ul>
              </b-col>
            </b-row>
          </b-col>
        </b-row>
        <b-row class="icons">
          <b-nav v-for="value in socials" v-bind:key="value.title">
            <b-col>
              <b-nav-item v-bind:href="value.url" class="icon">
                <img v-bind:src="value.img_source" />
              </b-nav-item>
            </b-col>
          </b-nav>
        </b-row>
      </b-container>
      <h6>By Ethan H.</h6>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      //Social media links to be displayed in the footer
      socials: [
        {
          title: "LinkedIn",
          img_source:
            "https://cdn3.iconfinder.com/data/icons/popular-services-brands/512/linkedin-48.png",
          url: "",
        },
        {
          title: "Discord",
          img_source:
            "https://cdn3.iconfinder.com/data/icons/popular-services-brands-vol-2/512/discord-48.png",
          url: "",
        },
        {
          title: "Instagram",
          img_source:
            "https://cdn3.iconfinder.com/data/icons/popular-services-brands/512/instagram-48.png",
          url: "",
        },
        {
          title: "GitHub",
          img_source:
            "https://cdn3.iconfinder.com/data/icons/popular-services-brands/512/github-48.png",
          url: "",
        },
      ],
    };
  },
};
</script>

<style scoped>
footer {
  color: rgb(73, 73, 73);
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
  padding: 0%;
}

.icon:hover {
  border-radius: 20px;
  background-color: rgba(153, 153, 153, 0.205);
  animation: raiseIn 200ms ease-in-out;
  animation-fill-mode: forwards;
}

.contact-us,
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