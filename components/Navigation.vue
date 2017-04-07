<template lang="html">
  <nav>
    <li v-for="(link, key) in links">
      <nuxt-link exact :to="link.href">{{link.title}}</nuxt-link>
    </li>
  </nav>
</template>

<script>
export default {
  data () {
    return {
      links: [{
        href: '/',
        title: 'Home'
      }, {
        href: '/about',
        title: 'About'
      }, {
        href: '/contact',
        title: 'Contact'
      }]
    }
  }
}
</script>

<style lang="scss">
nav {
    display: flex;
    justify-content: center;
    background: #35495e;
    li {
        list-style-type: none;
        margin: 1em;

        a {
          color: white;
          font-weight: 600;

          &.nuxt-link-active {
            color: gray;
          }
        }
    }
}
</style>
