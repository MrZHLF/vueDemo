<template>
	<footer>
		<p>{{copyrigth}} {{title}}</p>
	</footer>
</template>

<script>
export default {
  name: 'FooterTitle',
  props: {
    title: {
      type: String
    }
  },
  data () {
    return {
      copyrigth: 'Copyrigth 2017-01-26'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less">
footer {
	width: 100%;
	height: 50px;
	background: #222;
	p{
		color: #fff;
		text-align: center;
		line-height: 50px;
	}
}
</style>
