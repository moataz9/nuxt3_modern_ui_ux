<script setup lang="ts"></script>

<template>
  <div class="gpt3__brand section__padding">
    <div>
      <img src="~/assets/images/google.png" />
    </div>
    <div>
      <img src="~/assets/images/slack.png" />
    </div>
    <div>
      <img src="~/assets/images/atlassian.png" />
    </div>
    <div>
      <img src="~/assets/images/dropbox.png" />
    </div>
    <div>
      <img src="~/assets/images/shopify.png" />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.gpt3__brand {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;

  div {
    flex: 1;
    max-width: 150px;
    min-width: 120px;
    margin: 1rem;
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
</style>
