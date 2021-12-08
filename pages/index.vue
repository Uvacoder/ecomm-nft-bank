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
        <a
          href="https://app.nftplus.studio"
          target="_blank"
          class="primary-btn"
          >Open App</a
        > 
    </div> 
    <!-- Services Section -->
    <div id="our-services" class="our-service-section wf-section">
      <div class="section-container website-container w-container">
        <h2 class="section-header-title">Our Services</h2>
        <div class="columns-2 w-row">
          <div class="w-col w-col-6">
            <div class="content-card">
              <div class="w-row">
                <div class="column-2 w-col w-col-3">
                  <div class="our-service-icon-container">
                    <img
                      src="https://uploads-ssl.webflow.com/616d17f88acab6507439a0d2/616e8c8b84fc4ff489dc7e23_arts.svg"
                      loading="lazy"
                      width="62"
                      alt="Arts Icon"
                      class="our-service-icon"
                    />
                  </div>
                </div>
                <div class="w-col w-col-9">
                  <div class="our-service-title-text">Generative Art</div>
                  <p class="our-service-description">
                    Import a folder with assets or create your own layers.
                    Configure traits, rarities, background palettes and more.
                    Generate up to 50,000 unique images with a click of a
                    button. <span class="italic-bold">No coding required!</span>
                  </p>
                </div>
              </div>
            </div>
          </div>
          <div class="w-col w-col-6">
            <div class="content-card w-row">
              <div class="column-3 w-col w-col-3">
                <div class="our-service-icon-container contract-icon-container">
                  <img
                    src="https://uploads-ssl.webflow.com/616d17f88acab6507439a0d2/616e8f26b295545266c00db4_contract.svg"
                    loading="lazy"
                    width="60"
                    alt="Smart Contract Icon"
                    class="our-service-icon"
                  />
                </div>
              </div>
              <div class="w-col w-col-9">
                <div class="our-service-title-text">Custom Smart Contracts</div>
                <p class="our-service-description">
                  Create custom smart contracts for your NFT collection,
                  <span class="italic-bold"
                    >with no coding skills required.</span
                  >
                  We support Ethereum, Solana, and Binance Chain. It’s as easy
                  as filling in a form and clicking the deploy button.
                </p>
              </div>
            </div>
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
    background-image: -webkit-gradient(linear,left top,left bottom,from(#7a05eb),to(#ff00a1));
    background-image: linear-gradient(
180deg,#7a05eb,#ff00a1);
    color: #7a05eb;
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
  }

  .hero-title {
    font-family: 'Titillium Web',sans-serif;
    color: #fff;
    font-size: 72px;
    line-height: 109.51px;
    text-shadow: 0 4px 10px rgb(0 0 0 / 10%);
  }

  .hero-subtitle {
    position: relative;
    font-family: 'Titillium Web',sans-serif;
    color: #fff;
    font-size: 48px;
    line-height: 51px;
    font-weight: 400;
  }

  .intro-section {
    padding-top: 3em;
    padding-bottom: 3em;
    text-align: center;
  }
  
  .intro-section .title {
    font-size: 30px;
    line-height: 46px;
    text-align: center;
  }

  .intro-section .description {
    margin-bottom: 2em;
    font-family: 'Titillium Web',sans-serif;
    color: rgba(0,0,0,.45);
    font-size: 24px;
    line-height: 36.5px;
    text-align: center;
  }

  .primary-btn {
    display: block;
    padding: 0.8em 1.5em;
    border-radius: 7px;
    background-image: -webkit-gradient(linear,left top,left bottom,from(#ff00a1),color-stop(84%,#ff114f));
    background-image: linear-gradient(
180deg,#ff00a1,#ff114f 84%);
    font-family: 'Titillium Web',sans-serif;
    font-size: 18px;
    font-weight: 600;
    width: max-content;
    height: max-content;
    margin: auto;
  }
</style>

<script></script>
