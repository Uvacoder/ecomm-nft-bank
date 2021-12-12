<template>
  <nav id="main-nav"> 
    <div class="logo-container">
      <a href="/">
        <img
        src="https://uploads-ssl.webflow.com/616d17f88acab6507439a0d2/6173d9ac2ea50e62cf676dba_logo.png"
        loading="lazy"
        height="81"
        alt="NFT+ Studio Logo"
      />
      </a>
    </div> 
    <div class="nav-container">
      <ul role="list" class="nav-list">
        <li class="main-menu-item">
          <a href="#our-services" class="main-menu-item-link">Services</a>
        </li>
        <li class="main-menu-item">
          <a href="#roadmap" class="main-menu-item-link">Roadmap</a>
        </li>
        <li class="main-menu-item">
          <a href="#faq" class="main-menu-item-link">FAQ</a>
        </li>
      </ul>
      <div class="div-block">
        <a href="https://app.nftplus.studio" target="_blank" class="primary-btn"
          >Open App</a
        >
      </div>
    </div>
  </nav>
  <!-- <div id="roadmap" class="roadmap-section wf-section">
      <div class="website-container section-container w-container">
        <h2 class="section-header-title">The Roadmap</h2>
        <div class="div-block-4"></div>
      </div>
    </div>
    <div id="faq" class="faq-section wf-section">
      <div class="website-container section-container w-container">
        <h2 class="section-header-title">Frequently Asked Questions</h2>
        <div class="faq-container">
          <div data-hover="false" data-delay="0" class="faq-item w-dropdown">
            <div class="dropdown-toggle w-dropdown-toggle">
              <div class="faq-icon w-icon-dropdown-toggle"></div>
              <div class="toggle-text">Are these services free?</div>
            </div>
            <nav class="dropdown-list w-dropdown-list">
              <div class="faq-body-cont">
                <div class="faq-body-text">
                  We have a free tier for all our services but they are not
                  completely free if you want access to custom features because
                  of the cost in resources that we need to incur to provide
                  these services.
                </div>
              </div>
            </nav>
          </div>
          <div data-hover="false" data-delay="0" class="faq-item w-dropdown">
            <div class="dropdown-toggle w-dropdown-toggle">
              <div class="faq-icon w-icon-dropdown-toggle"></div>
              <div class="toggle-text">
                Do I need to create an account to use these services?
              </div>
            </div>
            <nav class="dropdown-list w-dropdown-list">
              <div class="faq-body-cont">
                <div class="faq-body-text">
                  There is no need to create an account. Your project data is
                  auto saved locally in your machine so if you leave the page
                  and come back again, you can find all your projects including
                  the ones in progress right where you left off. We&#x27;ll only
                  need your email address when paying so we can send you your
                  receipt, a link to your generated files, or other useful
                  information
                </div>
              </div>
            </nav>
          </div>
          <div data-hover="false" data-delay="0" class="faq-item w-dropdown">
            <div class="dropdown-toggle w-dropdown-toggle">
              <div class="faq-icon w-icon-dropdown-toggle"></div>
              <div class="toggle-text">
                What are the supported payment methods?
              </div>
            </div>
            <nav class="dropdown-list w-dropdown-list">
              <div class="faq-body-cont">
                <div class="faq-body-text">
                  We will only support crypto payments in the future.
                </div>
              </div>
            </nav>
          </div>
          <div data-hover="false" data-delay="0" class="faq-item w-dropdown">
            <div class="dropdown-toggle w-dropdown-toggle">
              <div class="faq-icon w-icon-dropdown-toggle"></div>
              <div class="toggle-text">
                Do I have copyrights and commercial license to the images and
                smart contracts?
              </div>
            </div>
            <nav class="dropdown-list w-dropdown-list">
              <div class="faq-body-cont">
                <div class="faq-body-text">
                  Yes, of course! They are your materials after all. Whether you
                  use the free tier or paid tier, whatever you generate in our
                  studio belongs to you and you have copyright and commercial
                  license to them.
                </div>
              </div>
            </nav>
          </div>
        </div>
      </div>
    </div> -->
</template>
<style scoped>
#main-nav {
  display: grid;
  grid-template-columns: 200px 1fr;
  padding: 1.5em 4.5em;
  height: 570px;
  background-image: url("https://uploads-ssl.webflow.com/616d17f88acab6507439a0d2/616d18ec52009be11f4a23a0_vecteezy_retro-futurism-background_en0121_generated.jpg");
  background-position: 0 0;
  background-size: cover;
}

#main-nav .primary-btn {
  display: block;
  width: max-content;
  height: 50px;
  padding: 0.6em 1.4em;
  border-radius: 7px;
  color: aliceblue;
  background-image: -webkit-gradient(
    linear,
    left top,
    left bottom,
    from(#ff00a1),
    color-stop(84%, #ff114f)
  );
  background-image: linear-gradient(180deg, #ff00a1, #ff114f 84%);
  font-family: "Titillium Web", sans-serif;
  font-size: 18px;
  font-weight: 600;
}

#main-nav .nav-container {
  display: flex;
  gap: 4em;
  justify-content: end;
  height: max-content;
}

#main-nav .nav-list {
  display: flex;
  gap: 1.5em;
  justify-content: center;
  margin: auto 0;
  font-weight: bolder;
  transition: all 1s;
}
#main-nav .nav-list li {
  color: #bcabfe;
  transition: color 0.6s;
}

#main-nav .nav-list li:hover {
  color: #ff00a1;
  transition: color 0.6s;
}

@media only screen and (max-width: 600px) {
  #main-nav {
    grid-template-columns: 1fr;
    gap: 0;
  }

  #main-nav .nav-container {
    position: relative;
    display: grid;
    grid-template-columns: 1fr;
    gap: 2em; 
    place-items: center;
    top: -120px;
  }
}
</style>
<script>

export default {
  name: 'Header',
};
</script>
