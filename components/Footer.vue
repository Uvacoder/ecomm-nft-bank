<template>
  <footer id="footer" class="footer wf-section">
    <div class="website-container w-container">
      <div class="footer-flex-container">
        <div>
          <a href="#" class="link-block w-inline-block"
            ><img
              src="https://uploads-ssl.webflow.com/616d17f88acab6507439a0d2/6173d9ac2ea50e62cf676dba_logo.png"
              loading="lazy"
              alt="NFT+ Studio Logo"
              class="footer-logo"
          /></a>
          <div class="copyright-text">Copyright © 2021 NFT+ Studio</div>
        </div>
        <div>
          <h3 class="footer-heading">Site Content</h3>
          <ul role="list" class="w-list-unstyled">
            <li><a href="#our-services" class="footer-link">Services</a></li>
            <li><a href="#roadmap" class="footer-link">Roadmap</a></li>
            <li><a href="#faq" class="footer-link">FAQ</a></li>
          </ul>
        </div>
        <div>
          <h3 class="footer-heading">Legal</h3>
          <ul role="list" class="w-list-unstyled">
            <li><a href="#" class="footer-link">Terms of Service</a></li>
            <li><a href="#" class="footer-link">Privacy Policy</a></li>
          </ul>
        </div>
        <div>
          <h3 class="footer-heading">Community</h3>
          <ul role="list" class="w-list-unstyled">
            <li>
              <a
                href="https://discord.gg/t8pRYMyg3H"
                target="_blank"
                class="footer-link"
                >Discord</a
              >
            </li>
            <li>
              <a
                href="https://twitter.com/NFTPlusStudio"
                target="_blank"
                class="footer-link"
                >Twitter</a
              >
            </li>
            <li><a href="#" class="footer-link">Instagram</a></li>
          </ul>
        </div>
      </div>
      <div class="powered-by-text">
        Powered by
        <span class="footer-link-highlight">Nebula Core Technologies</span>
      </div>
    </div>
  </footer>
</template>
<style>
footer {
  padding-top: 60px;
  padding-bottom: 40px;
  -webkit-box-align: start;
  -webkit-align-items: flex-start;
  -ms-flex-align: start;
  align-items: flex-start;
  background-color: #110458;
  text-align: center;
}
.footer-flex-container {
  display: -webkit-box;
  display: -webkit-flex;
  display: -ms-flexbox;
  display: flex;
  margin-bottom: 40px;
  -webkit-box-pack: justify;
  -webkit-justify-content: space-between;
  -ms-flex-pack: justify;
  justify-content: space-between;
  text-align: left;
}
.footer-logo-link {
  max-height: 60px;
  min-width: 60px;
  -webkit-box-flex: 0;
  -webkit-flex: 0 auto;
  -ms-flex: 0 auto;
  flex: 0 auto;
}
.footer-image {
  width: 100%;
  height: 100%;
  -o-object-fit: contain;
  object-fit: contain;
  -o-object-position: 0% 50%;
  object-position: 0% 50%;
}
.footer-heading {
  margin-top: 0;
  margin-bottom: 20px;
  font-family: "Titillium Web", sans-serif;
  color: #fff;
  font-size: 16px;
  line-height: 1.5;
}
.footer-link {
  display: block;
  margin-bottom: 10px;
  font-family: "Titillium Web", sans-serif;
  color: #bcabfe;
  font-size: 16px;
  text-decoration: none;
}
.footer-link:hover {
  text-decoration: underline;
}
.footer-logo {
  display: block;
  width: 155px;
  height: 67px;
  max-width: none;
  margin-bottom: 1em;
  text-align: left;
}
.image-2 {
  max-width: none;
}
.copyright-text {
  font-family: "Titillium Web", sans-serif;
  color: #fff;
  font-size: 12px;
  font-weight: 300;
}
.link-block {
  text-align: left;
}
.powered-by-text {
  font-family: "Titillium Web", sans-serif;
  color: #fff;
  font-size: 12px;
  font-weight: 300;
}
.footer-link-highlight {
  color: #bcabfe;
}
</style>

<script> 

export default {
  name: 'Footer',
  computed: {
    siteName() {
      return global.siteName;
    },
  },
};
</script>
