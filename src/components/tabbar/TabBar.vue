<template>
	<div class="tab-bar">
		<slot></slot>
	</div>
</template>

<script>
	export default{
		name:'TabBar',
		
	}
</script>

<style>
	.tab-bar{
		
		font-size: 14px;
		display: flex;
		position: fixed;
		left: 0;
		right: 0;
		bottom: 0;
		box-shadow: 0 -1px 2px rgba(100,100,100,.4);
	}
	
	
</style>
