<template lang="html">
  <div id="main"></div>
</template>

<script>
export default {
  name: 'header',
  data() {
    return {
      active: 'home'
    }
  },
  methods: {
    makeActive(item) {
      this.active = item;
    }
  }
};

</script>

<style lang="css">

*{
	margin:0;
	padding:0;
}

body{
	font:15px/1.3 'Open Sans', sans-serif;
	color: #194d33;
	text-align:center;
}

a, a:visited {
	outline:none;
	color:#194d33;
}

a:hover{
	text-decoration:none;
}

section, footer, header, aside, nav{
	display: block;
}

nav{
	display:inline-block;
	margin:60px auto 45px;
	background-color:#00B16A;
	box-shadow:0 1px 1px #ccc;
	border-radius:2px;
}

nav a{
	display:inline-block;
	padding: 20px 40px;
	color:#fff !important;
	font-weight:bold;
	font-size:16px;
	text-decoration:none !important;
	line-height:1;
	text-transform: uppercase;
	background-color:transparent;

	-webkit-transition:background-color 0.25s;
	-moz-transition:background-color 0.25s;
	transition:background-color 0.25s;
}

nav a:first-child{
	border-radius:2px 0 0 2px;
}

nav a:last-child{
	border-radius:0 2px 2px 0;
}
  
.nuxt-link-active {
  background-color:#1BA39C;
}


p{
	font-size:22px;
	font-weight:bold;
	color:#7d9098;
}

p b{
	color:#ffffff;
	display:inline-block;
	padding:5px 10px;
	background-color:#c4d7e0;
	border-radius:2px;
	text-transform:uppercase;
	font-size:18px;
}
.resource {
  margin: 20px 0;
}
</style>
