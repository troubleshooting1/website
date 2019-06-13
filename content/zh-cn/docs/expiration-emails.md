---
title: 过期邮件提醒
slug: expiration-emails
top_graphic: 1
date: 2016-07-02
lastmod: 2016-07-02
---

{{< lastmod >}}

# 订阅

如果你在创建你账号的时候给Let's Encrypt提供了邮件地址，当你的证书将要被更新的时候，我们将自动的给你发一个到期提醒。
我们将在你证书过期的前20天发送第一次提醒，在过期前第10天和前1天再发送提醒。

# 当你收到过期提醒邮件

如果你的证书已经更新过了，我们将不再发送过期提醒。如果存在具有完全相同名称集的较新证书，无论哪个账号创建的，
我们认为证书需要被更新。如果你发布了一个新的证书，添加或移除了你老的证书相关的名字，你将收到关于你老的证书的过期邮件
提醒。如果您检查当前在您的网站上运行的证书，并且它显示正确的日期，则无需进一步操作。

# 退订

邮件正文有一个链接，可以取消以后的通知。如果你点击这个链接，在接下来的一年你将不会受到任何过期通知。"谁退订了"列表
在隔离环境的通知和生产环境的通知是独立的，你可以随意在隔离环境退订，不会影响生产状态。

注意你退订只在一年内有效，一年之后需要更新。

如果你取消订阅，我们没有办法使你重新订阅。我们的邮件供应商Mandrill[有一个手动机制，我们仍然需要自动化](https://mandrill.zendesk.com/hc/en-us/articles/205582947-About-Unsubscribes).

然而，你可以修改你账号上的邮件地址，从而重新有效的订阅。许多常用的邮件服务把`yourname+1@example.com`和`yourname@example.com`当做一样的。
所以如果你更新你的邮件地址为`yourname+1@example.com`，你将会重新受到过期邮件提醒。使用Certbot：

` ~/certbot/venv/bin/certbot  register --update-registration --email yourname+1@example.com`