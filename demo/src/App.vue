<template>
	<div>
		<ul>
			<li v-for="item in items">
				<h2>
      			<input type="checkbox" />
      			{{ item.value }}
      		</h2>
				<ul>
					<li v-for="twoitem in item.twoitems">
						<h3>
      			<input type="checkbox" />
      			{{ twoitem.value }}
      		</h3>
      		<ul>
					<li v-for="threeitem in twoitem.threeitems">
						<h3>
      			<input type="checkbox" />
      			{{ threeitem.value }}
      		</h3>
					</li>
				</ul>
					</li>
				</ul>
			</li>
		</ul>
	</div>
</template>

<script>
	export default {
		data() {
			return {
				items: [{
					value: '风险大盘概览',
					twoitems: [{
						value: '风险趋势',
						threeitems: [{
							value: '风险事件趋势',
						}, {
							value: '风险结果分布'
						}, {
							value: '事件类型分布'
						}]
					}, {
						value: '风险指标'
					}]
				}, {
					value: '贷前审核服务'
				}]
			}
		}
	}
</script>
<style>
	#app {
		font-family: 'Avenir', Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		text-align: center;
		color: #2c3e50;
		margin-top: 60px;
	}
	
	ul {
		list-style: none;
	}
</style>