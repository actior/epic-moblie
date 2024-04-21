<!-- home -->
<template>
  <div class="index-container">
    <div class="warpper">
      <h1 class="title"><span>Uniapp H5开发模板</span></h1>
      <h2 class="desc">A Uniapp h5 template with Thor UI</h2>
    </div>
    <tui-list-view color="#777">
      <tui-list-cell v-for="item in list" :hover="false" :arrow="false" :key="item">
        <tui-icon name="check" :size="24" color="#999"></tui-icon>
        <text class="tui-list-cell_name">{{ item }}</text>
      </tui-list-cell>
    </tui-list-view>
    <tui-tabbar
      :tabBar="tabBar2"
      :unlined="true"
      backgroundColor="#F7F7F7"
      :current="current"
      @click="tabbarSwitch"
    ></tui-tabbar>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        list: [
          'Vue-cli4',
          '配置多环境变量',
          'ThorUi 组件按需加载',
          'Less 全局样式',
          'Webpack 4',
          'Vuex 状态管理',
          '请求 封装及接口管理',
          'Webpack 4 vue.config.js 基础配置',
          '配置 proxy 跨域',
          '配置 alias 别名',
          '去掉 console.log',
          'Eslint+Stylelint+Pettier 统一开发规范',
          'Vue-cli4',
          '配置多环境变量',
          'ThorUi 组件按需加载',
          'Less 全局样式',
          'Webpack 4',
          'Vuex 状态管理',
          '请求 封装及接口管理',
          'Webpack 4 vue.config.js 基础配置',
          '配置 proxy 跨域',
          '配置 alias 别名',
          '去掉 console.log',
          'Eslint+Stylelint+Pettier 统一开发规范',
        ],
        current: 0,
        tabBar2: [
          {
            pagePath: '',
            text: 'extend',
            iconPath: '/static/images/tabbar/index.png',
            hump: true,
            selectedIconPath: '/static/images/tabbar/index.png',
          },
        ],
      };
    },
    methods: {
      tabbarSwitch(e) {
        //获取登录状态，此处默认未登录
        let isLogin = false;
        if (e.verify && !isLogin) {
          this.tui.toast('您还未登录，请先登录');
        } else {
          this.current = e.index;
        }
      },
    },
  };
</script>
<style lang="less" scoped>
  .index-container {
    .warpper {
      padding: 20rpx;
      background: #fff;
      .tui-list-cell_name {
        padding-left: 100rpx;
        display: flex;
        align-items: center;
        justify-content: center;
      }
      .title {
        margin: 0 0 20rpx;
        font-size: 60rpx;

        .title img,
        .title span {
          display: inline-block;
          vertical-align: middle;
        }

        img {
          width: 70rpx;
        }

        span {
          margin-left: 30rpx;
          font-weight: bold;
        }
      }

      .desc {
        padding: 30rpx;
        color: #999;
        font-size: 32rpx;
      }
    }
  }
</style>
