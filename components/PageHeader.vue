<template>
  <nav id="main-nav">
    <div class="w-col w-col-8">
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
</template>
<style scoped>
#main-nav {
  display: grid;
  grid-template-columns: 200px 1fr;
  padding: 1.5em 4.5em;
  /* height: 570px;
  background-image: url("https://uploads-ssl.webflow.com/616d17f88acab6507439a0d2/616d18ec52009be11f4a23a0_vecteezy_retro-futurism-background_en0121_generated.jpg");
  background-position: 0 0;
  background-size: cover; */
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
</style>
<script>

export default {
  name: 'PageHeader',
};
</script>
