<template>
	<view class="content">
        <div v-if="list[0]" style="background: #d8dce1">
            {{list[0].name}}
            <input v-model="list[0].name" style="border: 1px solid red">
        </div>
		<view v-for="item in list" style="padding: 10px">
		    <child-item v-model="item.name" :item="item" :name="item.name"></child-item>
		</view>
	</view>
</template>

<script>
	import ChildItem from "./childItem";
    export default {
        components: {ChildItem},
        data() {
			return {
				list: [
					{
						name: 'Hello'
					}
				]
			}
		},
		onLoad() {
		},
		methods: {

		}
	}
</script>

<style>

</style>
