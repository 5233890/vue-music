<template>
  <div>recommend</div>
</template>

<script>
  import {getCommend} from 'api/recommend.js'
  import {ERR_OK} from 'api/config'
  export default {
    created () {
      this._getRecommend()
    },
    methods: {
      _getRecommend () {
        getCommend().then(res => {
          if (res.code === ERR_OK) {
            console.log('res', res.data.slider)
          }
        })
      }
    }
  }
</script>

<style scoped></style>
