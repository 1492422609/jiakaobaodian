<template>
    <view>
        <view v-for="(item,pri) in items" :key=item.price :class="item.price==4 ? 'addclass' : '' " @click='onclick(pri)' class="fruits">
            <text>{{item.name}}</text>
            <text>{{item.price}}</text>

        </view>
    </view>
</template>

<script>
    export default {
			// 页面加载完给自然方向，它就能根据用户横竖自动切换
			onLoad() {
					// #ifdef APP-PLUS
					plus.screen.lockOrientation('default');
					// #endif
				},
			// 页面关闭时清除横屏正方向
			onUnload() {
					// #ifdef APP-PLUS
					plus.screen.lockOrientation('portrait-primary');
					// #endif
				},

        data() {
            return {
                items: [{
                        name: '苹果',
                        price: '5'
                    },
                    {
                        name: '香蕉',
                        price: "8"
                    },
                    {
                        name: '西瓜',
                        price: '4'
                    },
                    {
                        name: '桃子',
                        price: '3'
                    },
                    {
                        name: '草莓',
                        price: "6"
                    },
                    {
                        name: '樱桃',
                        price: '10'
                    },
                ],
                isactive: '1'
            }
        },
        methods: {
            onclick(index) {
                console.log(index)
				
                //将点击的元素的索引赋值给bian变量
                this.isactive = index
				console.log(this.isactive)
            }
        }
    }
</script>

<style>
    .fruits {
        margin: 50upx;
    }
    .addclass {
        color: red;
    }
</style>
