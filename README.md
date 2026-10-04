# TikTok Shop 静态授权回调页

这个公共仓库只包含一个静态授权提示页，不包含 App Key、App Secret、Access Token 或 Refresh Token。

GitHub Pages 地址：

```text
https://ximengzhe.github.io/tiktok-shop-callback-pages/tiktok-shop/callback/
```

授权结束后，TikTok Shop 会把 `code` 和 `state` 放在浏览器地址栏。页面不显示这些值；请复制完整浏览器地址并粘贴到本地“上架助手”。

## 新应用的独立入口

```text
https://ximengzhe.github.io/tiktok-shop-callback-pages/tiktok-shop/callback-2/
```

在新官方应用的重定向链接，以及本地程序中新应用的 HTTPS 回调地址中填写上面的完整地址，包括末尾 `/`。原应用继续使用原地址。

新入口不绑定 App Key，也不包含密钥或店铺凭据。无授权参数时显示“回调页已就绪”；收到 `code` 与 `state` 时提供复制完整地址按钮，仍由本地程序校验授权并交换令牌。错误、缺失或重复参数不表示授权成功。本页不加载第三方资源，不将参数写入页面正文或浏览器存储。
