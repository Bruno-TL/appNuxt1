<template>
  <div>
    <pre>{{ $store.state.user }}</pre>
    <br>
    <pre>{{ user }}</pre>
  </div>
</template>

<script>
import {mapState} from 'vuex';
export default {
  name: 'IndexPage',
  computed: {
    ...mapState({
      user: state => state.user
    })
  }
}
</script>
