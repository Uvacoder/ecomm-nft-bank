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
          <a href="/#our-services" class="main-menu-item-link">Services</a>
        </li>
        <li class="main-menu-item">
          <a href="/#roadmap" class="main-menu-item-link">Roadmap</a>
        </li>
        <li class="main-menu-item">
          <a href="/#faq" class="main-menu-item-link">FAQ</a>
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
  box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 12px;
  background: #C33764;  /* fallback for old browsers */
  background: -webkit-linear-gradient(to right, #1D2671, #C33764);  /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to right, #1D2671, #C33764); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
}

#main-nav .primary-btn {
  display: block;
  width: max-content;
  height: min-content;
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
  height: fit-content; 
  margin: auto 0; 
}

#main-nav .nav-list {
  display: flex;
  gap: 1.5em;
  justify-content: center;
  margin: auto 0;
  font-weight: bolder;
  transition: all 1s;
  font-family: "Titillium Web", sans-serif;
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
    top: 0;
    left: 0;
  }

  #main-nav .logo-container {
    display: flex;
    justify-content: center;
  }
}
</style>
<script>

export default {
  name: 'PageHeader',
};
</script>
