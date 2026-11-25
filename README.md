# 双币日内雷达

单文件 BTC / ETH 日内观察页，用 GitHub Pages 做静态托管，手机浏览器直接打开。

预期地址（合并并开启 Pages 之后）：

https://dayu713.github.io/btc-eth-radar/

## 页面范围

`index.html` 是完整源文件，计算都在浏览器里完成。

- 只读取公开行情：Binance USDⓈ-M 的 BTCUSDT、ETHUSDT，以及 Deribit 公共期权接口
- 保留方向观察、关键价位、挂单墙辅助、触价提醒和本机强平估算
- 没有账户、没有 API Key、不下单
- 地域限制、限流或读取失败会显示错误；不使用示例价格或假行情补位
- 页面横幅在打开期间可用。系统通知必须由使用者授权，手机浏览器可能不允许后台持续提醒；关闭或休眠后不再监控

## 发布

站点使用仓库根目录，不绑定自定义域名，也不使用付费服务。

1. 把此变更合并进默认分支 `main`。
2. 打开仓库 **Settings → Pages**。
3. **Build and deployment** 选择 **Deploy from a branch**。
4. Branch 选择 `main`，文件夹选择 `/ (root)`，然后保存。
5. 等 GitHub 显示站点已发布，再访问上面的地址。

请保留空文件 `.nojekyll`。页面脚本含有 `${{...}}` 写法；开启 Jekyll 后，构建会改写脚本或直接失败。不要添加 Jekyll 主题或 `_config.yml`。
