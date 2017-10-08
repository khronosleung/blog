# 关于github的2步验证（谨慎使用及保存）

故事因由：

1. 开启2步验证后，没有保存 `recovery code`
2. iphone使用DFU模式升级IOS11，Google Autenticator坑我一把，没有与我任何账号关联记录
3. macbook使用抹盘升级至macOS High Sierra，公私钥没有备份（我不知道备份了后能不能继续使用）
4. 一面懵逼的情况找到[小鱼周凌宇](http://zhoulingyu.com/) 妹子的一篇文章（[传送门](http://zhoulingyu.com/2017/02/07/%E6%89%BE%E5%9B%9E%E4%B8%A2%E5%A4%B1%E7%9A%84-Github-%E8%A1%80%E6%B3%AA%E5%8F%B2%EF%BC%88%E8%B0%A8%E6%85%8E%E4%BF%9D%E7%AE%A1-2FA-%E9%AA%8C%E8%AF%81%EF%BC%89/)），情况相近
5. 最后找github客服**证明我妈是我妈**



apple带来的2步验证的体验，于是在原本的github账号([@kidney](https://github.com/kidney))开启这个功能，

传送门：https://github.com/settings/two_factor_authentication/intro

github开启2步验证提供2种选择：

- TOTP application
- ~~短信（中国不支持）~~

当时我使用了TOTP application的方式，其原理介绍看妹子blog



### 客服过程

跟妹子情况一致，客服要我run 

```shell
ssh -T git@github.com verify
```

结果是：

```shell
Permission denied (publickey).
```

*如果返回内容带有*`Warning`和*ip地址，恭喜你受到GFW保护*

已经是一台全新的电脑，除了我原来的公匙（公司git有记录）和登陆邮箱地址，我根本没有任何资料在手足以证明我妈是我妈，客服不能靠公匙来关闭我的2步验证



### 结果

github客服只能帮忙从原账号取消与邮箱地址关联，然后用原来的邮箱地址注册一个新账号



### 建议

1. `recovery code` 死活都要保存，善用1password这些工具
2. Google Autenticator是一个坑（或许我使用姿势不对）
3. 用Lastpass,1Password, Keeper这些软件做个高强度密码，别无事折腾2步验证