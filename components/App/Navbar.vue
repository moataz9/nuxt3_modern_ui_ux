<script setup lang="ts">
const toggleMenu = ref(false)
</script>

<template>
  <div>
    <div class="gpt3__navbar">
      <div class="gpt3__navbar-links">
        <div class="gpt3__navbar-links_logo">
          <img src="/images/logo.png" />
        </div>
        <div class="gpt3__navbar-links_container">
          <p><a href="#home">Home</a></p>
          <p><a href="#wgpt3">What is GPT3?</a></p>
          <p><a href="#possibility">Open AI</a></p>
          <p><a href="#features">Case Studies</a></p>
          <p><a href="#blog">Library</a></p>
        </div>
      </div>
      <div class="gpt3__navbar-sign">
        <p>Sign in</p>
        <button type="button">Sign up</button>
      </div>
      <div class="gpt3__navbar-menu">
        <Icon v-if="toggleMenu" @click="toggleMenu = false" name="fa:close" size="27" color="#fff" />
        <Icon v-else @click="toggleMenu = true" name="fa:bars" size="27" color="#fff" />
        <div v-if="toggleMenu" class="gpt3__navbar-menu_container scale-up-center">
          <div class="gpt3__navbar-menu_container-links">
            <p><a href="#home">Home</a></p>
            <p><a href="#wgpt3">What is GPT3?</a></p>
            <p><a href="#possibility">Open AI</a></p>
            <p><a href="#features">Case Studies</a></p>
            <p><a href="#blog">Library</a></p>
          </div>
          <div class="gpt3__navbar-menu_container-links-sign">
            <p>Sign in</p>
            <button type="button">Sign up</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.gpt3__navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 2rem 6rem;

  &-links {
    flex: 1;
    display: flex;
    justify-content: flex-start;
    align-items: center;

    &_logo {
      margin-right: 2rem;
      img {
        width: 62.56px;
        //height: 16.02px;
        filter: contrast(150%)
      }
    }

    &_container {
      display: flex;
      flex-direction: row;
    }
  }
}

.gpt3__navbar-sign {
  display: flex;
  justify-content: flex-end;
  align-items: center;
}

.gpt3__navbar-links_container p,
.gpt3__navbar-sign p,
.gpt3__navbar-menu_container p {
  color: #fff;
  font-family: var(--font-family);
  font-weight: 500;
  font-size: 18px;
  line-height: 25px;
  text-transform: capitalize;

  margin: 0 1rem;
  cursor: pointer;
}

.gpt3__navbar-sign button,
.gpt3__navbar-menu_container button {
  padding: 0.5rem 1rem;
  color: #fff;
  background: #ff4820;
  font-family: var(--font-family);
  font-weight: 500;
  font-size: 18px;
  line-height: 25px;
  border: none;
  outline: none;
  cursor: pointer;
  border-radius: 5px;
}

.gpt3__navbar-menu {
  margin-left: 1rem;
  display: none;
  position: relative;

  svg {
    cursor: pointer;
  }

  &_container {
    display: flex;
    justify-content: flex-end;
    align-items: flex-end;
    flex-direction: column;

    text-align: end;
    background: var(--color-footer);
    padding: 2rem;
    position: absolute;
    right: 0;
    top: 40px;
    margin-top: 1rem;
    min-width: 210px;
    border-radius: 5px;
    box-shadow: 0px 0px 5px rgba(0, 0, 0, 0.2);

    p {
      margin: 1rem 0;
    }
    &-links-sign {
      display: none;
    }
  }
}

@media screen and (max-width: 1050px) {
  .gpt3__navbar-links_container {
    display: none;
  }

  .gpt3__navbar-menu {
    display: flex;
  }
}

@media screen and (max-width: 700px) {
  .gpt3__navbar {
    padding: 2rem 4rem;
  }
}

@media screen and (max-width: 550px) {
  .gpt3__navbar {
    padding: 2rem;

    &-sign {
      display: none;
    }
  }

  .gpt3__navbar-menu_container {
    top: 20px;
    &-links-sign {
      display: block;
    }
  }
}
</style>
