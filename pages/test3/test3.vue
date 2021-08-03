<template>
    <view>
        <view v-for="(item,index) in items" :class="index === isactive ? 'addclass' : '' " @click='onclick(index)' class="fruits">
            <text>{{item.name}}</text>
            <text>{{item.price}}</text>

        </view>
    </view>
</template>

<script>
    export default {
        data() {
            return {
                items: [{
                        name: '苹果',
                        price: '5$'
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
    .fruits {
        margin: 50upx;
    }
    .addclass {
        color: red;
    }
</style>
