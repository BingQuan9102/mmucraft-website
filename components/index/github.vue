<template>
  <div class="card gl-bg-white-30 mt-3 rounded shadow">
    <div class="card-header text-center">
      <MCSubtitle>Github</MCSubtitle>
    </div>
    <div class="card-body text-white text-center">
      <b-img src="/getstart/github.png" />
      <b-row
        v-for="(item,i) in items"
        :key="`item-${i}`"
        class="mt-3 justify-content-center"
      >
        <b-col cols="2" class="mr-2">
          <b-img :src="`/getstart/${item.image}.png`" class="mr-2" />
        </b-col>
        <b-col cols="5" sm="7" class="text-left">
          <div>
            {{ item.title }}
          </div>
          <a :href="item.link" target="_blank">
            See repository
          </a>
        </b-col>
      </b-row>
    </div>
  </div>
</template>

<script>
import MCSubtitle from '~/components/mc/mc-subtitle'

export default {
  components: {
    MCSubtitle
  },
  data: () => {
    return {
      items: [
        {
          image: 'diamond',
          title: 'MMUCraft Website',
          link: 'https://github.com/keishidesu/mmucraft-website'
        },
        {
          image: 'book',
          title: 'API',
          link: 'https://github.com/Tajam/mmucraft-api'
        },
        {
          image: 'bot',
          title: 'Discord Bot',
          link: 'https://github.com/Tajam/mmucraft-discord-bot'
        }
      ]
    }
  }
}
</script>

<style scoped>
a {
  color: rgb(0,0,128)
}

a:hover {
  color: rgb(0,0,128)
}
</style>
