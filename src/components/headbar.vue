<template>
    <header>
      <nav id="headbar">
        <div class="head-container">
          <div class="head-brand">
          <h1 style="margin:0">TC Club</h1>
          </div>
          <div class="head-links">
            <router-link to="/">
              HOME
            </router-link>
            <router-link to="/about">
              ABOUT
            </router-link>
          </div>
        </div>
      </nav>
    </header>
</template>>

<style scoped>
#headbar {
  height: 8vh;
}
.head-container {
  height: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 75%;
  margin: 0 auto;
}
.head-links a {
  padding: 10px 20px;
  color: black;
  font-size: 1.5rem;
  text-decoration-line: none;
}
</style>