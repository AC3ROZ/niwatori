<template>
	<div class="timeline">
		<el-card class="box-card">
      <div class="tweets">
        <tweet v-for="(tweet, index) in tweets" :tweet="tweet" :index="index" :route="$route"></tweet>
      </div>
		</el-card>
	</div>
</template>
<style scoped>
.timeline {
  height: 100%;
  overflow-y: scroll;
}
.tweets {
  height: 100%;
}
</style>
<script>
import Tweet from './Tweet/Tweet'
import { mapGetters } from 'vuex'
export default {
  computed: {
    ...mapGetters(['tweets'])
  },
  components: {
    Tweet
  }
}
</script>
