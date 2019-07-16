# SDK Q&A

[TOC]

---

#### **Q:**  本文档使用方法?

**A:**  快捷键`Ctrl + F`(windows) 或者 `command + F`(Mac OS) 在页面中搜索关键词或者下载文档后在文本编辑器中搜索.

---

#### **Q:** 为什么我HTML引入了SDK调试时报`trim`这个错误?
![trim-error](https://static-oss.qutoutiao.net/sdk/questions_and_answers/trim_error.png)

**A:** 打开chrome的`Toggle device toolbar`然后刷新页面

![Toogle-device-toolbar](https://static-oss.qutoutiao.net/sdk/questions_and_answers/Tggle-device-toolbar.png)

---

#### **Q:** 为什么我调用广告相关方法不起作用?

**A:** 联系运营开通SDK中广告权限

---

#### **Q:** 为什么我开通广告权限了,还是不显示广告?广告接口返回`204`状态码?
![204_state](https://static-oss.qutoutiao.net/sdk/questions_and_answers/204_state.png)


**A:**  204表示接口是正常的,此时无广告分配.

---

#### **Q:** 我之前广告接入了`qtt_help.js`,现在为什么要改掉?

**A:** 出于 **优化游戏** 的考虑,在游戏初始化需要下载的文件总体积变小了,总时间将缩短,因为将SDK和`qtt_help.js`编译在一起,公共库部分不用打包两次,相应代码不需要解析两次.

---

#### **Q:** 我改换成现在的广告接入方式,我的代码需要做出什么改动?

**A:**
1.  `qtt_help.ad`上的方法全部变更到`qttGame`上
2.  SDK地址更换成最新地址即可

---

#### **Q:** 我现在使用`qtt_help.js`也用着好好的,为什么要换呢?

**A:** `qtt_help.js`已经不再维护,后期新功能将不会出现在`qtt_help.js`上,所以应该尽快更新以保持同步.

---