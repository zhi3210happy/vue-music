# 基于Vue.js的音乐播放器（Webapp）

--------
### 概述
#### 视图层
> 
* 推荐页
* 歌手页
	* 歌手详情
* 歌曲排行榜
	* 排行榜详情
* 搜索页
* 用户中心

#### 数据来源
部分接口设置了： 
``` javascript
  headers: {
      referer: 'https://c.y.qq.com/',
      host: 'c.y.qq.com'
```
以此绕过`host`的限制并跨域。

#### 技术栈
> 
* [x] Vue
* [x] Vuex
* [x] Vue-Router
* [x] Vue-cli
* [x] Stylus
* [x] Axios
* [x] nginx
* [x] Express

```
#### 数据处理
`src/common/js/song.js` 文件下对数据做了处理方便调用。

`src/common/js/jsonp.js` 文件对josnp 进行包装返回Promise 方便做后续动作。


#### 线上地址：[demo](http://music.zhi3210happy.xin/)。

每个跳转都是用`Vue`的`transition`动画。包括路由之间切换时的简单动画，播放器打开时的动画等等。


### 构建
#### 开发环境

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

#### 线上部署
# cd server
npm install
npm start


采用Nginx 转发端口 然后 使用 Express 监听相应端口并做路由处理，详细后续补充。
