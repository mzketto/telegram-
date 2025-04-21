# Mr.Robot
### KV空间创建名称填写 nfd
私聊机器人有以下优势：不暴露原账号、解决 +86 号码无法私聊的问题、无需服务器，简单易用。发信人,截图:收信人,截图:准备工作:由于部分国外网络访问受限，建议准备一个稳定的网络工具，以保证能够顺利打开和下载资源。在搭建前，请确保拥有以下账号：👉推荐网络工具使用：(此项是付费服务，已经测试能长期稳定使用)https://user.vpn4.top/s/#/register?code=dEe7WSkWCloudflare 账号https://www.cloudflare.com/zh-cn/Telegram 账号以上三个缺一不可.搭建步骤准备好上述准备工作,开始搭建教程1. 申请 Telegram 机器人 Token•在@BotFather处创建 Bot，设置名称和用户名。•发送/setjoingroups禁止 Bot 被添加进群组。
•复制生成的Token（格式示例：6330000000:AAAAAAAAAAA-AAAAAAAAAAAAAAAAA）。https://t.me/BotFather2. 生成随机 UUID•访问UUID Generator，获取一个随机UUID作为secret。https://www.uuidgenerator.net3. 获取 Telegram 用户 ID•通过@username_to_id_bot查询你的用户 ID。https://t.me/username_to_id_bot4. 在 Cloudflare 创建 Workerhttps://www.cloudflare.com/zh-cn/先配置环境，再次点这里，选择你创建的workers点进去刚部署完的项目点击设置点击变量和机密点添加这里记得添加三个变量
增加一个ENV_BOT_TOKEN变量，数值为从步骤1中获得的token
增加一个ENV_BOT_SECRET变量，数值为从步骤2中获得的secret
增加一个ENV_ADMIN_UID变量，数值为从步骤3中获得的用户id创建一个KV名称输入nfd,添加然后回到概述在点进去项目名称找到设置点进去找到 绑定 在点添加在点 KV 命名空间选择之前部署好的,名称取一样回到workers页面,选择你刚创建的workers,点击 编辑代码进入这个网页，点击图中按钮复制https://github.com/kissimok/ljj/blob/main/worker.js复制到这个框里,然后点右上角的保存并部署以上都做完后，回到你的workers，有一个访问 点开他你能获得一个网址
类似这样:https://cold-XXXXXXXXXXXX.lunjiejie.workers.dev将这个网址复制到浏览器，在后面添加"/registerWebhook"，然后回车
网页中会弹出OK
至此，Telegram 私聊机器人搭建完成！

转载至：https://mp.weixin.qq.com/s/_A3fRzjUHz08jILyFDIyog
