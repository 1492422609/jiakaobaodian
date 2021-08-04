<template>
    <view>
        <view v-for="(item,index) in items" :key=item.index :class="index === isactive ? 'addclass' : 'ddd' " @click='onclick(index)' class="fruits">
            <text>{{item.name}}</text>
            <text>{{item.price}}</text>

        </view>
		<text>{{arr}}</text>
    </view>
</template>

<script>
    export default {
		onLoad(){
			this.arr=this.arr.concat(this.arr1)
			console.log(this.arr.concat(this.arr1))
		},
        data() {
            return {
				arr:['e','w'],
				arr1:['d','d'],
                items: [{
                        name: '苹果',
                        price: '5$',
						index:'0'
                    },
                    {
                        name: '香蕉',
                        price: "3$"
                    },
                    {
                        name: '西瓜',
                        price: '4$'
                    },
                    {
                        name: '桃子',
                        price: '3$'
                    },
                    {
                        name: '草莓',
                        price: "6$"
                    },
                    {
                        name: '樱桃',
                        price: '10$'
                    },
                ],
                isactive:''
            }
        },
        methods: {
            onclick(index) {
                console.log(index)
                //将点击的元素的索引赋值给bian变量
                this.isactive = index
				
            }
        }
    }
</script>

<style>
	.ddd{
		color: blue;
	}
    .fruits {
        margin: 50upx;
		color: black;
    }
    .addclass {
        color: red;
    }
</style>
