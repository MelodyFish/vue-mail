<template>
	<div class="tab-bar-item" @click="itemClick()">
		<div>
			<slot v-if="!isActive" name="item-icon"></slot>
			<slot v-else name="item-icon-active"></slot>
		</div>
		<div :class="{active:isActive}">
			<slot name="item-text"></slot>
		</div>
	</div>
</template>

<script>
	
	export default{
		name:'TarBarItem',
		props:{
			path:String
		},
		
		computed:{
			isActive(){
				return this.$route.path.indexOf(this.path) !==-1
			}
		},
		methods:{
			itemClick(){
				this.$router.push(this.path)
			}
		}
	}
</script>

<style>
.tab-bar-item{
		flex: 1;
		height: 49px;
		text-align: center;
		background-color: #f6f6f6;
	}
	.tab-bar-item img{
		width: 24px;
		height: 24px;
		margin-top: 3px;
		vertical-align: middle;
		margin-bottom: 2px;
	}
	.active{
		color: #f00056;
	}
</style>
