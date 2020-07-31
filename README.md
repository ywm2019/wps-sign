## ~~wps签到打卡得会员~~写的有点仓促，请看原文：[酷安](https://www.coolapk.com/feed/18644146?shareKey=NjAyZTVmM2FhZWY4NWVmNzJhYTE~&shareUid=2751597&shareFrom=com.coolapk.market_9.63)
- 1、wps_sid获取：网页登录wps  https://zt.wps.cn/2018/clock_in?csource=pc_clock_oldactivity按下F12打开控制台 选择network刷新一下网页点击wps的链接进入，查看cookie 有wps_sid那一坨 =后边就是所需的sid（V02开头的那一串，不含’wps_sid=’)
- 2、分享ID获取：左边的复制链接，其中的sid=后面的那一串数字就是分享ID
- 3、SCF代码：登录腾讯云scf，新建一个项目 环境选择node.js10.15，选择本地上传zip包 （下载的代码）选择函数代码，点击 config.js，输入这三个参数wps_sid  第二步获得的id  server酱id
- sckey是为了微信通知提醒，没有的去这里注册http://sc.ftqq.com/3.version，非必填项
- 4、创建定时任务：触发管理 新建触发器 定时任务，填入 0 0 12 * * * *  表示每天12点整执行。
