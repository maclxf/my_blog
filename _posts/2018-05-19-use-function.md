---
layout: post
title: "2018-05-19周会"
date: 2018-05-19 23:22:20 +0800
description:   # Add post description (optional)
img:  2018-05-19.jpg # Add image post (optional)
list_img:  2018-05-19-list.jpg
tags: ['function']# add tag
---
## 上周codereview执行结果回馈

<!--
	引出问题，看一个我注册的账号
-->
* 如何判断字符串中是否包含某个字符串（某段）比如在'123@qq.com' 中 '@'？


<!--
	如何判断字符串中是否包含某个字符串（某段）
	目的：学习两个函数
	补完内容：用途，参数以及参数类型，返回值，注意事项
-->
<a href="#" id="show_action">先点我</a>
<p id="show_content" class="hidden" >
    <a href="http://php.net/manual/zh/function.strpos.php" id="show_action">strpos</a><br>
	<a href="http://php.net/manual/zh/function.strstr.php" id="show_action">strstr</a><br>
	expload
</p>

<!--
	给定的例子adi-fr.dev/test/test_strop
	$str = '123@qq.com';
	if (strripos($str, '@')) {
	    echo '有@符号';
	} else {
	    echo '没有@符号';
	}
-->
<a href="#" class="click_me" data-show_where="code_part1">再点我</a>
<p id="code_part1" class="hidden" >
	<code>
	$str = '123@qq.com';
	if (strripos($str, '@')) {
	    echo '有@符号';
	} else {
	    echo '没有@符号';
	}
	</code>
</p>

<!-- PHP宽松的类型系统提供了许多不同的方法来检测一个变量的值。然而这也造成了很多问题。 使用==来检测一个值是否为null或false，如果该值实际上是一个空字符串或0，也会误报 为false。 -->
<a href="#" class="click_me" data-show_where="code_part2">然后点我</a>
<p id="code_part2" class="hidden" >
	PHP宽松的类型系统提供了许多不同的方法来检测一个变量的值。然而这也造成了很多问题。 使用==来检测一个值是否为null或false，如果该值实际上是一个空字符串或0，也会误报 为false。
</p>

<!-- 为何返回值要尽可能统一类型 -->
<a href="#" class="click_me" data-show_where="code_part3">最后点我</a>
<p id="code_part3" class="hidden" >
	返回值要尽可能统一类型<br>
	即使不能保证也应在备注中描述清楚
</p>

## 分享
> 遇到大坑小坑常做记录，周会分享，大家学习，共同进步

* 陈喆`array_merge`和'array() + array()'的区别
<a href="../assets/attchment/2018-05-19/cz_share.rar" >点击下载</a>


## 绩效追踪
> 工作的时间做工作相关的事情

* 任务完成率

|  姓名  | 占当月 |
|--------|------|
| 余林   |27.84%|
| 何安平 |27.50%|
| 陈喆   |35.43%|
| 李彬   |26.56%|
| 罗鑫   |35.86%|

* bug率
 * 李彬：
 	* 会员点击【删除】并确定后还是可以重复点击
 * 余林：
 	* 在线填报的宣传图无法访问链接
	* 导入奶粉渠道备案商品功能，导入失败


## 项目进度
> 会前整理好本周的工作，体现出可实施性。

* EDK
	* 调整上周测试出现的问题后，再完成一次流程测试
* FR：
	* 邮件中的内容
	* 提出BUG的整改
	* base_url的处理
	* 导入奶粉渠道备案商品功能，导入失败


## 周会记录
* <a href="../assets/attchment/2018-05-19/mk_content.docx" download="周会记录.docx">周会记录</a>


## 备注
* 讨论 如何用框架使用的 `OR WHERE` VS `$this->db->or_where`
* 罗鑫 总结如何调试ios兼容性的问题并分享
* 李彬 uploadfive 的使用介绍


