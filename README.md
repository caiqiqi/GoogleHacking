# some google hacking scripts
These srcipts are from > Google Hacking for Penetration Testers

- 查找所有文档的文本中包含password或者passwd的页面。在那些页面中，只要求显示出那些包含username、userid或者user的页面。对于那些页面，只需要显示csv文件（google是从左到右来读取查询的）
`intext:password |passwd intext:username| userid| user filetype:csv`
当然也可加括号，这样更明显
`intext:(password |passwd) intext:(username| userid| user) filetype:csv`

- Google Hacking 小提示
我们无法简单地证明：真正的黑客总是活跃在灰色地带。filetype操作符给那些真正的Google黑客开辟了另一片有趣的天地。考虑查询filetype:xls -xls。这个查询不应该返回结果，因为所有的XLS文件的URL中都包含XLS，对吗？错。在本书写作之时，这个查询确实给出了7000多条结果别的不说，至少这些结果都是相当有趣的。
`filetype:xls -xls site:edu.cn`
- Google的缓存功能是件让人感到非常惊奇的事情。一个最简单的事实是如果Google曾经抓取了某个网页或者文档，即使源文件现在已经不存在或者更新了，那么你仍然很可能获得它的一个副本。

