<template lang='pug'>
div
  Donate(
    :address='address'
    :displayName='displayName'
    :message='message'
    :showBalance='showBalance'
    :eth='eth'
  )
</template>

<script>
export default {
  layout: 'headerless',
  computed: {
    address () {
      return this.$route.params.address
    },
    displayName () {
      return this.$route.query.n
    },
    message () {
      return this.$route.query.m
    },
    showBalance () {
      return this.$route.query.b
    },
    eth () {
      return this.$route.query.e
    }
  }
}
</script>
