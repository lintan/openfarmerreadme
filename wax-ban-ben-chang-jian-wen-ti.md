# WAX版本常见问题

1.程序日志显示，已经成功喂鸡，成功浇水，成功采集了，为什么Chrome中的游戏界面上还是显示没有喂鸡，没有浇水，没有采集？

> 这是因为程序是通过直接调用智能合约的方式进行的操作，Chrome中游戏界面并不会自动更新，实际上只要日志显示操作成功，就已经操作成功了，Chrome中的游戏界面不更新，无需理会，你可以重新开一个Chrome窗口，重新登录游戏查看，到底操作成功了没有

2.无法使用google账号登录，提示此浏览器或应用可能不安全？

[![image](https://raw.githubusercontent.com/encoderlee/OpenFarmer/main/doc/question1.png)](https://raw.githubusercontent.com/encoderlee/OpenFarmer/main/doc/question1.png)

这是因为Chrome本身就是google家的，google判断到该Chrome浏览器正受程序控制，便判定为不安全，不允许登录。解决办法就是在WAX云钱包登录界面，点【Forgot Password】（忘记密码），输入google邮箱账号，根据提示重置密码（可以重置为和原来一样的密码），重置成功后，便可在WAX云钱包登录界面，直接输入google邮箱账号和重置后的密码进行登录，而不需要点google图标，不需要通过google账号登录。
