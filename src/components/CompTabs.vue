<template>
	<div class="compo-tabs">
		<div class="tabs-title">
			<span>{{title}}</span>
			<ion-icon name="heart"></ion-icon>
		</div>
	</div>
</template>

<script>
export default {
	name: 'comp-tabs',
	data(){
		return{

		}
	},
	props:{
		title: String,
	},
	methods: {
		

	}
}
</script>

<style>
	.demo-ref {
		margin-top : 100px;
		padding: 100px 30px;
		border: 1px solid  #000;
	}
	.avatar {
		color: #fff;
		border: 2px solid #333;
		padding: 12px 15px;
		background-color: #333;
		transition: all .3s ease;
	}

	.avatar:hover {
		color: #333;
		background-color: #fff;
	}
</style>