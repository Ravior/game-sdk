# CPC 游戏接入

### 接入步骤
> 1. 联系商务或运营申请app_id引入 sdk
> 2. 如果需要展示广告,联系商务在SDK中开通广告权限
> 3. [引入SDK](#引入-sdk)
> 4. [广告](./游戏广告接入文档.md),[支付](./游戏支付接入文档.md),[数据上报](./SDK数据上报接入文档.md) API 及用法参看对应[文档](./README.md)
> 5. 其他问题可以先参看[SDK Q&A文档](./SDK_Q&A.md)

### 引入 sdk

在HTML头部引入以下标签

```javascript
<script type="text/javascript" src="//newidea4-gamecenter-frontend.1sapp.com/sdk/prod/h5.v1.0.0.js?spread=required"></script>
```
---

> 使用SDK接入广告时, 如果引用了旧的广告方法文件`qtt_help.js`, 请尽快**升级本新SDK**, 参看[升级原因和方法](./SDK_Q&A.md)

---

> Tip: 务必将`<script>`标签放在HTML靠前位置加载, **禁止**动态加载, 务必在SDK加载完成后再调用`qttGame`的方法,否则可能出现`qttGame is not defined`的错误警告

### 浏览器中调试

1. 打开打开chrome的`Toggle device toolbar`
2. 在游戏地址后面加queryString`?app_id=xxxxx&_NO_BRIDGE_=true`
3. 刷新页面

> queryString加`app_id`保证 SDK 正确识别游戏,`_NO_BRIDGE_`使浏览器忽略桥接

### 注意事项

> `app_id`联系商务或运营申请

> 如果游戏文件存在于本地, **禁止**以`ftp`协议打开游戏文件调试,只允许`http`或`https`方式的server中运行

> 调试广告时请确保系统未安装广告拦截软件且浏览器未安装广告拦截插件，否则将导致[广告js加载出错`net::ERR_BLOCKED_BY_CLIENT`](./SDK_Q&A.md)
> (如果不想卸载相关软件和插件，请暂时关闭广告拦截功能，并开启浏览器无痕式窗口/隐私模式调试)

> 如果游戏开发使用了**`cocos`引擎**,请勿在引擎中开启**全屏**设置, 否则将会导致不可预料的显示问题
> (这些问题在某些高端机型出现,所以强烈不建议开启)
