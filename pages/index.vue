<template>
  <section class="container">
    <div>
      <logo/>
      <h1 class="title">
        nuxt
      </h1>
      <nuxt-link to="/about">ABOUT</nuxt-link>
      <h2 class="subtitle">
        My mind-blowing Nuxt.js project
      </h2>
      <first-component />
      <user-component />
      <counter-component :title="title" />
      <slot-component>
        <div>ワイヤで</div>
        <div slot="it_is_slot">
          <div>slot内やで</div>
        </div>
      </slot-component>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          class="button--green">Documentation</a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="button--grey">GitHub</a>
      </div>
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'
import FirstComponent from '~/components/FirstComponent.vue'
import UserComponent from '~/components/users/FirstComponent.vue'
import CounterComponent from '~/components/CounterComponent.vue'
import SlotComponent from '~/components/SlotComponent.vue'

export default {
  components: {
    Logo,
    FirstComponent,
    UserComponent,
    CounterComponent,
    SlotComponent
  },
  data() {
    return {
      title: 'counterのページだよ！'
    }
  }
}
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
