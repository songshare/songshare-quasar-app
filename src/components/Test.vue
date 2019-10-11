<template>
  <div class="col">
    <div v-bind:id="id"></div>
    <q-btn @click="test">Test</q-btn>
  </div>
</template>

<script>
let reactStandalone = require('../../node_modules/ReactPlayer.standalone')

export default {
  name: 'Test',
  data () {
    return {
      id: Math.random()
    }
  },
  methods: {
    test () {
      console.log('GROS')
      const container = document.getElementById(this.id)
      const url = 'https://youtu.be/rt2e08XNvxg'
      reactStandalone.renderReactPlayer(container, { url, playing: true, controls: true, width: '320', height: '180px' })

      // const container2 = document.getElementById('container2')
      // const url2 = 'https://youtu.be/rt2e08XNvxg'
      // reactStandalone.renderReactPlayer(container2, { url2, playing: true, controls: true, width: '320', height: '180px' })

      // const container3 = document.getElementById('container3')
      // const url3 = 'https://www.youtube.com/watch?v=vpU6jz301MQ'
      // reactStandalone.renderReactPlayer(container3, { url3, playing: true, controls: true, width: '320', height: '180px', onError: () => console.error('erre'), onReady: () => console.error('erre') })
    }

  }
}
</script>
