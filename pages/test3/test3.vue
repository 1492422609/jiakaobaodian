<template>
     <view class="content">
         <view class="page-section indexListBox">
            <view class="indexList" v-for="(item , index) in homePosts" :key="index">
                <view class="title">{{item.title}}</view>
                <view v-html="item.content"></view>
            </view>
        </view>
    </view>
</template>
<style>
    .indexList uni-image {
            width: 100%;
            height: 130px;
            background: #eaeaea;
        }
        .indexList {
            margin-top: 15px;
            margin-bottom: 15px;
        }
        .indexList .title {
            background: #000;
            color: #fff;
            font-size: 16px;
            line-height: 37px;
            padding: 0 10px;
            margin-top: -5px;
    }
       .indexListBox{
           margin-top: 20px;
       }
</style>
<script>
     export default {
            data() {
                return {
                   homePosts:[],
                }
            },
             onLoad() {
                         //教程 uni-app:渲染app的首页文章数据第一步:将该方法加入onLoad中，使页面一加载的时候就获取文章列表
                         this.getHomePosts();
                     },
            methods:{
                getHomePosts(){
                    var _self = this;
                    uni.request({
                        url: 'http://192.168.1.156:10086/smart-admin-api/article/page/list',//接口地址
                        header: {
                          'content-type': 'application/x-www-form-urlencoded',  //自定义请求头信息
                        },
                        success: (res) => {
                            // 请求成功之后将文章列表数据赋值给homePosts
                            _self.homePosts=res.data.data.list;//根据API数据找到对应的集合
                        }
                    });
                }
            }
      
        }
</script>