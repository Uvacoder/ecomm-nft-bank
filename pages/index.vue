<template>
  <div>
    <!-- Hero Section -->
    <div class="main-hero-container">
      <h1 class="hero-title">
        <span class="main-title-highlight">No Code</span> NFT Tools
      </h1>
      <p class="hero-subtitle">
        A full-fledge studio to generate, customize and deploy NFTs
      </p>
    </div>
    <!-- Intro Section -->
    <div class="intro-section">
      <h2 class="title">
        Built for everyone to join the revolution of Digital Assets <br />
        stored in multiple decentralized networks
      </h2>
      <p class="description">
        NFT+ Studio was made to make it simple for anyone to work with NFT
        (Non-Fungible Tokens) without knowledge about coding or finding a
        developer.
      </p>
      <a href="https://app.nftplus.studio" target="_blank" class="primary-btn"
        >Open App</a
      >
    </div>
    <!-- Video Section -->
    <div class="video-section">  
      <iframe src="https://www.youtube-nocookie.com/embed/TNK-yRJ4-PI?rel=0&amp;controls=1&amp;autoplay=0&amp;mute=1&amp;start=0" frameBorder="0" style="position:absolute;left:0;top:0;width:100%;height:100%;pointer-events:auto" allow="autoplay; encrypted-media" allowfullscreen=""></iframe>
    </div>
    <!-- Services Section -->
    <div id="our-services" class="our-service-section">
      <h2 class="section-header-title">Our Services</h2>
      <div class="services-grid">
        <div class="card">
          <div class="card-content">
            <div class="card-icon">
              <img
                src="https://uploads-ssl.webflow.com/616d17f88acab6507439a0d2/616e8c8b84fc4ff489dc7e23_arts.svg"
                loading="lazy"
                alt="Arts Icon"
              />
            </div>
            <div class="card-info">
              <div class="card-title">Generative Art</div>
              <p class="card-description">
                Import a folder with assets or create your own layers. Configure
                traits, rarities, background palettes and more. Generate up to
                50,000 unique images with a click of a button.
                <span class="italic-bold">No coding required!</span>
              </p>
            </div>
          </div>
        </div>
        <div class="card">
          <div class="card-content">
            <div class="card-icon">
              <img
                src="https://uploads-ssl.webflow.com/616d17f88acab6507439a0d2/616e8f26b295545266c00db4_contract.svg"
                loading="lazy"
                alt="Smart Contract Icon"
              />
            </div>
            <div class="card-info">
              <div class="card-title">Custom Smart Contracts</div>
              <p class="card-description">
                Create custom smart contracts for your NFT collection,
                <span class="italic-bold">with no coding skills required.</span>
                We support Ethereum, Solana, and Binance Chain. It’s as easy as
                filling in a form and clicking the deploy button.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- Road Map Section -->
    <div id="roadmap" class="road-map-section">
       <h2 class="roadmap-title">Road Map</h2>
      <div class="img-container">
        <img
          src="https://uploads-ssl.webflow.com/616d17f88acab6507439a0d2/616eac8169cde240ec58f6b0_roadmap.png"
          alt=""
        />
      </div>
    </div>
    <!-- FAQ Section -->
    <div id="faq" class="faq-section">
      <h2 class="faq-title">Frequently Asked Questions</h2>
      <div class="faqs">
        <div class="question">
          <button class="collapsible" @click="toggle">
            Are your services free?
          </button>
          <div class="content">
            <p>
              We have a free tier for all our services but they are not
              completely free if you want access to custom features because of
              the cost in resources that we need to incur to provide these
              services.
            </p>
          </div>
        </div>
        <div class="question">
          <button class="collapsible" @click="toggle">
            Do I need to create an account to use these services?
          </button>
          <div class="content">
            <p>
              There is no need to create an account. Your project data is auto
              saved locally in your machine so if you leave the page and come
              back again, you can find all your projects including the ones in
              progress right where you left off. We'll only need your email
              address when paying so we can send you your receipt, a link to
              your generated files, or other useful information
            </p>
          </div>
        </div>
        <div class="question">
          <button class="collapsible" @click="toggle">
            What are the supported payment methods?
          </button>
          <div class="content">
            <p>We will only support crypto payments in the future.</p>
          </div>
        </div>
        <div class="question">
          <button class="collapsible" @click="toggle">
            Do I have copyright and commerical license to the images and smart
            contracts
          </button>
          <div class="content">
            <p>
              Yes, of course! They are your materials after all. Whether you use
              the free tier or paid tier, whatever you generate in our studio
              belongs to you and you have copyright and commercial license to
              them.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.main-hero-container {
  position: absolute;
  text-align: center;
  top: 20%;
  left: 15%;
  right: 15%;
}

.main-hero-container .main-title-highlight {
  background-image: -webkit-gradient(
    linear,
    left top,
    left bottom,
    from(#7a05eb),
    to(#ff00a1)
  );
  background-image: linear-gradient(180deg, #7a05eb, #ff00a1);
  color: #7a05eb;
  -webkit-background-clip: text;
  background-clip: text;
  -webkit-text-fill-color: transparent;
}

.hero-title {
  font-family: "Titillium Web", sans-serif;
  color: #fff;
  font-size: clamp(30px, 5vw, 72px);
  line-height: 109.51px;
  text-shadow: 0 4px 10px rgb(0 0 0 / 10%);
}

.hero-subtitle {
  position: relative;
  font-family: "Titillium Web", sans-serif;
  color: #fff;
  font-size: clamp(20px, 5vw, 48px); 
  line-height: 51px;
  font-weight: 400;
}

.intro-section {
  padding-top: 3em;
  padding-bottom: 3em;
  text-align: center;
}

.intro-section .title {
  font-size: clamp(10px, 5vw, 30px);
  line-height: 46px;
  text-align: center;
}

.intro-section .description {
  margin-bottom: 2em;
  font-family: "Titillium Web", sans-serif;
  color: rgba(0, 0, 0, 0.45);
  font-size: 24px;
  line-height: 36.5px;
  text-align: center;
}

.primary-btn {
  display: block;
  padding: 0.8em 1.5em;
  border-radius: 7px;
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
  width: max-content;
  height: max-content;
  margin: auto;
}

.our-service-section {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  gap: 3em;
  background-color: #f5fbff;
  height: 540px;
}

.section-header-title,
.faq-title, .roadmap-title {
  font-size: 30px;
  line-height: 46px;
  font-weight: 700;
  text-align: center;
}

.services-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2em;
  padding: 1.5em 4.5em;
}

.card {
  height: 255px;
  padding: 24px;
  border-radius: 6px;
  background-color: #fff;
  box-shadow: 0 4px 10px 0 rgb(0 0 0 / 10%);
}

.card-content {
  display: grid;
  grid-template-columns: auto auto;
  gap: 3.5em;
}

.card .card-content .card-icon {
  background-color: #00b2fe;
  height: 80px;
  width: 80px;
  align-items: center;
  margin-top: 6px;
  border-radius: 16px;
}

.card-icon img {
  width: 100%;
  height: 100%;
  padding: 0.5em;
}

.card-title {
  font-family: "Titillium Web", sans-serif;
  font-size: 24px;
  font-weight: 700;
  white-space: 0;
  text-align: left;
}

.card-description {
  margin-top: 10px;
  font-family: "Titillium Web", sans-serif;
  font-size: 17px;
  line-height: 27.382px;
  text-align: left;
}

.italic-bold {
  font-style: italic;
  font-weight: 700;
}

.faq-section { 
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  height: auto;
  min-height: 700px;
  background-color: #f5fbff;
}

.faqs { 
  width: 100%;
  padding: 1.5em 4.5em;
}

.question {
  display: block;
  margin: 2em; 
}

.question .collapsible {
  color: black;
  cursor: pointer;
  padding: 18px;
  width: 100%;
  border: none;
  text-align: left;
  outline: none;
  font-size: 15px;
  border-radius: 12px;
  background-color: #fff;
  box-shadow: 0 4px 10px 4px rgb(0 0 0 / 10%);
}

.question .active,
.collapsible:hover {
  box-shadow: 0 4px 10px 4px rgb(0 0 0 / 15%);
}

.collapsible:after {
  content: "\002B";
  color: #555;
  font-weight: bold;
  float: right;
  margin-left: 5px;
}

.active:after {
  content: "\2212";
}

.content {
  display: none;
  padding: 0 18px;
  margin-top: 1.5em;
  margin-left: 2em;
  padding: 1em;
  overflow: hidden;
  transition: max-height 0.6s ease-out;
  background-color: #fff;
}

.road-map-section {
  background-color: #fff;
}

.road-map-section .img-container {
  padding: 1.5em 4.5em;
}

.roadmap-title {
  padding-top: 2em;
}

.video-section {
  position: relative;
  max-width: 90%; 
  height: 90vh; 
  position: relative;
  padding: 0;
  margin: auto;
  background-image: url(https://d3e54v103j8qbb.cloudfront.net/static/youtube-placeholder.2b05e7d68d.svg);
  background-size: cover;
  background-position: 50% 50%;
}

@media only screen and (max-width: 600px) {
  .main-hero-container {
    top: 40%;
  }

  .faqs {
    padding: 0;
  }
}

</style>

<script>
export default {
  methods: {
    toggle(e) {
      let faq = e.target;
      document.querySelectorAll('.question .collapsible').forEach(el => {
        //remove styling from all elements
        el.classList.remove('active');
        el.nextElementSibling.style.display = "none";
        //update collapsible styling for element clicked
        faq.classList.add('active');
        faq.nextElementSibling.style.display = "block";
      });
    }
  }
}
</script>
