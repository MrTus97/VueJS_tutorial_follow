<template>
	<div class="demo-slot">
		<comp-tabs title="Tiêu đề của tabs">
			 
		</comp-tabs>
	</div>
</template>

<script>
import CompTabs from './CompTabs.vue'
export default {
	name: 'demo-slot',
	components: {
		CompTabs,
	},
	data(){
		return {

		}
	},
	methods: {

	}
}
</script>

<style>
	.demo-slot{
		margin-top: 100px;
		padding: 100px 30px;
		border: 1px solid #000;
	}
</style>