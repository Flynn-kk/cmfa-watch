# cmfa-watch

盯 [MetaCubeX/ClashMetaForAndroid](https://github.com/MetaCubeX/ClashMetaForAndroid) 的 release。

- 每 15 分钟查一次上游最新 release
- 跟 `state.json` 里记录的 `last_tag` 不同 → 开一个 issue 并 assign 给 `@Flynn-kk`
- issue 的 assign 会触发 GitHub 通知（手机 App 推送 / 邮件），这就是「第一时间知道」

## 为什么不用 fork

GitHub fork **不复制 release**，fork 里只有源码，手机上下不到 APK。所以要单独建这个轻量仓库来做「监听」。

## 备注

- 仓库 60 天无提交会被 GitHub 停掉定时任务，所以脚本每 20 天左右会做一次心跳提交（只改 `checked_at`）
- 想手动触发一次：Actions → Watch ClashMetaForAndroid → Run workflow
