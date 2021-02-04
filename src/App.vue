<template>
  <div id="app">
		<router-view></router-view>
    <tab-bar>
			<tab-bar-item path="/home">
					<img slot ="item-icon" src = "./assets/img/home.svg" alt="">
					<img slot="item-icon-active"  src = "./assets/img/home-active.svg" alt="">
				<div slot = "item-text">首页</div>
			</tab-bar-item>
			<tab-bar-item path="/category">
				<img slot ="item-icon" src = "./assets/img/category.svg" alt="">
				<img slot="item-icon-active"  src = "./assets/img/category-active.svg" alt="">
				<div slot = "item-text">分类</div>			
			</tab-bar-item>
			<tab-bar-item path="/shopcart">
				<img slot ="item-icon" src = "./assets/img/shopcart.svg" alt="">
				<img slot="item-icon-active"  src = "./assets/img/shopcart-active.svg" alt="">
				<div slot = "item-text">购物车</div>
			</tab-bar-item>
			<tab-bar-item path="/profile">  
				<img slot ="item-icon" src = "./assets/img/profile.svg" alt="">
				<img slot="item-icon-active"  src = "./assets/img/profile-active.svg" alt="">
				<div slot = "item-text">我的</div>
			</tab-bar-item>
		</tab-bar>
    <!-- <router-view/> -->
  </div>
</template>
<script>
	import TabBar from './components/tabbar/TabBar.vue'
	import TabBarItem from './components/tabbaritem/TabBarItem.vue'
	export default{
		name:"App",
		components:{
			TabBar,
			TabBarItem
		}
		
	}
</script>
<style>
*{
	margin: 0;
	padding: 0;
	list-style: none;
	text-decoration: none;
}
</style>
