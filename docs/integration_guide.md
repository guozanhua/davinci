---
layout: global
title: 集成整合支持
---


集成整合能力是指无缝集成到三方系统里，使其和三方系统融为一体。通过使用 Davinci 的分享功能就可以做到这点。分享有两个层级，一是分享单个 Widget，二是分享 Dashboard/Display。分享都支持“普通分享”和“授权分享”。同时，Schedule 功能能以邮件的形式定时分享若干个 Widget/Dashboard/Display。另外，Davinci 还具备让用户下载的能力，无论是在登录的页面还是在分享页面，你都能做到。

### 1 分享 Widget

选中某一 Widget，点击“分享”，选择分享类型，完整的 Widget 将呈现在你面前。![integration_share_widget](./img/integration_share_widget.png)

### 2 分享 Dashboard

Dashboard 面板右上角点击“分享”，选择分享方式，你将看到当前仪表板所有的 Widget 信息。

![inregration_share_dashboard](./img/integration_share_dashboard.png)

### 3 分享 Display

进入 Display，可以在这里根据喜好自由布局，所以当你制作出一个非常漂亮实用的大屏面板之后，可以点击菜单栏的“分享”按钮，让更多的人看到你的成果。

![integration_share_display](./img/integration_share_display.png)

### 4 Schedule 定时分享

在 Schedule 中进行相关配置，通过邮件的形式发送给想要分享的人。

![integration_schedule](./img/integration_schedule.png)

### 5 组件 CSV 下载

**与三方系统整合**

- **base64 编码**

  ```
  IHsiZiI6ImNpdHk9ICYjMzk75YyX5LqsJiMzOTsiLCJwIjpbeyJrIjoic3RhcnRUaW1lIiwidiI6IiYjMzk7Mj AxNy0wNy0wMSAwMDowMDowMCYjMzk7In0seyJrIjoiZW5kVGltZSIsInYiOiImIzM5OzIwMTgtMDctMDIgMDA6 MDA6MDAmIzM5OyJ9XX0=
  ```

- **url encode**

  ```
  IHsiZiI6ImNpdHk9ICYjMzk75YyX5LqsJiMzOTsiLCJwIjpbeyJrIjoic3RhcnRUaW1lIiwidiI6IiYjMzk7Mj AxNy0wNy0wMSAwMDowMDowMCYjMzk7In0seyJrIjoiZW5kVGltZSIsInYiOiImIzM5OzIwMTgtMDctMDIgMDA6 MDA6MDAmIzM5OyJ9XX0%3d
  ```

- **并入 share url 中**，如：

  Widget

  ```
  http://localhost:8080/share.html#share/dashboard?shareInfo=DA1C3E7DAF7EC46FDC39861F361C78B7517FC6CEF4F1ED425FFF75A2CB7527D3ABD4F0725AF12462EE9485E57D5234013FD9671DD7069F3C8B476F77AABD65EF7BFC4FAFB8ACBB3360E96D5FFEB8AF7BE1C597E57BD00C16C7B90885898178693E61136AC05A74E8CBF291648DE0193461763C3A6E2B2663E58C656D77C2BC1BE2FF4F26C5F92B4EE8F049B1D6C23B562E64FC6D33B26907C885A73F29A73FB7CB1264E69D7C009D524EC6907286B7E04D8CEA9412B160261E16F5E6BCAECE589AE1E63E15DAC434301EDF5B8504FC07687FFB5AFF2A6305BAE532C35879BFEE1872F0DBA32804D149FC137A168E43ED314FAD6F76B12DC58CFFA991EFDF1532&type=widget
  ```

  Dashboard

  ```
  http://localhost:8080/share.html#share/dashboard?shareInfo=DA1C3E7DAF7EC46FDC39861F361C78B7517FC6CEF4F1ED425FFF75A2CB7527D3ABD4F0725AF12462EE9485E57D52340195C57902158F3E592877DB7ACD9CA4059CCE6FBEA29AAD5DB305F13254166B47DAA9E15357E0113F85405C090E7DCA4CB2A61355A235625968FC7D51AA20A6E9221DB74CC3251DA990F8E9AE35D77F7543419A59BADDBEF1AF47E27705A851E02E0733E1D60D4B67CA0D0087AC8C32BC6215DB3F6443706988CFE00FF483700F75AB71D8FB2A8242B7D34144DEF92A285EF81B820C85F9EAF708618516197A0E85671DDA93650CE9E0027F988B5D9E2E6BBDC440B489E304FF5FD127272F22AD366C5821A3FC551D679EB7F2A21E6DD6&type=dashboard
  ```

  Display

  ```
  http://localhost:8080/share.html#share/display?shareInfo=DA1C3E7DAF7EC46FDC39861F361C78B7517FC6CEF4F1ED425FFF75A2CB7527D3ABD4F0725AF12462EE9485E57D523401AFA249F2FD1E0875CED644F5814CD5A7EE148482695E82877125E2E348F5CBDDE1C597E57BD00C16C7B90885898178693E61136AC05A74E8CBF291648DE019345BED14D831F24630E4D45418C604EB01E2FF4F26C5F92B4EE8F049B1D6C23B56322941CC2F0BABDDE8071E3E53BA9AE5EEE5A1F51B07F173E086CF5F7D9A59D765170BD669E73210B8EC4D8B5122DCC0C49059BD3927201C50C31F1DB5239CBC08177A64A54EFEE415CCA11B0DDBE4F1FCE0D3F74B750B5188039DCA7881A8CB0AEB311D12DE58C36CE9E5A19E7C73C5
  ```
