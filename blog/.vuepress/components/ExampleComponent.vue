<template>
  <!-- Component html here -->
  <a :href="link">
    <img :src="buttonImage" :alt="buttonAlt" />
  </a>
</template>

<script>
export default {
/* Component js here */
    data() {
        return {
            link: "https://app.netlify.com/start/deploy?repository=https://github.com/p440davis/VuePress-Blog-with-Netlify-CMS&amp;stack=cms",
            buttonImage: "https://www.netlify.com/img/deploy/button.svg",
            buttonAlt: "Deploy to Netlify"
        }
    }
}
</script>

<style scoped>
/* Component css here */
a {
  display: inline-block;
}
</style>