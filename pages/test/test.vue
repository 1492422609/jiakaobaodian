<template>
        <view>
                <view v-for="(item,i) in lists" :key="i">
                        <view><view :class="['aaa', type == 1 ? 'aaa' : type == 2 ? 'active' : 'classB']" @click="dianwo(item)">{{item.op1}}</view></view>
                        <view><view :class="['aaa', type1 == 1 ? 'aaa' : type1 == 2 ? 'active' : 'classB']" @click="dianwo1(item)">{{item.op2}}</view></view>
                        <view><view :class="['aaa', type2 == 1 ? 'aaa' : type2 == 2 ? 'active' : 'classB']" @click="dianwo2(item)">{{item.op3}}</view></view>
                        <view><view :class="['aaa', type3 == 1 ? 'aaa' : type3 == 2 ? 'active' : 'classB']" @click="dianwo3(item)">{{item.op4}}</view></view>
                </view>
        </view>
        
</template>

<script>
export default {
        data() {
                return {
                        type: 1,
                        type1: 1,
                        type2: 1,
                        type3: 1,
                        
                        currentIndex: 0,
                        lists: [
                                {
                                        op1: 'A',
                                        op2: 'B',
                                        op3: 'C',
                                        op4: 'D',
                                        answer: 'B'
                                }
                        ]
                };
        },

        methods: {
                dianwo(e) {
                        if(e.op1===e.answer){
                                this.type=2
                                this.type1=1
                                this.type2=1
                                this.type3=1
                        }else{
                                this.type=3
                                this.type1=1
                                this.type2=1
                                this.type3=1
                        }
                },
                dianwo1(e){
                        if(e.op2===e.answer){
                                this.type1=2
                                this.type=1
                                this.type2=1
                                this.type3=1
                        }else{
                                this.type1=3
                                this.type=1
                                this.type2=1
                                this.type3=1
                        }
                },
                dianwo2(e){
                        if(e.op3===e.answer){
                                this.type2=2
                                this.type=1
                                this.type1=1
                                this.type3=1
                        }else{
                                this.type2=3
                                this.type=1
                                this.type1=1
                                this.type3=1
                        }
                },
                dianwo3(e){
                        if(e.op3===e.answer){
                                this.type3=2
                                this.type=1
                                this.type1=1
                                this.type2=1
                        }else{
                                this.type3=3
                                this.type=1
                                this.type1=1
                                this.type2=1
                        }
                }
                        
        }
};
</script>

<style lang="scss" scoped>
page {
        background: #f2f3f6;
}

.aaa {
        background: red;
        width: 100%;
        height: 50rpx;
        margin-top: 10rpx;
}
.calssA {
        background-color: blue;
}
.active {
        background-color: black;
}

.classB {
        background-color: yellow;
}
</style>